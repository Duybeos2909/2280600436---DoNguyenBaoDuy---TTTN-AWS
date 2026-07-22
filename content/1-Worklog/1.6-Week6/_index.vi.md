---
title: "Nhật ký công việc Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6:

* Thiết kế kiến trúc Event-Driven cho hệ thống.
* Tìm hiểu Amazon EventBridge, Amazon SQS và Amazon SNS.
* Xây dựng cơ chế xử lý bất đồng bộ.
* Tối ưu kiến trúc AWS Serverless.

### Các công việc thực hiện trong tuần:

| Ngày | Hoạt động | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Nghiên cứu kiến trúc Event-Driven trên AWS và các mô hình giao tiếp giữa các dịch vụ. | 25/05/2026 | 25/05/2026 | https://cloudjourney.awsstudygroup.com/vi/6-event-driven-overview/<br><br>https://000080.awsstudygroup.com/vi/1-introduce/1.2-event-driven/ |
| Thứ 3 | Thiết kế cơ chế định tuyến sự kiện bằng Amazon EventBridge và xác định các sự kiện phát sinh trong quá trình chấm công. | 26/05/2026 | 26/05/2026 | https://000066.awsstudygroup.com/vi/4-realtime-ridewaittimes/4.1-backend/4.1.1-eventbridge/<br><br>https://000080.awsstudygroup.com/vi/3-deployapp/3.4-eventbridge-rules/ |
| Thứ 4 | Tích hợp Amazon SQS vào kiến trúc để xử lý bất đồng bộ và xây dựng Dead Letter Queue (DLQ) cho các thông điệp lỗi. | 27/05/2026 | 27/05/2026 | https://000080.awsstudygroup.com/vi/3-deployapp/3.5-sqs-queues/<br><br>https://000078.awsstudygroup.com/vi/4-dlq-configuration/ |
| Thứ 5 | Thiết kế luồng gửi thông báo sử dụng Amazon SNS và đánh giá các phương thức gửi email, thông báo hệ thống. | 28/05/2026 | 28/05/2026 | https://000080.awsstudygroup.com/vi/3-deployapp/3.6-sns-topics/<br><br>https://000081.awsstudygroup.com/vi/5-notifications/ |
| Thứ 6 | Rà soát và tối ưu sơ đồ kiến trúc theo góp ý của mentor. Giảm số lượng Lambda không cần thiết và tối ưu luồng xử lý giữa các dịch vụ. | 29/05/2026 | 29/05/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/4-review/v4-eventdriven/ |

### Kết quả đạt được Tuần 6:

* Hiểu rõ kiến trúc Event-Driven trên nền tảng AWS.

* Thiết kế luồng xử lý sự kiện sử dụng Amazon EventBridge.

* Tích hợp Amazon SQS và Dead Letter Queue (DLQ) nhằm tăng khả năng xử lý lỗi và độ tin cậy của hệ thống.

* Xây dựng cơ chế gửi thông báo thông qua Amazon SNS.

* Tối ưu kiến trúc AWS Serverless bằng cách giảm số lượng Lambda Functions và cải thiện luồng xử lý giữa các dịch vụ.

* Hoàn thiện kiến trúc Event-Driven làm nền tảng cho các chức năng điểm danh thời gian thực ở các tuần tiếp theo.
