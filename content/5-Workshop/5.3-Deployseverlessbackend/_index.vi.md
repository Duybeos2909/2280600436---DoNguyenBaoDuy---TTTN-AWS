---
title : "Deploy Serverless Backend"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Deploy Serverless Backend Infrastructure

In this module, you will build and deploy the backend infrastructure of the **Smart Attendance SaaS Platform** using **AWS Serverless Application Model (AWS SAM)**. After deployment, the backend will consist of Amazon Cognito, Amazon API Gateway, AWS Lambda, Amazon DynamoDB, and AWS Key Management Service (KMS).

---

#### 1. Review the Infrastructure Template

The **template.yaml** file defines the entire AWS infrastructure using the **Infrastructure as Code (IaC)** approach.

The template provisions the following AWS resources:

+ **Amazon Cognito User Pool** for user registration, authentication, and JWT token generation.
+ **Amazon API Gateway HTTP API** integrated with a **JWT Authorizer** for secure API access.
+ **AWS KMS Customer Managed Key (CMK)** for encrypting data stored in Amazon DynamoDB and Amazon S3.
+ **Amazon DynamoDB** using a **Single-Table Design** with **Partition Key (PK)**, **Sort Key (SK)**, **On-Demand Billing**, and **DynamoDB Streams** enabled.
+ **AWS Lambda Functions** implementing the application's business logic, including:

- AuthFunction – Handles user authentication and registration.
- CheckInFunction – Records employee check-in events.
- CheckOutFunction – Records employee check-out events.
- AttendanceHistoryFunction – Retrieves attendance history.
- AdminFunction – Manages companies and employees.
- ReportFunction – Generates attendance reports asynchronously.
- WebhookFunction – Processes payment webhooks and external events.

---

#### 2. Build the Serverless Application

Navigate to the backend directory and execute the build command:

```bash
cd backend

sam build
```

After a successful build, AWS SAM displays:

```text
Build Succeeded

Built Artifacts  : .aws