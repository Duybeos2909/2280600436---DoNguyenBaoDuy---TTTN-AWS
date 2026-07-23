---
title : "Deploy Serverless Backend"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Deploy Serverless Backend Infrastructure

In this module, you will package and deploy the complete **Serverless Backend Infrastructure** of the **Smart Attendance SaaS Platform** using **AWS Serverless Application Model (AWS SAM)**.

The deployment includes:

+ Amazon Cognito User Pool
+ Amazon API Gateway HTTP API
+ AWS Lambda microservices
+ Amazon DynamoDB Single-Table Design
+ AWS KMS Customer Managed Key
+ DynamoDB Streams
+ Supporting IAM roles and policies

---

#### 1. Inspect Infrastructure Code (`template.yaml`)

The **template.yaml** file defines the complete AWS infrastructure declaratively using the **Infrastructure as Code (IaC)** approach.

The main resources include:

+ **Amazon Cognito User Pool (`CognitoUserPool`)**  
  Manages user registration, authentication, and JWT token generation. Custom attributes such as `tenantId` and `role` are used to support multi-tenant authentication and authorization.

+ **Amazon API Gateway HTTP API (`AttendanceApi`)**  
  Exposes the backend API endpoints and uses a Cognito-based JWT Authorizer to validate authenticated requests.

+ **AWS KMS Key (`DataKMSKey`)**  
  Provides a Customer Managed Key for encrypting data at rest in Amazon DynamoDB and Amazon S3.

+ **Amazon DynamoDB Table (`SaaSAttendanceTable`)**  
  Uses a Single-Table Design with `PK` as the Partition Key and `SK` as the Sort Key. The table uses On-Demand billing and has DynamoDB Streams enabled.

+ **AWS Lambda Microservices**  
  Implement the core business logic of the Smart Attendance SaaS Platform.

The Lambda functions include:

- **AuthFunction** – Handles registration, login, and token exchange through `/auth/*`.
- **CheckInFunction** – Records employee check-in events through `/attendance/check-in`.
- **CheckOutFunction** – Records employee check-out events through `/attendance/check-out`.
- **AttendanceHistoryFunction** – Retrieves attendance records through `/attendance/history`.
- **AdminFunction** – Handles employee management, tenant administration, and company metrics through `/admin/*`.
- **ReportFunction** – Receives and processes asynchronous report generation requests.
- **WebhookFunction** – Processes external payment webhooks and system notifications.

---

#### 2. Build Infrastructure Artifacts

Navigate to the backend directory:

```bash
cd backend
```

Build the serverless application:

```bash
sam build
```

After the build completes successfully, AWS SAM displays output similar to:

```text
Build Succeeded

Built Artifacts  : .aws-sam/build
Built Template   : .aws-sam/build/template.yaml
```

![AWS SAM Build Result](../../images/A2.png)

The generated deployment artifacts are stored in:

```text
.aws-sam/build
```

The generated SAM template is located at:

```text
.aws-sam/build/template.yaml
```

These artifacts will be used by AWS SAM during the deployment process.

---

#### 3. Deploy the Cloud Infrastructure

Run the guided deployment command:

```bash
sam deploy --guided
```

During the first deployment, AWS SAM asks for configuration parameters.

Provide values similar to the following:

```text
Configuring SAM deploy
======================

Stack Name [sam-app]: smart-attendance-backend
AWS Region [us-east-1]: ap-southeast-1
Parameter AllowedOrigin [https://your-cloudfront-domain.cloudfront.net]: https://localhost:3000
Parameter OriginVerifySecret [SaaS-Secure-Verification-Token-2026]: SaaS-Secure-Verification-Token-2026
Confirm changes before deploy [Y/n]: n
Allow SAM CLI IAM role creation [Y/n]: Y
Disable rollback [y/N]: N
Save arguments to configuration file [Y/n]: Y
SAM configuration file [samconfig.toml]: samconfig.toml
SAM configuration environment [default]: default
```

AWS SAM uses AWS CloudFormation to create or update all resources defined in `template.yaml`.

The deployment process may take approximately **2–5 minutes**, depending on the number of resources and the current AWS service provisioning time.

After deployment completes successfully, the terminal displays the CloudFormation resource status and stack output values.

![AWS SAM Deployment Result](../../images/A3.png)

A successful deployment message appears similar to:

```text
Successfully created/updated stack
```

---

#### Troubleshooting: S3 Bucket Does Not Exist

During deployment, you may encounter the following error:

```text
S3 Bucket does not exist
```

This problem can occur when the AWS SAM managed CloudFormation stack still exists, but the underlying deployment S3 bucket was deleted manually.

Delete the existing managed stack:

```bash
aws cloudformation delete-stack \
  --stack-name aws-sam-cli-managed-default \
  --region ap-southeast-1
```

Wait until the stack is deleted successfully.

You can verify its status using:

```bash
aws cloudformation describe-stacks \
  --stack-name aws-sam-cli-managed-default \
  --region ap-southeast-1
```

After the old stack has been removed, run the guided deployment again:

```bash
sam deploy --guided
```

AWS SAM will automatically create a new deployment bucket and continue provisioning the backend infrastructure.

---

#### 4. Capture Stack Outputs

After deployment completes successfully, AWS SAM displays the CloudFormation stack outputs.

Example:

```text
Key                 AttendanceApiUrl
Description         API Endpoint URL
Value               https://xxxxxxx.execute-api.ap-southeast-1.amazonaws.com/prod
```

```text
Key                 CognitoUserPoolId
Description         Cognito User Pool ID
Value               ap-southeast-1_xxxxxxxxx
```

```text
Key                 CognitoUserPoolClientId
Description         Cognito App Client ID
Value               xxxxxxxxxxxxxxxxxxxxxxxxxx
```

Save the following values:

+ **AttendanceApiUrl**
+ **CognitoUserPoolId**
+ **CognitoUserPoolClientId**

These values will be used later to configure the production environment variables of the React SPA frontend.

Example `.env.production` configuration:

```env
VITE_API_BASE_URL=https://xxxxxxx.execute-api.ap-southeast-1.amazonaws.com/prod
VITE_COGNITO_USER_POOL_ID=ap-southeast-1_xxxxxxxxx
VITE_COGNITO_CLIENT_ID=xxxxxxxxxxxxxxxxxxxxxxxxxx
VITE_AWS_REGION=ap-southeast-1
```

---

#### Module Summary

After completing this module, you have:

+ Reviewed the AWS SAM infrastructure template.
+ Identified the main backend AWS resources.
+ Built the Serverless application with `sam build`.
+ Deployed the backend infrastructure using `sam deploy --guided`.
+ Provisioned AWS Lambda, Amazon Cognito, Amazon API Gateway, Amazon DynamoDB, and AWS KMS resources.
+ Captured the API and Cognito output values for frontend integration.

The Smart Attendance SaaS backend is now deployed and ready for database validation, event-driven processing, and frontend integration.