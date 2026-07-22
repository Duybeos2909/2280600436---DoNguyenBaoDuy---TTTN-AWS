---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Study Infrastructure as Code (IaC) using AWS SAM and AWS CloudFormation.
* Research CI/CD deployment pipelines for AWS Serverless applications.
* Strengthen system security using AWS IAM and AWS KMS.
* Optimize backend service interactions and complete deployment preparation.

### Tasks to be carried out this week:

| Day | Activity Description | Start Date | Completion Date | Documentation |
| --- | --- | --- | --- | --- |
| Monday | Authored AWS SAM and AWS CloudFormation templates to manage Serverless infrastructure as code. Defined resources, parameters, IAM roles, and cross-stack references. | 22/06/2026 | 22/06/2026 | https://000037.awsstudygroup.com/vi/3-cloudformationbasic/3.2-createcloudformationtemplate/<br><br>https://000080.awsstudygroup.com/vi/1-preparation/ |
| Tuesday | Configured automated CI/CD deployment pipelines using AWS CodePipeline and AWS CodeBuild for seamless build and zero-downtime Serverless deployments. | 23/06/2026 | 23/06/2026 | https://000139.awsstudygroup.com/vi/<br><br>https://000017.awsstudygroup.com/vi/5-cicd-codebuild/3-create-code-build-be/ |
| Wednesday | Implemented security hardening using AWS IAM granular roles and configured AWS KMS Customer Managed Keys (CMK) for encryption at rest on Amazon DynamoDB and Amazon S3. | 24/06/2026 | 24/06/2026 | https://000044.awsstudygroup.com/vi/1-iam-intro/<br><br>https://000002.awsstudygroup.com/vi/1-introduction/ |
| Thursday | Optimized backend service interactions across Amazon API Gateway, AWS Lambda, and Amazon DynamoDB to support high-concurrency attendance check-in workflows. | 25/06/2026 | 25/06/2026 | https://000066.awsstudygroup.com/vi/3-deployapp/3.2-backend/<br><br>https://000079.awsstudygroup.com/vi/1-introduction/ |
| Friday | Executed end-to-end integration tests, finalized deployment configurations, updated the project documentation, and summarized the Week 10 activities. | 26/06/2026 | 26/06/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://000139.awsstudygroup.com/vi/ |

### Week 10 Achievements:

* Successfully designed Infrastructure as Code (IaC) templates using AWS SAM and AWS CloudFormation for managing AWS Serverless resources.

* Studied and configured a CI/CD deployment workflow using:

  * AWS CodePipeline
  * AWS CodeBuild

* Enhanced the security architecture by implementing:

  * AWS IAM least-privilege policies
  * AWS KMS Customer Managed Keys (CMK)
  * Encryption for Amazon DynamoDB and Amazon S3

* Optimized backend interactions between Amazon API Gateway, AWS Lambda, and Amazon DynamoDB to improve system performance under concurrent attendance requests.

* Completed end-to-end integration testing to verify the interactions among core AWS services within the Smart Attendance SaaS architecture.

* Updated the project documentation and finalized the deployment preparation for the proposed AWS Serverless solution.

* Established a deployment strategy that supports automation, security, scalability, and maintainability for future implementation.