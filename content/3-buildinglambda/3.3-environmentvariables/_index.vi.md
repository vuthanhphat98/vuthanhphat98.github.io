---
title : "Cấu hình Biến Môi trường"
date : "2024-07-27"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

### Chỉ định bucket output cho lambda

Đây là bước quan trọng để khắc phục nếu gặp lỗi `NoSuchBucket`. Chúng ta sẽ chỉ cho Lambda biết tên chính xác của bucket output.

1\. Trong trang quản lý `ImageProcessorFunction`, chuyển sang tab **Configuration**.  

2\. Chọn **Environment variables** từ menu bên trái, sau đó nhấn **Edit**.  
   ![environmentvariables](/images/image1.png)  

3\. Nhấn **Add environment variable**.  

4\. Nhập các thông tin sau:  
* **Key:** `OUTPUT_BUCKET`  
* **Value:** `phat-workshop-output-images` (Hãy thay thế bằng tên **chính xác** của bucket output bạn đã tạo ở Bước 1.2).

5\. Nhấn **Save**.

![environmentvariables](/images/image21.png)  
{{% notice note %}}
Bây giờ, mã nguồn Python của bạn có thể đọc biến môi trường này để biết chính xác nơi lưu file thumbnail.
{{% /notice %}}

### Cấu hình quan trọng
 
Vẫn trong tab **Configuration** \-\> **General configuration** \-\> **Edit**.

   ![LambdaFunction](/images/image39.png)

   * **Memory:** Mặc định là 128MB. Đối với xử lý ảnh, hãy tăng lên **256MB** hoặc **512MB** để có hiệu năng tốt hơn.  
   * **Timeout:** Mặc định là 3 giây, quá ngắn cho việc xử lý ảnh. Tăng lên **30 giây**.  
   * Nhấn **Save**.

   ![LambdaFunction](/images/image26.png)
