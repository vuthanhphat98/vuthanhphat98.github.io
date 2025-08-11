
---
title : "Create S3 Buckets"
date : "2024-07-27"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

### Create two S3 Buckets
{{% notice info %}}
We need two separate S3 buckets.
{{% /notice %}}
This separation is a best practice from an architectural perspective: it helps with clear data management (raw data and processed data) and, most importantly, to prevent the risk of creating infinite loops, a serious risk that will be discussed in the "Risk Assessment" section.

1\. Access the AWS Management Console and find the **S3** service.
![hinh1.1](/images/image14.png)

2\. Click the **Create bucket** button.
![hinh1.2](/images/image4.png)

3\. Create a Bucket for original images (**Input Bucket**):

Bucket name: The bucket name must be globally unique. Follow a good naming convention, for example: `phat-workshop-input-images`. This helps to avoid name conflicts and makes it easy to identify your resources.
![hinh1.3](/images/image3.png)
+ **AWS Region**: Choose the Region closest to you to reduce latency when uploading files *(e.g., ap-southeast-1 - Singapore)*.
+ **Block Public Access settings for this bucket**: Always keep the Block all public access option. This is an important security setting that ensures your original image files are not publicly accessible from the internet unless you explicitly grant permission.
+ Click **Create bucket**.
![hinh1.4](/images/image24.png)

4\. Create a Bucket for result images (**Output Bucket**):

Repeat the above process to create a second bucket.
Bucket name: Give it a different but similar name, for example: `phat-workshop-output-images`.
Keep the other settings and click Create bucket.

{{% notice note %}}
You now have 2 separate S3 buckets, secured and ready for storage.
{{% /notice %}}
![hinh1.5](/images/image6.png)
