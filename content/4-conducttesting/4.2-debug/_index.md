---
title : "Monitoring with Amazon CloudWatch Logs"
date : "2024-07-27" 
weight : 2 
chapter : false
pre : " <b> 4.2 </b> "
---


1. Navigate to the **CloudWatch** service in the AWS Console.

![debug](/images/image12.png)

2. Select **Log groups** from the left menu.

![debug](/images/image17.png)

3. Find and click on the **log group** for the Lambda function, named `/aws/lambda/ImageProcessorFunction`.  
4. Inside, you will see **Log streams**, with each stream corresponding to an instance of the Lambda execution environment. Click on the latest stream to view the logs.  
   * A **successful log** will contain the print statements you wrote, for example: "Successfully created thumbnail...".

   ![debug](/images/image2.png)

   * An **error log** will show a detailed "stack trace". Read from top to bottom to find the cause, such as "Access Denied" (an IAM permission error) or "No module named 'PIL'" (a packaging error).

   ![debug](/images/image11.png)