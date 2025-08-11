
---
title : "Install Python"
date : "2024-07-27"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

### Install the latest Python for your device
{{% notice note %}}
If your device already has Python installed, you can skip this step.
{{% /notice %}}

To write code and package libraries for AWS Lambda, your computer needs Python and the pip package manager installed. Here are detailed instructions to check and install it. If your device already has Python installed, you can skip this step.

1\. Check the current Python version:

* Open Terminal (on macOS/Linux) or Command Prompt/PowerShell (on Windows).
* Type the following command and press Enter:
```
python3 --version
```

* If the above command doesn't work, try this one:
```
python --version

```
{{% notice info %}}
If you see a version like Python 3.8.x or later, you're ready and can proceed to Step 1.2. If you get a "command not found" error or a version lower than 3.8, you need to install Python.{{% /notice %}}


2\. Download the Python installer:

* Visit the official Python download page at [python.org/downloads](https://www.python.org/downloads/).
* The website will automatically detect your operating system and recommend the latest version. Click the download button.

![installPython](/images/image32.png)

3\. Perform the installation:

* For Windows users:
* Run the `.exe` file you just downloaded.
{{% notice warning %}}
On the first installation screen, be sure to check the box for "**Add Python to PATH**" at the bottom. This will allow you to run python and pip commands from anywhere in the Command Prompt without complex configuration.{{% /notice %}}
* Click "**Install Now**" and follow the on-screen instructions to complete.
![installPython](/images/image16.png)

* For macOS users:
* Run the `.pkg` file you just downloaded.
* Follow the on-screen instructions. The macOS installer will handle the PATH configuration for you automatically.

4\. Verify successful installation:

* Completely close your current Terminal or Command Prompt window and open a new one.
* Re-enter the version check command:
```
python3 --version

```

* If the above command doesn't work, try this one:
```
python --version

```

* This time, you should see the new Python version you just installed. This confirms that Python is successfully installed and ready to use.

![installPython](/images/image22.png)
