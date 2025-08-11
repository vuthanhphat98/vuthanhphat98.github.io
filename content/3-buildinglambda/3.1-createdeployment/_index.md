---
title : "Create a Deployment Package"
date : "2024-07-27"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

### Create a Deployment Package (.zip)

The Lambda execution environment only includes the AWS SDK (boto3), not third-party libraries like Pillow. Therefore, we must package them along with our source code.

1\. Open a **terminal** or **command prompt** and navigate to your project directory (e.g., `lambda-image-processor`).

![DeploymentPackage](/images/image28.png)

2\. Run the following command to install the `Pillow` version compatible with the **Lambda** environment:

This command tells `pip` to download a version of Pillow pre-built for the Amazon Linux environment (manylinux2014\_x86\_64) instead of the version for your computer.
```

pip install --platform manylinux2014\_x86\_64 --target . --python-version 3.9 --only-binary=:all: Pillow

```

![DeploymentPackage](/images/image30.png)
3\. Now, the directory contains the Pillow folders. Download the [lambda_function.py](https://github.com/vuthanhphat98/Internship/blob/1bdc58ccd9772fee0e169e0047554f925458ddbc/submissions/VuThanhPhat/project-proposal/sourcecode/lambda_function.py) file from lambda_function.py and place it into this directory.

![DeploymentPackage](/images/image7.png)

4\. Compress all of this content into a single `deployment-package.zip` file.

![DeploymentPackage](/images/image36.png)

{{% notice tip %}}
Select all the files and folders *inside* your project directory and compress them, rather than compressing the `lambda-image-processor` folder itself. The `.zip` file structure must have `lambda_function.py` at the root level.
{{% /notice %}}
