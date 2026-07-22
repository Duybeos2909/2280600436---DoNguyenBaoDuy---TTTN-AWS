---
title: "Nhật ký công việc Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4:

* Thiết kế cơ chế xác thực và phân quyền cho hệ thống Smart Attendance SaaS.
* Tìm hiểu Amazon Cognito và JWT Authentication.
* Xây dựng mô hình phân quyền theo vai trò (RBAC).
* Thiết kế mô hình Multi-Tenant cho hệ thống SaaS.

### Các công việc thực hiện trong tuần:

| Ngày | Hoạt động | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tìm hiểu Amazon Cognito User Pool và Identity Pool. Nghiên cứu cơ chế xác thực và phân quyền người dùng trong AWS. | 11/05/2026 | 11/05/2026 | https://000081.awsstudygroup.com/vi/1-introduce/1.1-cognito-overview/<br><br>https://000081.awsstudygroup.com/vi/2-prerequiste/2.1-iam-roles/ |
| Thứ 3 | Thiết kế luồng xác thực bằng Amazon Cognito kết hợp JWT Authentication và xây dựng cơ chế bảo vệ API thông qua Amazon API Gateway. | 12/05/2026 | 12/05/2026 | https://000081.awsstudygroup.com/vi/3-deploy/3.2-jwt-authorizer/<br><br>https://000079.awsstudygroup.com/vi/3-deployapp/3.2-jwt-integration/ |
| Thứ 4 | Xây dựng mô hình phân quyền theo vai trò (RBAC), bao gồm Administrator, Manager và Employee. | 13/05/2026 | 13/05/2026 | https://000081.awsstudygroup.com/vi/4-rbac/4.1-custom-claims/<br><br>https://000004.awsstudygroup.com/vi/2-prerequiste/2.1-iam-policy/ |
| Thứ 5 | Thiết kế mô hình Multi-Tenant bằng Tenant ID và nghiên cứu các phương pháp cô lập dữ liệu giữa các doanh nghiệp. | 14/05/2026 | 14/05/2026 | https://000081.awsstudygroup.com/vi/4-rbac/4.2-tenant-isolation/<br><br>https://cloudjourney.awsstudygroup.com/vi/5-multi-tenancy/ |
| Thứ 6 | Rà soát kiến trúc xác thực cùng nhóm, cập nhật sơ đồ hệ thống theo góp ý của mentor và tổng kết Tuần 4. | 15/05/2026 | 15/05/2026 | https://github.com/nganh25/smart-attendance-saas<br><br>https://cloudjourney.awsstudygroup.com/vi/4-review/v2-auth/ |

### Kết quả đạt được Tuần 4:

* Nắm được cơ chế xác thực và phân quyền bằng Amazon Cognito.

* Thiết kế thành công luồng JWT Authentication giữa Client, Amazon Cognito và Amazon API Gateway.

* Hoàn thiện mô hình phân quyền RBAC cho ba nhóm người dùng: Administrator, Manager và Employee.

* Thiết kế mô hình Multi-Tenant sử dụng Tenant ID nhằm đảm bảo khả năng mở rộng và tách biệt dữ liệu giữa các doanh nghiệp.

* Cập nhật sơ đồ kiến trúc AWS Serverless với tầng Authentication hoàn chỉnh.
