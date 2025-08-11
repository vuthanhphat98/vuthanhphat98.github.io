---
title : "Tạo và Cấu hình Lambda Function"
date : "2024-07-27"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

### Tiến hành tạo Lambda Function

1\. Quay lại AWS Console, tìm đến dịch vụ **Lambda** và nhấn **Create function**.

![LambdaFunction](/images/image38.png)

2\. Chọn **Author from scratch**.

![LambdaFunction](/images/image34.png)

3\. **Basic information:**  
   * **Function name:** `ImageProcessorFunction`  
   * **Runtime:** Chọn **Python 3.9** (hoặc phiên bản mới hơn).  
   * **Architecture:** Chọn **x86\_64**.  
   {{% notice info %}}
arm64 (Graviton2) thường cho hiệu năng/giá tốt hơn, nhưng đòi hỏi gói triển khai phải được build cho kiến trúc ARM.
{{% /notice %}}
   * **Permissions:** Mở rộng "Change default execution role", chọn **Use an existing role**, và chọn LambdaS3ImageProcessorRole bạn đã tạo.

   ![LambdaFunction](/images/image10.png)

4\. Nhấn **Create function**.  

### Tiến cấu hình Lambda Function

5\. Sau khi function được tạo, trong tab **Code source**, nhấn nút **Upload from** và chọn **.zip file**. 

![LambdaFunction](/images/image27.png)

6\. Tải lên file deployment-package.zip bạn vừa tạo.

![LambdaFunction](/images/image31.png)

![LambdaFunction](/images/image13.png)


