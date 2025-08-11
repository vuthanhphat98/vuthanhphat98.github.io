---
title : "Create and Configure Lambda Function"
date : "2024-07-27"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

### Create the Lambda Function

1.  Return to the AWS Console, navigate to the **Lambda** service, and click **Create function**.

    ![LambdaFunction](/images/image38.png)

2.  Select **Author from scratch**.

    ![LambdaFunction](/images/image34.png)

3.  **Basic information:**
    * **Function name:** `ImageProcessorFunction`
    * **Runtime:** Select **Python 3.9** (or a newer version).
    * **Architecture:** Select **x86_64**.
    {{% notice info %}}
    arm64 (Graviton2) often offers better price/performance, but requires the deployment package to be built for the ARM architecture.
    {{% /notice %}}
    * **Permissions:** Expand "Change default execution role," select **Use an existing role**, and choose the `LambdaS3ImageProcessorRole` you created.

    ![LambdaFunction](/images/image10.png)

4.  Click **Create function**.

### Configure the Lambda Function

5.  After the function is created, in the **Code source** tab, click the **Upload from** button and select **.zip file**.

    ![LambdaFunction](/images/image27.png)

6.  Upload the `deployment-package.zip` file you just created.

    ![LambdaFunction](/images/image31.png)

    ![LambdaFunction](/images/image13.png)