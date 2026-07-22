---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

In this section, I present the proposed architecture and implementation plan for the **Smart Attendance SaaS** project, which was designed during my internship as a **Cloud Serverless Architect**.

# Smart Attendance SaaS
## A Multi-Tenant Attendance Management System Built on AWS Serverless

---

## 1. Executive Summary

Smart Attendance SaaS is a cloud-native, multi-tenant attendance management platform designed to help organizations manage employee attendance through a fully serverless architecture on Amazon Web Services (AWS).

Employees can check in and check out using GPS location and geofencing validation, while administrators can monitor attendance records, manage employees, receive notifications, and generate monthly attendance reports.

The proposed solution emphasizes scalability, high availability, security, and cost optimization by leveraging AWS Serverless services instead of traditional virtual machine deployments.

---

## 2. Problem Statement

### What's the Problem?

Many small and medium-sized businesses still rely on manual attendance systems or traditional on-premises software that requires expensive infrastructure and continuous maintenance.

Common challenges include:

- Manual attendance recording.
- Limited support for multiple companies.
- High infrastructure maintenance costs.
- Lack of real-time notifications.
- Poor scalability.
- Difficult monitoring and reporting.

### The Solution

The proposed solution adopts a fully managed AWS Serverless architecture that eliminates server management while providing a secure and scalable SaaS platform.

The architecture follows the AWS Well-Architected Framework by emphasizing Security, Reliability, Performance Efficiency, Operational Excellence, and Cost Optimization.

The solution integrates:

- Amazon Cognito
- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- Amazon EventBridge
- Amazon SQS
- Amazon SNS
- Amazon SES
- AWS Location Service
- AWS Step Functions
- Amazon CloudWatch

### Benefits and Return on Investment

The proposed architecture provides several advantages:

- Lower operational costs through serverless computing.
- Automatic scaling according to application workload.
- High availability without server administration.
- Secure authentication using Amazon Cognito.
- Event-driven processing for higher reliability.
- Flexible multi-tenant architecture supporting future business growth.

The solution also serves as a reference architecture for organizations planning to modernize attendance management systems using AWS Serverless technologies.

---

## 3. Solution Architecture

The Smart Attendance SaaS platform adopts a fully managed AWS Serverless architecture.

Users authenticate through Amazon Cognito before accessing backend services exposed by Amazon API Gateway. Business logic is implemented using AWS Lambda functions, while attendance information is stored in Amazon DynamoDB using a pooled multi-tenant design.

Background processing is handled asynchronously through Amazon EventBridge and Amazon SQS, while Amazon SNS and Amazon SES deliver notifications and attendance reports.

Employee GPS coordinates are validated using AWS Location Service before attendance records are accepted.

The proposed architecture is illustrated below.

![Smart Attendance SaaS Architecture](/images/2-Proposal/SaaS_Serverless.jpg)

### AWS Services Used

- Amazon Route 53
- AWS WAF
- Amazon CloudFront
- Amazon S3
- Amazon Cognito
- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- Amazon EventBridge
- Amazon SQS
- Amazon SNS
- Amazon SES
- AWS Location Service
- AWS Step Functions
- Amazon CloudWatch
- AWS IAM
- AWS CloudFormation

### Component Design

**Frontend**

- React Web Application hosted on Amazon S3.
- Amazon CloudFront for global content delivery.

**Authentication**

- Amazon Cognito User Pool.
- JWT Authentication.

**Backend**

- Amazon API Gateway.
- AWS Lambda Functions.

**Database**

- Amazon DynamoDB using pooled multi-tenant architecture.

**Messaging**

- Amazon EventBridge.
- Amazon SQS.
- Amazon SNS.
- Amazon SES.

**Location Validation**

- AWS Location Service.

**Monitoring**

- Amazon CloudWatch.

---

## 4. Technical Implementation

### Implementation Phases

The project consists of four implementation phases.

**Phase 1**

- Study business requirements.
- Research AWS services.
- Design the initial AWS Serverless architecture.

**Phase 2**

- Design user authentication using Amazon Cognito.
- Design RESTful APIs.
- Build the DynamoDB data model.

**Phase 3**

- Design the Event-Driven Architecture.
- Integrate AWS Location Service.
- Design notification workflows.

**Phase 4**

- Optimize the overall architecture.
- Estimate AWS infrastructure costs.
- Complete technical documentation.
- Prepare the internship presentation and report.

### Technical Requirements

The implementation requires knowledge of:

- AWS Serverless Architecture
- Amazon Cognito
- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- Amazon EventBridge
- Amazon SQS
- Amazon SNS
- Amazon SES
- AWS Location Service
- AWS Step Functions
- Amazon CloudWatch

---

## 5. Timeline & Milestones

### Project Timeline

**Week 1**

Study AWS fundamentals and project requirements.

**Week 2**

Research AWS services.

**Week 3**

Design the initial architecture.

**Week 4**

Implement authentication using Amazon Cognito.

**Week 5**

Design backend services and database.

**Week 6**

Design Event-Driven Architecture.

**Week 7**

Integrate GPS attendance validation.

**Week 8**

Design report generation workflow.

**Week 9**

Improve architecture security and monitoring.

**Week 10**

Estimate infrastructure costs using AWS Pricing Calculator.

**Week 11**

Complete architecture documentation.

**Week 12**

Prepare final presentation and internship report.

---

## 6. Budget Estimation

The infrastructure cost was estimated using the AWS Pricing Calculator based on a small-scale deployment for demonstration and educational purposes.

### Infrastructure Costs

**AWS Services:**

Amazon Route 53: **$0.90/month** (1 Hosted Zone for Smart Attendance SaaS domain).

AWS WAF: **$8.03/month** (1 Web ACL with 3 managed security rules).

Amazon CloudFront: **$2.50/month** (Approximately 20 GB content delivery).

Amazon S3 (Frontend Hosting): **$0.35/month** (10 GB static website hosting and report storage).

Amazon Cognito: **$0.00/month** (Up to 200 Monthly Active Users within AWS Free Tier).

Amazon API Gateway (HTTP API): **$0.21/month** (Approximately 50,000 API requests).

AWS Lambda: **$0.81/month** (Approximately 300,000 invocations).

Amazon DynamoDB (On-Demand): **$0.70/month** (2 GB storage).

AWS Location Service: **$1.00/month** (GPS validation and geofencing requests).

Amazon EventBridge: **$0.05/month** (Approximately 50,000 events).

Amazon SQS: **$0.04/month** (Approximately 100,000 queue requests).

Amazon SNS: **$0.02/month** (Approximately 20,000 notifications).

Amazon SES: **$0.50/month** (Approximately 5,000 emails).

AWS Step Functions: **$0.25/month** (Approximately 10,000 state transitions).

Amazon CloudWatch Logs: **$3.80/month** (5 GB log ingestion).

CloudWatch Metrics & Alarms: **$1.00/month** (10 metrics and 5 alarms).

CloudWatch Dashboard: **$3.00/month** (1 monitoring dashboard).

AWS Shield Standard: **$0.00/month** (Included with AWS services).

AWS CloudFormation / AWS SAM: **$0.00/month** (Infrastructure as Code deployment).

---

**Estimated Total Infrastructure Cost:** **Approximately USD 23.16/month**

**Estimated Annual Cost:** **Approximately USD 277.92/year**

The estimated cost is suitable for a prototype deployment and may increase depending on the number of organizations, employees, API requests, and attendance records.

---

## 7. Risk Assessment

### Risk Matrix

- Incorrect AWS service configuration.
- GPS spoofing during attendance.
- Lambda timeout.
- SQS message failures.
- DynamoDB hot partitions.

### Mitigation Strategies

- Apply least-privilege IAM policies.
- Validate GPS using AWS Location Service.
- Configure SQS Dead Letter Queues.
- Monitor CloudWatch metrics and alarms.
- Optimize DynamoDB partition keys.

### Contingency Plans

- Enable CloudWatch alarms.
- Retry failed events through Amazon SQS.
- Restore data using DynamoDB Backup.
- Improve the architecture based on mentor feedback.

---

## 8. Expected Outcomes

### Technical Improvements

The project is expected to deliver:

- A production-ready AWS Serverless architecture.
- A secure multi-tenant SaaS platform.
- Event-driven backend processing.
- GPS-based attendance validation.
- Automated notification workflows.
- AWS cost estimation using AWS Pricing Calculator.
- Technical documentation following AWS Well-Architected best practices.

### Long-term Value

The proposed solution serves as a reference architecture for organizations adopting AWS Serverless technologies for attendance management systems while providing a strong foundation for future cloud-native SaaS applications.