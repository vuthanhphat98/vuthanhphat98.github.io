---
title : "Xây dựng và Triển khai Lambda Function"
date : "2024-07-27" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---

Đây là phần cốt lõi, nơi chúng ta sẽ viết logic xử lý và triển khai nó lên môi trường serverless của AWS.

### Phân tích và Chuẩn bị Mã nguồn Python
* Hàm Lambda được kích hoạt bởi một sự kiện S3. Sự kiện này chứa thông tin về file vừa được tải lên.
* Code của chúng ta cần trích xuất tên bucket và tên file từ sự kiện đó.
* Sử dụng thư viện boto3 (AWS SDK cho Python), chúng ta sẽ tải file ảnh từ S3 vào bộ nhớ của Lambda.
* Sử dụng thư viện Pillow, chúng ta sẽ xử lý ảnh trong bộ nhớ: thay đổi kích thước.
* Cuối cùng, dùng boto3 để tải ảnh đã xử lý lên bucket output.
* Để xem mã nguồn chi tiết và giải thích từng dòng, vui lòng tham khảo tài liệu "**Mã nguồn Python Chi tiết cho Lambda**" đi kèm.

### Nội dung
- [Tạo Deployment Package](3.1-createdeployment)
- [Tạo và Cấu hình Lambda Function](3.2-createlambdafunction)
- [Cấu hình Biến Môi trường](3.3-environmentvariables)
- [Cấu hình S3 Trigger](3.4-S3trigger)