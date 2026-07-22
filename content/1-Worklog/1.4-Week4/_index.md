---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Design the authentication architecture for the Smart Attendance SaaS platform.
* Study Amazon Cognito, JWT authentication, and Role-Based Access Control (RBAC).
* Design a secure multi-tenant authentication and authorization model.
* Update the AWS architecture based on authentication requirements.

### Tasks to be carried out this week:

| Day | Activity Description | Start Date | Completion Date | Documentation |
| --- | --- | --- | --- | --- |
| Monday | Studied Amazon Cognito User Pool and Identity Pool. Learned user authentication and authorization concepts. | 11/05/2026 | 11/05/2026 | https://000081.awsstudygroup.com/vi/1-introduce/1.1-cognito-overview/<br><br>https://000081.awsstudygroup.com/vi/2-prerequiste/2.1-iam-roles/ |
| Tuesday | Designed the authentication flow using Amazon Cognito and JWT authentication. Planned secure API access through Amazon API Gateway. | 12/05/2026 | 12/05/2026 | https://000081.awsstudygroup.com/vi/3-deploy/3.2-jwt-authorizer/<br><br>https://000079.awsstudygroup.com/vi/3-deployapp/3.2-jwt-integration/ |
| Wednesday | Defined user roles including Administrator, Manager, and Employee. Planned Role-Based Access Control (RBAC) for different system features. | 13/05/2026 | 13/05/2026 | https://000081.awsstudygroup.com/vi/4-rbac/4.1-custom-claims/<br><br>https://000004.awsstudygroup.com/vi/2-prerequiste/2.1-iam-policy/ |
| Thursday | Designed the multi-tenant access model using tenant identifiers. Studied tenant isolation strategies for shared resources. | 14/05/2026 | 14/05/2026 | https://000081.awsstudygroup.com/vi/4-rbac/4.2-tenant-isolation/<br><br>https://cloudjourney.awsstudygroup.com/vi/5-multi-tenancy/ |
| Friday | Reviewed the authentication architecture with team members. Updated the architecture diagram based on discussion and mentor feedback, then summarized the Week 4 activities. | 15/05/2026 | 15/05/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/4-review/v2-auth/ |

### Week 4 Achievements:

* Completed the authentication architecture for the Smart Attendance SaaS platform.

* Successfully designed a secure authentication flow using Amazon Cognito and JWT tokens.

* Defined the user roles within the system, including:

  * Administrator
  * Manager
  * Employee

* Designed a Role-Based Access Control (RBAC) model to control access permissions across different system functions.

* Planned a multi-tenant authentication model using tenant identifiers to ensure logical isolation between companies sharing the same infrastructure.

* Updated the AWS Serverless architecture to integrate authentication and authorization components based on mentor feedback.

* Established the security foundation for implementing backend APIs, business logic, and tenant management in the following internship weeks.