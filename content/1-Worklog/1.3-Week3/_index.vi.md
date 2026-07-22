---
title: "Nhật ký công việc Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3:

* Thiết kế kiến trúc tổng thể của hệ thống Smart Attendance SaaS.
* Xây dựng kiến trúc cho các lớp Edge, Authentication, Backend và Data.
* Hiểu luồng xử lý giữa người dùng và các dịch vụ AWS.
* Hoàn thiện phiên bản đầu tiên của sơ đồ kiến trúc AWS Serverless.

### Các công việc thực hiện trong tuần:

| Ngày | Hoạt động | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thiết kế kiến trúc AWS Serverless ban đầu cho Smart Attendance SaaS, xác định các tầng chính của hệ thống và các dịch vụ AWS sẽ sử dụng. | 04/05/2026 | 04/05/2026 | https://cloudjourney.awsstudygroup.com/vi/2-architecture-design/<br><br>https://000078.awsstudygroup.com/vi/3-architecture/ |
| Thứ 3 | Thiết kế tầng Frontend sử dụng Amazon Route 53, AWS WAF, Amazon CloudFront và Amazon S3. Nghiên cứu luồng request từ người dùng đến hệ thống Backend. | 05/05/2026 | 05/05/2026 | https://000117.awsstudygroup.com/7-optimization-cdn/7.1-cloudfront/<br><br>https://000117.awsstudygroup.com/1-intro-prepare/1.2-waf-setup/ |
| Thứ 4 | Thiết kế kiến trúc xác thực sử dụng Amazon Cognito và Amazon API Gateway. Lập kế hoạch bảo vệ API bằng cơ chế JWT Authentication. | 06/05/2026 | 06/05/2026 | https://000081.awsstudygroup.com/vi/3-deploy/3.1-cognito-userpool/<br><br>https://000079.awsstudygroup.com/vi/3-deployapp/3.1-apigateway/ |
| Thứ 5 | Thiết kế luồng xử lý Backend sử dụng AWS Lambda và Amazon DynamoDB. Xây dựng luồng tương tác giữa tầng xử lý nghiệp vụ và cơ sở dữ liệu. | 07/05/2026 | 07/05/2026 | https://000078.awsstudygroup.com/vi/3-deploy/3.1-lambda/<br><br>https://000080.awsstudygroup.com/vi/3-deployapp/3.1-dynamodb/ |
| Thứ 6 | Rà soát kiến trúc cùng các thành viên trong nhóm, cập nhật phiên bản đầu tiên của sơ đồ kiến trúc AWS dựa trên các góp ý và tổng kết Tuần 3. | 08/05/2026 | 08/05/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/4-review/ |

### Kết quả đạt được Tuần 3:

* Hoàn thành thiết kế phiên bản đầu tiên của kiến trúc AWS Serverless cho hệ thống Smart Attendance SaaS.

* Xây dựng kiến trúc cho các tầng chính của hệ thống gồm:

  * Edge Layer
  * Authentication Layer
  * Backend Layer
  * Data Layer

* Thiết kế luồng xử lý từ người dùng đến hệ thống Backend thông qua Amazon Route 53, AWS WAF, Amazon CloudFront, Amazon S3, Amazon Cognito và Amazon API Gateway.

* Xây dựng luồng xử lý nghiệp vụ sử dụng AWS Lambda kết hợp Amazon DynamoDB.

* Hoàn thành phiên bản đầu tiên của sơ đồ kiến trúc AWS Serverless và cập nhật theo các góp ý từ mentor và các thành viên trong nhóm.

* Tạo nền tảng cho việc triển khai các chức năng xác thực, xử lý nghiệp vụ và Event-Driven Architecture trong các tuần tiếp theo.
