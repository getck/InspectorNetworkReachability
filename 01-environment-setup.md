Module 1: Environment Build and Configuration
=============================================

In this first module you will be building the environment using a CloudFormation template. To start make sure you are in a region supported by Amazon Inspector (<https://docs.aws.amazon.com/inspector/latest/userguide/inspector_supported_os_regions.html>); the recommended region is *us-east-1*. Then, you must check to see if you have an EC2 Key Pair. If you do not, you must create an EC2 Key Pair for the instances to use. Instructions on how to do this are found at (<https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair>).

You are now ready to run the CloudFormation and create the environment. The CloudFormation template takes about 5 minutes to run. The instances then take about another 5 minutes to complete their software installations and get their listeners active. 

Deploy the AWS CloudFormation template
======================================

Running the CloudFormation script is easy. There are specific outputs at the end of the process to help you test and validate the instances are up and keep track of instances while looking at the Inspector Report.

Before you deploy the CloudFormation template feel free to view it [here](./resources/EnvironmentBuild.json).

1.  Make sure you are in a region that supports Amazon Inspector (<https://docs.aws.amazon.com/inspector/latest/userguide/inspector_supported_os_regions.html>)

2.  Open CloudFormation

3.  Click “Create Stack”

    1.  Select “Upload a Template File” and add the JSON file provided [here](./resources/EnvironmentBuild.json

4.  Click Next

5.  Fill out the screen as follows:

    1.  Stack Name: {Whatever name you will remember}

    2.  Availability Zone 1: Pick any availability zone

    3.  Availability Zone 2: Pick any availability zone except the first one youpicked

    4.  LatestLinuxAmiID: Leave as default. This is here to get the latestAmazon Linux 2 AMI. The demo has only been tested on this.

    5.  PassedKeyName: {Enter the EC2 Key Pair you generated in the Pre-Demo work}

![](./images/mod1-1-create-stack.png)

6.  Click “Next”

7.  Click “Next” on the following screen.

8.  **Acknowledge the CloudFormation Template creates a user by checking the box.**

    1.  **People miss this step all the time**

![](./images/mod1-2-acknowledge.png)

9.  Click “Create Stack”

While the CloudFormation stack is creating your environment, now is a good time to review the presentation material. If you're interested, go to the [Presentation Notes](presentation-notes.md) page.

If you want to skip directly to [Running the Inspector Report](02-running-inspector.md) you may do so as well.