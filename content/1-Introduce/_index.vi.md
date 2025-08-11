---
title : "Giới thiệu"
date : "2024-07-27" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

### Giới thiệu hệ thống
Hệ thống xử lý ảnh này là một **pipeline tự động**, được xây dựng hoàn toàn trên nền tảng serverless (không máy chủ) của Amazon Web Services (AWS). Mục đích cốt lõi của nó là loại bỏ hoàn toàn công việc xử lý ảnh thủ công, lặp đi lặp lại.

Thay vì phải dùng các phần mềm đồ họa để chỉnh sửa từng ảnh, bạn chỉ cần tải ảnh gốc lên, và hệ thống sẽ tự động thực hiện các tác vụ đã được lập trình sẵn.

### Luồng hoạt động của Hệ thống
Kiến trúc của hệ thống được thiết kế theo mô hình **hướng sự kiện (event-driven)**, hoạt động theo một quy trình 3 bước đơn giản nhưng cực kỳ mạnh mẽ:

1\. **Kích hoạt (Upload)**: Người dùng hoặc một ứng dụng tải một file ảnh gốc lên một thư mục lưu trữ đặc biệt trên **Amazon S3**.

2\. **Xử lý (Process)**: Hành động tải file lên này ngay lập tức kích hoạt một hàm **AWS Lambda**. Đây là một đoạn mã Python sẽ tự động chạy mà không cần bất kỳ máy chủ nào. Đoạn mã này sẽ:

* Đọc file ảnh gốc.

* Thực hiện các thao tác xử lý, ví dụ như thay đổi kích thước để tạo ảnh thu nhỏ (thumbnail).

3\. **Lưu trữ (Save)**: Sau khi xử lý xong, hàm Lambda sẽ tự động lưu file ảnh kết quả (thumbnail) vào một thư mục lưu trữ khác trên Amazon S3.

### Các Lợi ích Chính
- **Tự động hóa 100%**: Giải phóng nhân lực khỏi các công việc nhàm chán, giúp họ tập trung vào các nhiệm vụ sáng tạo hơn.

- **Khả năng mở rộng Vô hạn**: Hệ thống có thể xử lý một ảnh hay hàng ngàn ảnh cùng lúc mà không cần bất kỳ sự can thiệp nào.

- **Tối ưu Chi phí**: Bạn chỉ trả tiền cho mỗi mili-giây mà mã xử lý chạy. Nếu không có ảnh nào được tải lên, bạn không phải trả bất kỳ chi phí nào.

- **Hiệu quả và Nhanh chóng**: Toàn bộ quá trình chỉ mất vài giây, giúp tăng tốc độ đưa nội dung và sản phẩm ra thị trường.

### Mục đích chính
cung cấp một lộ trình thực hành rõ ràng, giúp bạn chuyển từ lý thuyết sang thực tế trong việc xây dựng ứng dụng trên nền tảng đám mây AWS.

Cụ thể, bài hướng dẫn mang lại những giá trị sau:

**1\. Xây dựng Kỹ năng Thực tiễn**
* Giải quyết bài toán thực tế: Thay vì học các khái niệm trừu tượng, bạn được tự tay xây dựng một giải pháp cho một vấn đề rất phổ biến: tự động hóa việc xử lý ảnh. Đây là một kỹ năng có tính ứng dụng cao trong các dự án web và ứng dụng di động.

* Học qua hành động (Learning by Doing): Bài hướng dẫn tập trung vào các bước thực hành cụ thể, giúp bạn củng cố kiến thức và xây dựng sự tự tin khi làm việc với các dịch vụ AWS.

**2\. Nắm vững Kiến trúc Đám mây Hiện đại**
* Hiểu sâu về Serverless: Bạn sẽ trực tiếp trải nghiệm lợi ích của kiến trúc không máy chủ (serverless) – không cần quản lý hạ tầng, tự động co giãn, và tối ưu chi phí.

* Tiếp cận Tư duy Hướng sự kiện (Event-Driven): Bạn sẽ hiểu cách các dịch vụ có thể tự động kích hoạt lẫn nhau dựa trên các sự kiện (ví dụ: tải file lên S3 kích hoạt Lambda), một mô hình thiết kế rất mạnh mẽ và hiệu quả.

**3\. An toàn và Tối ưu Chi phí**
* Học tập không tốn kém: Toàn bộ bài hướng dẫn được thiết kế để nằm trong giới hạn của AWS Free Tier, cho phép bạn học hỏi và thử nghiệm mà không lo phát sinh chi phí.

* Thực hành tốt nhất về Bảo mật: Hướng dẫn nhấn mạnh việc sử dụng IAM Roles với nguyên tắc quyền tối thiểu, giúp bạn hình thành thói quen tốt về bảo mật ngay từ đầu.