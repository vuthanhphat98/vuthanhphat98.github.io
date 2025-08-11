---
title : "Configure Environment Variables"
date : "2024-07-27"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

### Specify the Output Bucket for Lambda

This is a crucial step to fix potential `NoSuchBucket` errors. We will tell Lambda the exact name of the output bucket.

1.  In the `ImageProcessorFunction` management page, switch to the **Configuration** tab.

2.  Select **Environment variables** from the left menu, then click **Edit**.
    ![environmentvariables](/images/image1.png)

3.  Click **Add environment variable**.

4.  Enter the following information:
* **Key:** `OUTPUT_BUCKET`
* **Value:** `phat-workshop-output-images` (Replace this with the **exact** name of the output bucket you created in Step 1.2).

5.  Click **Save**.

![environmentvariables](/images/image21.png)
{{% notice note %}}
Now, your Python code can read this environment variable to know exactly where to save the thumbnail file.
{{% /notice %}}

### Important Configurations

Still in the **Configuration** tab -> **General configuration** -> **Edit**.

   ![LambdaFunction](/images/image39.png)

   * **Memory:** The default is 128MB. For image processing, increase this to **256MB** or **512MB** for better performance.
   * **Timeout:** The default is 3 seconds, which is too short for image processing. Increase it to **30 seconds**.
   * Click **Save**.

   ![LambdaFunction](/images/image26.png)