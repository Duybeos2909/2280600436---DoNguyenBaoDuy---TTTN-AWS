---
title: "Nhật ký công việc Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9:

* Đánh giá và tối ưu kiến trúc AWS Serverless.
* Điều chỉnh vị trí các dịch vụ AWS theo góp ý của mentor.
* Tối ưu Lambda Functions, DynamoDB và Event-Driven Architecture.
* Hoàn thiện phiên bản kiến trúc AWS cuối cùng.

### Các công việc thực hiện trong tuần:

| Ngày | Hoạt động | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Rà soát toàn bộ kiến trúc AWS cùng mentor, thu thập góp ý về việc lựa chọn dịch vụ và thiết kế hệ thống. | 15/06/2026 | 15/06/2026 | https://cloudjourney.awsstudygroup.com/vi/8-architecture-review/<br><br>https://cloudjourney.awsstudygroup.com/vi/8-architecture-review/8.1-feedback/ |
| Thứ 3 | Điều chỉnh kiến trúc bằng cách cập nhật vị trí AWS WAF, tối ưu CloudFront và chuẩn hóa cách sử dụng Amazon DynamoDB trong sơ đồ kiến trúc. | 16/06/2026 | 16/06/2026 | https://000117.awsstudygroup.com/7-optimization-cdn/7.2-waf-cloudfront/<br><br>https://000079.awsstudygroup.com/vi/4-optimization/4.1-dynamodb-gsi/ |
| Thứ 4 | Tối ưu số lượng AWS Lambda Functions và cải thiện luồng tương tác giữa API Gateway, Lambda và các dịch vụ Backend. | 17/06/2026 | 17/06/2026 | https://000078.awsstudygroup.com/vi/8-lambda-consolidation/<br><br>https://000079.awsstudygroup.com/vi/4-optimization/4.2-api-throttling/ |
| Thứ 5 | Bổ sung Amazon SQS Dead Letter Queue (DLQ), rà soát quy trình xử lý sự kiện và tối ưu cơ chế Retry cho các thông điệp lỗi. | 18/06/2026 | 18/06/2026 | https://000080.awsstudygroup.com/vi/4-optimization/4.1-sqs-dlq-redrive/<br><br>https://000078.awsstudygroup.com/vi/4-dlq-configuration/4.1-retry-policy/ |
| Thứ 6 | Hoàn thiện đánh số Workflow, cập nhật các kết nối giữa các dịch vụ AWS và hoàn chỉnh phiên bản cuối của sơ đồ kiến trúc hệ thống. | 19/06/2026 | 19/06/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/8-architecture-review/8.2-final-diagram/ |

### Kết quả đạt được Tuần 9:

* Hoàn thành việc tối ưu kiến trúc AWS Serverless theo góp ý của mentor.

* Điều chỉnh vị trí AWS WAF, CloudFront và DynamoDB để phù hợp với kiến trúc chuẩn của AWS.

* Giảm số lượng AWS Lambda Functions và tối ưu luồng xử lý nghiệp vụ.

* Bổ sung Amazon SQS Dead Letter Queue (DLQ) nhằm nâng cao khả năng xử lý lỗi.

* Hoàn thiện sơ đồ kiến trúc AWS Serverless cuối cùng với đầy đủ các lớp Edge, Authentication, Backend, Data và Event-Driven.

* Sẵn sàng chuyển sang giai đoạn triển khai hạ tầng, tài liệu kỹ thuật và chuẩn bị báo cáo trong các tuần tiếp theo.
