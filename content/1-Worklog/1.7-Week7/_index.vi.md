---
title: "Nhật ký công việc Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7:

* Tìm hiểu AWS Location Service và cơ chế Geofencing.
* Thiết kế quy trình Check-in/Check-out bằng GPS.
* Xây dựng luồng xác thực vị trí cho hệ thống Smart Attendance SaaS.
* Tích hợp AWS Location Service vào kiến trúc AWS Serverless.

### Các công việc thực hiện trong tuần:

| Ngày | Hoạt động | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Nghiên cứu AWS Location Service, các chức năng bản đồ, Geofencing và Location APIs. | 01/06/2026 | 01/06/2026 | https://000117.awsstudygroup.com/1-intro-prepare/1.3-location-service/<br><br>https://cloudjourney.awsstudygroup.com/vi/7-location-geofencing/ |
| Thứ 3 | Thiết kế quy trình Check-in/Check-out của nhân viên và xác định luồng tương tác giữa Mobile App, API Gateway, Lambda và AWS Location Service. | 02/06/2026 | 02/06/2026 | https://000079.awsstudygroup.com/vi/3-deployapp/3.2-backend/3.2.3-checkin-api/<br><br>https://000080.awsstudygroup.com/vi/3-deployapp/3.7-geofence-lambda/ |
| Thứ 4 | Thiết kế cơ chế kiểm tra vị trí hợp lệ trước khi ghi nhận dữ liệu chấm công và xác định các điều kiện Check-in thành công hoặc thất bại. | 03/06/2026 | 03/06/2026 | https://000078.awsstudygroup.com/vi/5-validation-logic/<br><br>https://000081.awsstudygroup.com/vi/6-device-location-auth/ |
| Thứ 5 | Cập nhật sơ đồ kiến trúc AWS bằng cách tích hợp AWS Location Service và rà soát toàn bộ luồng xử lý cùng các thành viên trong nhóm. | 04/06/2026 | 04/06/2026 | https://000080.awsstudygroup.com/vi/4-architecture-update/<br><br>https://cloudjourney.awsstudygroup.com/vi/7-location-geofencing/7.1-diagram/ |
| Thứ 6 | Hoàn thiện tài liệu mô tả quy trình điểm danh và cập nhật sơ đồ kiến trúc theo góp ý của mentor. | 05/06/2026 | 05/06/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/4-review/v5-location/ |

### Kết quả đạt được Tuần 7:

* Hiểu nguyên lý hoạt động của AWS Location Service và Geofencing.

* Hoàn thiện quy trình Check-in/Check-out bằng GPS.

* Thiết kế cơ chế xác thực vị trí trước khi ghi nhận dữ liệu điểm danh.

* Tích hợp AWS Location Service vào kiến trúc AWS Serverless.

* Hoàn thiện luồng xử lý điểm danh thời gian thực phục vụ hệ thống Smart Attendance SaaS.
