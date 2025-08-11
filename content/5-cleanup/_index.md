+++
title = "Clean up resources"
date = 2022
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

To avoid incurring unwanted costs after you're finished with this lab, be sure to clean up the resources you've created:

### Delete S3 Buckets
Go to **S3**, select each **bucket**, click **Empty** to delete all objects inside, then type `delete` and click **Delete** to delete the bucket.

![cleanup](/images/clean/image1.png)
type `permanently delete` and click **Empty** bucket.
![cleanup](/images/clean/image2.png)
enter the bucket name, in this case `phat-workshop-input-images`, and click **Delete bucket**.
![cleanup](/images/clean/image3.png)
Do the same for the remaining buckets.

### Delete Lambda Function
Go to **Lambda**, select **ImageProcessorFunction**, and delete it.
![cleanup](/images/clean/image4.png)

![cleanup](/images/clean/image5.png)

### Delete IAM Role
Go to **IAM**, find and delete `LambdaS3ImageProcessorRole`.


![cleanup](/images/clean/image6.png)
![cleanup](/images/clean/image7.png)