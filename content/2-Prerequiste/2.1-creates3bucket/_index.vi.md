---
title : "Tạo S3 Buckets"
date : "2024-07-27" 
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

### Tạo hai S3 Buckets
{{% notice info %}}
Chúng ta cần hai S3 buckets riêng biệt
{{% /notice %}}
Việc tách biệt này là một thông lệ tốt nhất về mặt kiến trúc: nó giúp quản lý dữ liệu rõ ràng (dữ liệu thô và dữ liệu đã xử lý) và quan trọng nhất là để ngăn chặn nguy cơ tạo ra các vòng lặp vô hạn, một rủi ro nghiêm trọng sẽ được thảo luận trong phần "Risk Assessment".

1\. Truy cập AWS Management Console và tìm đến dịch vụ **S3**.
![hinh1.1](/images/image14.png)

2\. Nhấn nút **Create bucket**.
![hinh1.2](/images/image4.png)

3\. Tạo Bucket chứa ảnh gốc (**Input Bucket**):

Bucket name: Tên bucket phải là duy nhất trên toàn cầu. Hãy tuân theo một quy ước đặt tên tốt, ví dụ: `phat-workshop-input-images`. Việc này giúp tránh xung đột tên và dễ dàng nhận diện tài nguyên của bạn.
![hinh1.3](/images/image3.png)
+ **AWS Region**: Chọn Region gần bạn nhất để giảm độ trễ khi tải file lên *(ví dụ: ap-southeast-1 - Singapore)*.
+ **Block Public Access settings for this bucket**: Luôn giữ nguyên tùy chọn Block all public access. Đây là cài đặt bảo mật quan trọng, đảm bảo rằng các file ảnh gốc của bạn không bị truy cập công khai từ internet trừ khi bạn cấp quyền một cách tường minh.
+ Nhấn **Create bucket**.
![hinh1.4](/images/image24.png)

4\. Tạo Bucket chứa ảnh kết quả (**Output Bucket**):

Lặp lại quy trình trên để tạo bucket thứ hai.
Bucket name: Đặt một cái tên khác tương tự, ví dụ: `phat-workshop-output-images`.
Giữ nguyên các cài đặt khác và nhấn Create bucket.

{{% notice note %}}
Bạn đã có 2 S3 buckets riêng biệt, được bảo mật và sẵn sàng cho việc lưu trữ.
{{% /notice %}}
![hinh1.5](/images/image6.png)



