
---
title : "Create IAM Role for Lambda"
date : "2024-07-27"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Create IAM Role

Our Lambda function needs permission to interact with other AWS services. Instead of granting permissions directly, we create a **Role** that Lambda can "assume". This adheres to the **Principle of Least Privilege**, a cornerstone of cloud security.

1\. In the AWS Console, navigate to the **IAM** (Identity and Access Management) service.
![createiamrole1](/images/image23.png)
2\. Select **Roles** from the left menu and click **Create role**.
![createiamrole2](/images/image33.png)
3\. **Select trusted entity**:
+ **Trusted entity type:** Choose **AWS service**. This means you're allowing an AWS service (in this case, Lambda) to assume this role.
+ **Use case:** Choose **Lambda**. This selection automatically creates a "trust policy" that allows the Lambda service to perform the sts:AssumeRole action.
+ Click **Next**.

![createiamrole3](/images/image25.png)

4\. Add permissions:
+ We need two AWS-managed policies. Use the search bar to find and select both policies:
    + **AWSLambdaBasicExecutionRole**: This policy is crucial. It allows Lambda to create log streams and write execution events to **Amazon CloudWatch Logs**. Without it, you won't be able to debug your function.
    ![createiamrole5](/images/image5.png)
    + **AmazonS3FullAccess**: This policy provides full access to S3.
    ![createiamrole4](/images/image37.png)
    + Click **Next**.

{{% notice tip %}}
For a production environment, you should create a custom policy with only the necessary permissions like **s3:GetObject** and **s3:PutObject** to ensure security.
{{% /notice %}}

5\. **Name**, **review**, and **create**:
+ **Role name**: Give it a meaningful name (*e.g., `LambdaS3ImageProcessorRole`*).
![createiamrole5](/images/image18.png)
+ Review the information, ensuring that the "Trusted entities" is lambda.amazonaws.com and that the two policies are attached. Click **Create role**.
![createiamrole6](/images/image29.png)

{{% notice note %}}
You now have a securely configured IAM Role ready for Lambda to use.
{{% /notice %}}
![createiamrole7](/images/image20.png)
