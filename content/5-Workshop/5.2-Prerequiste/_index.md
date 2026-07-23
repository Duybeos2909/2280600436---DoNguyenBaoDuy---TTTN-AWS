---
title : "Prerequisite"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---

#### Environment Prerequisites

Before deploying the **Smart Attendance SaaS Platform**, ensure that your local development environment or AWS Cloud9 workspace is properly configured. This workshop requires several development tools, AWS credentials, and access permissions to provision serverless resources.

The following software should be installed before continuing:

+ **AWS CLI v2** – Used to communicate with AWS services from the command line.
+ **AWS SAM CLI** – Used to build, package, test, and deploy AWS Serverless applications.
+ **Node.js (v20 or later)** and **npm** – Required for the React frontend and Lambda dependencies.
+ **Git** – Used to clone and manage the workshop source code.

Verify the installation by running:

```bash
aws --version
sam --version
node -v
npm -v
git --version
```
![CLI Tools Version Check](../../images/A1.png)

After confirming that all tools are installed correctly, you can continue with the AWS account configuration.

---

#### Create an IAM User

For security reasons, AWS recommends **never using the Root Account** for daily development activities.

Create a dedicated IAM User with administrative permissions by following these steps:

+ Sign in to the AWS Management Console.
+ Navigate to **IAM → Users**.
+ Choose **Create user**.
+ Enter a user name such as **WorkshopAdmin**.
+ (Optional) Enable AWS Management Console access.
+ Click **Next**.

Attach the required permissions:

+ Select **Attach policies directly**.
+ Search for and select **AdministratorAccess**.
+ Review the configuration.
+ Click **Create user**.

This IAM user will be used throughout the workshop to deploy AWS resources using AWS SAM.

---

#### Generate Access Keys

After creating the IAM User:

+ Open the newly created user.
+ Select the **Security credentials** tab.
+ Under **Access keys**, choose **Create access key**.
+ Select **Command Line Interface (CLI)** as the intended use.
+ Confirm the AWS recommendation.
+ (Optional) Add a description such as **Workshop AWS CLI**.
+ Click **Create access key**.

Download the generated **CSV file** immediately and store it securely.

The generated credentials include:

+ Access Key ID
+ Secret Access Key

These credentials will be used to authenticate the AWS CLI.

---

#### Configure AWS CLI

Open your terminal and execute:

```bash
aws configure
```

Provide the following information:

```text
AWS Access Key ID:
AWS Secret Access Key:
Default region:
ap-southeast-1

Default output format:
json
```

Verify that the configuration is successful by running:

```bash
aws sts get-caller-identity
```

If your **UserId**, **Account**, and **ARN** are displayed successfully, your AWS CLI has been configured correctly.

---

#### Clone the Workshop Repository

Navigate to your preferred working directory and clone the workshop source code.

```bash
cd ~/Documents/AWS

git clone https://github.com/karos2504/fcaj-workshop-template.git

cd smart-attendance-saas
```

The project structure is organized as follows:

```text
smart-attendance-saas/
│
├── backend/
│   ├── src/
│   ├── template.yaml
│   └── samconfig.toml
│
├── frontend/
│   ├── src/
│   └── package.json
│
└── platform_architecture.drawio
```

Where:

+ **backend/** contains the AWS SAM serverless application.
+ **frontend/** contains the React Single Page Application.
+ **template.yaml** defines the AWS infrastructure.
+ **samconfig.toml** stores deployment parameters.
+ **platform_architecture.drawio** contains the system architecture diagram.

---

#### Ready for Deployment

After completing all prerequisite steps, your development environment is fully prepared.

You are now ready to proceed with the next module, where the Smart Attendance SaaS backend will be deployed using **AWS SAM**, followed by configuring Amazon Cognito, Amazon API Gateway, AWS Lambda, Amazon DynamoDB, and other AWS Serverless services required by the application.