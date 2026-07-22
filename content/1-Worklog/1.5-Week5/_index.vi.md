---
title: "Nhật ký công việc Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5:

* Thiết kế hệ thống API cho Smart Attendance SaaS.
* Xây dựng kiến trúc Backend sử dụng AWS Lambda.
* Thiết kế mô hình dữ liệu DynamoDB Single-Table.
* Hoàn thiện luồng xử lý nghiệp vụ của hệ thống.

### Các công việc thực hiện trong tuần:

| Ngày | Hoạt động | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thiết kế RESTful API bằng Amazon API Gateway cho các chức năng xác thực, chấm công, quản lý nhân viên và báo cáo. | 18/05/2026 | 18/05/2026 | https://000079.awsstudygroup.com/vi/3-deployapp/3.2-backend/3.2.1-api-routes/<br><br>https://000079.awsstudygroup.com/vi/3-deployapp/3.2-backend/3.2.2-cors-config/ |
| Thứ 3 | Thiết kế các AWS Lambda Functions và xác định trách nhiệm của từng hàm xử lý nghiệp vụ. | 19/05/2026 | 19/05/2026 | https://000078.awsstudygroup.com/vi/3-deploy/3.2-lambda-handlers/<br><br>https://000080.awsstudygroup.com/vi/3-deployapp/3.2-function-layer/ |
| Thứ 4 | Thiết kế mô hình dữ liệu Amazon DynamoDB Single-Table, xác định Partition Key, Sort Key và các mẫu truy vấn dữ liệu. | 20/05/2026 | 20/05/2026 | https://000079.awsstudygroup.com/vi/3-deployapp/3.1-dynamodb-singletable/<br><br>https://000078.awsstudygroup.com/vi/3-deploy/3.3-dynamodb-keys/ |
| Thứ 5 | Rà soát luồng xử lý giữa Amazon API Gateway, AWS Lambda và Amazon DynamoDB. Cập nhật sơ đồ kiến trúc Backend. | 21/05/2026 | 21/05/2026 | https://000080.awsstudygroup.com/vi/3-deployapp/3.3-api-integration/<br><br>https://000066.awsstudygroup.com/vi/3-deployapp/3.2-backend/ |
| Thứ 6 | Thảo luận kiến trúc Backend với nhóm và tiếp nhận góp ý từ mentor để hoàn thiện thiết kế. | 22/05/2026 | 22/05/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/4-review/v3-backend/ |

### Kết quả đạt được Tuần 5:

* Hoàn thành thiết kế hệ thống RESTful API cho Smart Attendance SaaS.

* Thiết kế các AWS Lambda Functions phục vụ xử lý nghiệp vụ.

* Xây dựng mô hình dữ liệu Amazon DynamoDB Single-Table tối ưu cho hệ thống SaaS đa tenant.

* Hoàn thiện luồng xử lý Backend giữa Amazon API Gateway, AWS Lambda và Amazon DynamoDB.

* Cập nhật sơ đồ kiến trúc Backend theo góp ý của mentor và các thành viên trong nhóm.
