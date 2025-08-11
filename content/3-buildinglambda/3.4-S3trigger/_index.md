---
title : "Configure S3 Trigger"
date : "2024-07-27"
weight : 4
chapter : false
pre : " <b> 3.4 </b> "
---

### Create the Trigger

This is the final step to connect S3 with Lambda, completing the automated pipeline.

1.  In the `ImageProcessorFunction` management page, return to the **Code** tab.
2.  In the **Function overview** section, click **+ Add trigger**.

![S3trigger](/images/image35.png)

3.  **Trigger configuration:**
    * **Select a source:** Choose **S3**.
    * **Bucket:** Select your input bucket (`phat-workshop-input-images`).
    * **Event types:** Choose **All object create events**. This means that any action that creates a new object in the bucket (like PUT, POST, COPY) will trigger the Lambda function.
    * **Recursive invocation:** Check the box that says, "I acknowledge that using the same S3 bucket for input and output is not recommended." This is an important warning about the risk of infinite loops.

    ![S3trigger](/images/image19.png)

4.  Click **Add**.