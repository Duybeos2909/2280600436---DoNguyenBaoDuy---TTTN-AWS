---
title: "Nhật ký công việc Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8:

* Tìm hiểu AWS Step Functions để điều phối Workflow.
* Thiết kế quy trình tạo báo cáo điểm danh hàng tháng.
* Tích hợp Amazon S3 và Amazon SES vào kiến trúc.
* Hoàn thiện quy trình tự động hóa báo cáo và gửi email.

### Các công việc thực hiện trong tuần:

| Ngày | Hoạt động | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Nghiên cứu AWS Step Functions và cơ chế điều phối Workflow. Tìm hiểu cách tích hợp giữa AWS Lambda và Step Functions. | 08/06/2026 | 08/06/2026 | https://000080.awsstudygroup.com/vi/3-deployapp/3.8-stepfunctions-state/<br><br>https://000078.awsstudygroup.com/vi/6-stepfunctions-integration/ |
| Thứ 3 | Thiết kế quy trình tạo báo cáo điểm danh hàng tháng và xây dựng luồng xuất báo cáo PDF, Excel. | 09/06/2026 | 09/06/2026 | https://000080.awsstudygroup.com/vi/3-deployapp/3.9-report-generator/<br><br>https://000079.awsstudygroup.com/vi/3-deployapp/3.2-backend/3.2.4-report-export/ |
| Thứ 4 | Thiết kế lưu trữ báo cáo trên Amazon S3, nghiên cứu Lifecycle Management và tổ chức dữ liệu trong Bucket. | 10/06/2026 | 10/06/2026 | https://000117.awsstudygroup.com/1-intro-prepare/1.4-s3-bucket-lifecycle/<br><br>https://000078.awsstudygroup.com/vi/7-s3-report-storage/ |
| Thứ 5 | Nghiên cứu Amazon SES và thiết kế quy trình gửi email sau khi báo cáo được tạo thành công. | 11/06/2026 | 11/06/2026 | https://000080.awsstudygroup.com/vi/3-deployapp/3.10-ses-email/<br><br>https://000081.awsstudygroup.com/vi/7-ses-identity-verify/ |
| Thứ 6 | Cập nhật kiến trúc AWS Serverless bằng cách tích hợp AWS Step Functions, Amazon S3 và Amazon SES. Rà soát toàn bộ Workflow cùng các thành viên trong nhóm. | 12/06/2026 | 12/06/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/4-review/v6-stepfunctions/ |

### Kết quả đạt được Tuần 8:

* Hiểu rõ cách hoạt động của AWS Step Functions trong việc điều phối Workflow.

* Hoàn thiện quy trình tạo báo cáo điểm danh hàng tháng.

* Thiết kế chức năng xuất báo cáo PDF và Excel.

* Tích hợp Amazon S3 để lưu trữ báo cáo và Amazon SES để gửi email tự động.

* Hoàn thiện Workflow tự động hóa cho chức năng báo cáo của Smart Attendance SaaS.
