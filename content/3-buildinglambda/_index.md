
---
title : "Build and Deploy a Lambda Function"
date : "2024-07-27"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

This is the core section, where we will write the processing logic and deploy it to the AWS serverless environment.

### Analysis and Preparation of Python Source Code
* The Lambda function is triggered by an S3 event. This event contains information about the file that was just uploaded.
* Our code needs to extract the bucket name and file name from that event.
* Using the boto3 library (AWS SDK for Python), we will download the image file from S3 into Lambda's memory.
* Using the Pillow library, we will process the image in memory: resizing it.
* Finally, we will use boto3 to upload the processed image to the output bucket.
* For detailed source code and line-by-line explanations, please refer to the accompanying "**Detailed Python Source Code for Lambda**" document.

### Contents
- [Create a Deployment Package](3.1-createdeployment)
- [Create and Configure a Lambda Function](3.2-createlambdafunction)
- [Configure Environment Variables](3.3-environmentvariables)
- [Configure S3 Trigger](3.4-S3trigger)