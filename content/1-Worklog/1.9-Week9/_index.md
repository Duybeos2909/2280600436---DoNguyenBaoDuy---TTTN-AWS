---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Review the complete AWS Serverless architecture with mentors.
* Refine AWS WAF, Amazon CloudFront, Amazon DynamoDB, and AWS Lambda usage.
* Improve asynchronous processing by completing the Amazon SQS Dead Letter Queue design.
* Finalize the revised AWS architecture diagram and workflow documentation.

### Tasks to be carried out this week:

| Day | Activity Description | Start Date | Completion Date | Documentation |
| --- | --- | --- | --- | --- |
| Monday | Reviewed the AWS Serverless architecture with mentors. Collected feedback regarding service selection, security placement, system complexity, and the overall design of Smart Attendance SaaS. | 15/06/2026 | 15/06/2026 | https://cloudjourney.awsstudygroup.com/vi/8-architecture-review/<br><br>https://cloudjourney.awsstudygroup.com/vi/8-architecture-review/8.1-feedback/ |
| Tuesday | Updated the architecture by repositioning AWS WAF, refining the Amazon CloudFront integration, and reviewing the use of Amazon DynamoDB. Corrected the representation of DynamoDB Tables in the architecture diagram. | 16/06/2026 | 16/06/2026 | https://000117.awsstudygroup.com/7-optimization-cdn/7.2-waf-cloudfront/<br><br>https://000079.awsstudygroup.com/vi/4-optimization/4.1-dynamodb-gsi/ |
| Wednesday | Optimized the number of AWS Lambda functions by consolidating related business logic. Improved the interactions between Amazon API Gateway, AWS Lambda, Amazon DynamoDB, and other backend services. | 17/06/2026 | 17/06/2026 | https://000078.awsstudygroup.com/vi/8-lambda-consolidation/<br><br>https://000079.awsstudygroup.com/vi/4-optimization/4.2-api-throttling/ |
| Thursday | Added an Amazon SQS Dead Letter Queue to handle failed messages. Reviewed retry policies, event processing, and messaging workflows within the Event-Driven Architecture. | 18/06/2026 | 18/06/2026 | https://000080.awsstudygroup.com/vi/4-optimization/4.1-sqs-dlq-redrive/<br><br>https://000078.awsstudygroup.com/vi/4-dlq-configuration/4.1-retry-policy/ |
| Friday | Updated workflow numbering, service connections, arrow directions, and architecture documentation. Completed the revised AWS Serverless architecture diagram and summarized the Week 9 activities. | 19/06/2026 | 19/06/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/8-architecture-review/8.2-final-diagram/ |

### Week 9 Achievements:

* Completed a comprehensive review of the Smart Attendance SaaS architecture with mentors.

* Improved the edge and security layer by correcting the placement and integration of:

  * AWS WAF
  * Amazon CloudFront
  * Amazon Route 53
  * Amazon S3

* Reviewed the Amazon DynamoDB design and corrected the representation of DynamoDB Tables in the architecture diagram.

* Reduced unnecessary AWS Lambda functions by consolidating related business logic and simplifying backend interactions.

* Improved communication between Amazon API Gateway, AWS Lambda, Amazon DynamoDB, and event-driven services.

* Completed the Amazon SQS Dead Letter Queue design, including retry and failed-message handling strategies.

* Updated workflow numbering, connection directions, and service descriptions across the architecture diagram.

* Completed the revised AWS Serverless architecture diagram as the foundation for cost estimation and final technical documentation in the following internship weeks.