---
title : "Cài đặt Python"
date : "2024-07-27" 
weight : 3 
chapter : false
pre : " <b> 2.3 </b> "
---

### Cài đặt Python mới nhất cho thiết bị
{{% notice note %}}
Thiệt bị đã cài đặt python có thể bỏ qua bước này
{{% /notice %}}

Để có thể viết code và đóng gói thư viện cho AWS Lambda, máy tính của bạn cần được cài đặt Python và trình quản lý gói pip. Dưới đây là hướng dẫn chi tiết để kiểm tra và cài đặt. Nếu thiết bị của bạn đã cài đặt python, có thể bỏ qua bước này.

1\. Kiểm tra phiên bản Python hiện có:

* Mở Terminal (trên macOS/Linux) hoặc Command Prompt/PowerShell (trên Windows).  
* Gõ lệnh sau và nhấn Enter:  
  ```
  python3 \--version
  ```

* Nếu lệnh trên không hoạt động, hãy thử lệnh này:  
  ```
  python \--version
  ```
  {{% notice info %}}
Nếu bạn thấy một phiên bản như Python 3.8.x hoặc mới hơn, bạn đã sẵn sàng và có thể chuyển sang Bước 1.2. Nếu bạn nhận được thông báo lỗi "command not found" hoặc phiên bản thấp hơn 3.8, bạn cần cài đặt Python.{{% /notice %}}


2\. Tải về bộ cài đặt Python:

* Truy cập trang [python.org/downloads](https://www.python.org/downloads/) để tải về chính thức của Python.
* Trang web sẽ tự động nhận diện hệ điều hành của bạn và đề xuất phiên bản mới nhất. Hãy nhấn nút tải về.

![installPython](/images/image32.png)

3\. Thực hiện cài đặt:

* Đối với người dùng Windows:  
  * Chạy file `.exe` bạn vừa tải về.  
  {{% notice warning %}}
Ở màn hình cài đặt đầu tiên, hãy chắc chắn rằng bạn đã tick vào ô "**Add Python to PATH**" ở phía dưới cùng. Việc này sẽ cho phép bạn chạy lệnh python và pip từ bất kỳ đâu trong Command Prompt mà không cần cấu hình phức tạp.  {{% /notice %}}
  * Nhấn "**Install Now**" và làm theo các bước hướng dẫn để hoàn tất.
![installPython](/images/image16.png)

* Đối với người dùng macOS:  
  * Chạy file .pkg bạn vừa tải về.  
  * Làm theo các bước hướng dẫn trên màn hình. Bộ cài đặt cho macOS sẽ tự động xử lý việc cấu hình PATH cho bạn.

4\. Xác minh cài đặt thành công:

* Đóng hoàn toàn cửa sổ Terminal hoặc Command Prompt hiện tại và mở lại một cửa sổ mới.  
* Gõ lại lệnh kiểm tra phiên bản:  
   ```
  python3 \--version
  ```

* Nếu lệnh trên không hoạt động, hãy thử lệnh này:  
  ```
  python \--version
  ```

* Lần này, bạn sẽ thấy phiên bản Python mới mà bạn vừa cài đặt. Điều này xác nhận rằng Python đã được cài đặt thành công và sẵn sàng để sử dụng.

![installPython](/images/image22.png)