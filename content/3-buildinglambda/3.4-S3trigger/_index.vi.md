---
title : "Cấu hình S3 Trigger"
date : "2024-07-27"
weight : 4
chapter : false
pre : " <b> 3.4 </b> "
---

### Tạo trigger

Đây là bước cuối cùng để kết nối S3 với Lambda, hoàn thiện pipeline tự động.

1\. Trong trang quản lý ImageProcessorFunction, quay lại tab **Code**.  
2\. Trong phần **Function overview**, nhấn **\+ Add trigger**.

![S3trigger](/images/image35.png)

3\. **Trigger configuration:**  
   * **Select a source:** Chọn **S3**.  
   * **Bucket:** Chọn bucket input của bạn (phat-workshop-input-images).  
   * **Event types:** Chọn **All object create events**. Điều này có nghĩa là bất kỳ hành động nào tạo ra một đối tượng mới trong bucket (như PUT, POST, COPY) đều sẽ kích hoạt Lambda.  
   * **Recursive invocation:** Tick vào ô xác nhận "I acknowledge that using the same S3 bucket for input and output is not recommended." Đây là một lời cảnh báo quan trọng về nguy cơ vòng lặp vô hạn.

   ![S3trigger](/images/image19.png)

4\. Nhấn **Add**.