---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Design the overall AWS Serverless architecture for the Smart Attendance SaaS platform.
* Design the Edge, Authentication, Backend, and Data layers.
* Understand the interaction between AWS services within the proposed architecture.
* Produce the first version of the AWS architecture diagram.

### Tasks to be carried out this week:

| Day | Activity Description | Start Date | Completion Date | Documentation |
| --- | --- | --- | --- | --- |
| Monday | Designed the initial AWS Serverless architecture for Smart Attendance SaaS and identified the main system layers together with the required AWS services. | 04/05/2026 | 04/05/2026 | https://cloudjourney.awsstudygroup.com/vi/2-architecture-design/<br><br>https://000078.awsstudygroup.com/vi/3-architecture/ |
| Tuesday | Designed the frontend architecture using Amazon Route 53, AWS WAF, Amazon CloudFront, and Amazon S3. Studied the request flow from client applications to backend services. | 05/05/2026 | 05/05/2026 | https://000117.awsstudygroup.com/7-optimization-cdn/7.1-cloudfront/<br><br>https://000117.awsstudygroup.com/1-intro-prepare/1.2-waf-setup/ |
| Wednesday | Designed the authentication architecture using Amazon Cognito and Amazon API Gateway. Planned secure API access using JWT authentication. | 06/05/2026 | 06/05/2026 | https://000081.awsstudygroup.com/vi/3-deploy/3.1-cognito-userpool/<br><br>https://000079.awsstudygroup.com/vi/3-deployapp/3.1-apigateway/ |
| Thursday | Designed the backend processing workflow using AWS Lambda and Amazon DynamoDB. Planned data interactions between business logic and the database layer. | 07/05/2026 | 07/05/2026 | https://000078.awsstudygroup.com/vi/3-deploy/3.1-lambda/<br><br>https://000080.awsstudygroup.com/vi/3-deployapp/3.1-dynamodb/ |
| Friday | Reviewed the proposed architecture with team members, updated the first version of the AWS architecture diagram based on mentor feedback, and summarized the Week 3 activities. | 08/05/2026 | 08/05/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/4-review/ |

### Week 3 Achievements:

* Completed the first version of the AWS Serverless architecture for the Smart Attendance SaaS platform.

* Successfully designed the four main architecture layers, including:

  * Edge Layer
  * Authentication Layer
  * Backend Processing Layer
  * Data Layer

* Selected and integrated the core AWS services into the architecture, including:

  * Amazon Route 53
  * AWS WAF
  * Amazon CloudFront
  * Amazon S3
  * Amazon Cognito
  * Amazon API Gateway
  * AWS Lambda
  * Amazon DynamoDB

* Designed the request flow from client applications through authentication, API Gateway, Lambda, and the database.

* Completed the first AWS architecture diagram and refined it based on discussions with team members and mentor feedback.

* Established the architectural foundation for implementing Event-Driven processing and advanced AWS services in the following internship weeks.