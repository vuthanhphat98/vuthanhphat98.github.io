---
title : "Tạo IAM Role cho Lambda"
date : "2024-07-27" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

### Tạo IAM Role

Hàm Lambda của chúng ta cần được cấp quyền để tương tác với các dịch vụ AWS khác. Thay vì cấp quyền trực tiếp, chúng ta tạo một vai trò (Role) mà Lambda có thể "đảm nhận" (assume). Điều này tuân thủ **nguyên tắc quyền tối thiểu (Principle of Least Privilege)**, một nền tảng của bảo mật trên đám mây.

1\. Trong AWS Console, tìm đến dịch vụ **IAM** (Identity and Access Management).
![createiamrole1](/images/image23.png)
2\. Chọn **Roles** từ menu bên trái và nhấn **Create role**.
![createiamrole2](/images/image33.png)
3\. **Select trusted entity** (Chọn thực thể tin cậy):
+ **Trusted entity type:** Chọn **AWS service**. Điều này có nghĩa là bạn đang cho phép một dịch vụ của AWS (trong trường hợp này là Lambda) đảm nhận vai trò này.
+  **Use case:** Chọn **Lambda**. Lựa chọn này sẽ tự động tạo ra một "trust policy" cho phép dịch vụ Lambda thực hiện hành động sts:AssumeRole.
+ Nhấn **Next**.

![createiamrole3](/images/image25.png)

4\. Add permissions (Thêm quyền):
+ Chúng ta cần hai policy được quản lý bởi AWS, sử dụng thanh tìm kiếm để tìm và chọn cả hai policy sau:
    + **AWSLambdaBasicExecutionRole**: Policy này cực kỳ quan trọng, nó cho phép Lambda tạo log streams và ghi lại các sự kiện thực thi vào **Amazon CloudWatch Logs**. Nếu không có policy này, bạn sẽ không thể gỡ lỗi hàm của mình.
    ![createiamrole5](/images/image5.png)
    + **AmazonS3FullAccess**: Policy này cung cấp toàn bộ quyền truy cập vào S3.
    ![createiamrole4](/images/image37.png)
    + Nhấn **Next**.

{{% notice tip %}}
Đối với môi trường production, bạn nên tạo một policy tùy chỉnh chỉ với các quyền cần thiết như **s3:GetObject** và **s3:PutObject** để đảm bảo an toàn
{{% /notice %}}
  


5\. **Name**, **review**, và **create**:
+ **Role name**: Đặt tên có ý nghĩa (*ví dụ: `LambdaS3ImageProcessorRole`*). 
![createiamrole5](/images/image18.png)
+ Review lại các thông tin, đảm bảo "Trusted entities" là lambda.amazonaws.com và hai policy đã được đính kèm. Nhấn **Create role**.
![createiamrole6](/images/image29.png)
 
{{% notice note %}}
Bạn đã có một IAM Role được cấu hình an toàn, sẵn sàng để Lambda sử dụng.
{{% /notice %}}
![createiamrole7](/images/image20.png)
