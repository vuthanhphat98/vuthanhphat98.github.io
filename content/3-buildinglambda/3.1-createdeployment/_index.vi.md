---
title : "Tạo Deployment Package"
date : "2024-07-27"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

### Tiến hành Tạo Deployment Package (.zip)

Môi trường thực thi của Lambda chỉ có sẵn AWS SDK (boto3), không có các thư viện bên thứ ba như Pillow. Do đó, chúng ta phải đóng gói chúng cùng với mã nguồn của mình.

1\. Mở **terminal** hoặc **command prompt**, di chuyển vào thư mục dự án của bạn trên máy tính (ví dụ: `lambda-image-processor`).

![DeploymentPackage](/images/image28.png)

2\. Chạy lệnh sau để cài đặt phiên bản `Pillow` tương thích với môi trường **Lambda**:

Lệnh này sẽ yêu cầu `pip` tải về một phiên bản của Pillow được build sẵn cho môi trường Amazon Linux (manylinux2014\_x86\_64) thay vì phiên bản cho máy tính của bạn.  
```
pip install --platform manylinux2014_x86_64 --target . --python-version 3.9 --only-binary=:all: Pillow
```

![DeploymentPackage](/images/image30.png)
3\. Bây giờ, trong thư mục trên có các thư mục của Pillow. Hãy tải và đưa file [lambda\_function.py](https://github.com/vuthanhphat98/Internship/blob/1bdc58ccd9772fee0e169e0047554f925458ddbc/submissions/VuThanhPhat/project-proposal/sourcecode/lambda_function.py) vào thư mục trên.

![DeploymentPackage](/images/image7.png)

4\. Nén tất cả nội dung này thành một file `deployment-package.zip`. 

![DeploymentPackage](/images/image36.png)

{{% notice tip %}}
Hãy chọn tất cả các file và thư mục *bên trong* thư mục dự án và nén chúng lại, chứ không phải nén cả thư mục lambda-image-processor. Cấu trúc file .zip phải có lambda\_function.py ở cấp gốc.
{{% /notice %}}

