---
title : "Theo dõi bằng Amazon CloudWatch Logs"
date : "2024-07-27" 
weight : 2 
chapter : false
pre : " <b> 4.2 </b> "
---


1\. Đi đến dịch vụ **CloudWatch** trong AWS Console.

![debug](/images/image12.png)

2\. Chọn **Log groups** từ menu bên trái.

![debug](/images/image17.png)

3\. Tìm và nhấp vào **log group** của hàm Lambda, có tên là `/aws/lambda/ImageProcessorFunction`.  
4\. Bên trong, bạn sẽ thấy các **Log streams**, mỗi stream tương ứng với một phiên bản của môi trường thực thi Lambda. Nhấp vào stream mới nhất để xem logs.  
   * **Log thành công** sẽ chứa các dòng print mà bạn đã viết, ví dụ: "Đã tạo thumbnail thành công...".

   ![debug](/images/image2.png)

   * **Log lỗi** sẽ hiển thị một "stack trace" chi tiết. Hãy đọc từ trên xuống dưới để tìm ra nguyên nhân, ví dụ như "Access Denied" (lỗi quyền IAM) hoặc "No module named 'PIL'" (lỗi đóng gói).

   ![debug](/images/image11.png)