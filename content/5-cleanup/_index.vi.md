+++
title = "Dọn dẹp tài nguyên"
date = 2022
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

Để tránh phát sinh chi phí không mong muốn sau khi thực hành xong, hãy dọn dẹp các tài nguyên đã tạo:

### Xóa S3 Buckets
Vào **S3**, chọn từng **bucket**, nhấn **Empty** để xóa hết các đối tượng bên trong, sau đó nhập `delete` và nhấn **Delete** để xóa bucket.

![cleanup](/images/clean/image1.png)
nhập `permanently delete` và nhấn **Empty** bucket.
![cleanup](/images/clean/image2.png)
nhập tên bucket, trường hợp này là `phat-workshop-input-images` và nhấn **Delete bucket**.
![cleanup](/images/clean/image3.png)
Tương tự với các bucket còn lại.

### Xóa Lambda Function
Vào **Lambda**, chọn **ImageProcessorFunction** và xóa nó.
![cleanup](/images/clean/image4.png)

![cleanup](/images/clean/image5.png)

### Xóa IAM Role
Vào **IAM**, tìm và xóa `LambdaS3ImageProcessorRole`.


![cleanup](/images/clean/image6.png)
![cleanup](/images/clean/image7.png)

