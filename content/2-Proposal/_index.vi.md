---
title: "Bản đề xuất"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

Trong phần này, tôi trình bày đề xuất kiến trúc hệ thống và kế hoạch triển khai cho dự án **Smart Attendance SaaS**, được thiết kế trong quá trình thực tập với vai trò **Cloud Serverless Architect**.

# Smart Attendance SaaS
## Hệ thống quản lý chấm công đa Tenant trên nền tảng AWS Serverless

---

## 1. Tổng quan dự án

Smart Attendance SaaS là nền tảng quản lý chấm công đa tenant được xây dựng theo mô hình Cloud Native trên Amazon Web Services (AWS) với kiến trúc Serverless.

Hệ thống cho phép nhân viên thực hiện Check-in và Check-out thông qua GPS kết hợp Geofencing, đồng thời hỗ trợ quản trị viên theo dõi dữ liệu chấm công, quản lý nhân viên, nhận thông báo và tạo báo cáo chấm công theo tháng.

Giải pháp được đề xuất tập trung vào khả năng mở rộng, tính sẵn sàng cao, bảo mật và tối ưu chi phí bằng cách sử dụng các dịch vụ AWS Serverless thay cho mô hình triển khai máy chủ truyền thống.

---

## 2. Bài toán đặt ra

### Vấn đề cần giải quyết

Hiện nay nhiều doanh nghiệp vừa và nhỏ vẫn sử dụng hình thức chấm công thủ công hoặc các hệ thống triển khai tại chỗ (On-Premises), dẫn đến chi phí vận hành cao và khó mở rộng.

Một số hạn chế phổ biến gồm:

- Chấm công thủ công.
- Khó quản lý nhiều công ty trên cùng một hệ thống.
- Chi phí bảo trì hạ tầng lớn.
- Không hỗ trợ thông báo theo thời gian thực.
- Khả năng mở rộng hạn chế.
- Khó giám sát và thống kê dữ liệu.

### Giải pháp đề xuất

Giải pháp đề xuất sử dụng kiến trúc AWS Serverless hoàn toàn, giúp loại bỏ việc quản lý máy chủ nhưng vẫn đảm bảo tính bảo mật, khả năng mở rộng và đáp ứng mô hình SaaS.

Kiến trúc được xây dựng theo các nguyên tắc của **AWS Well-Architected Framework**, tập trung vào:

- Security (Bảo mật)
- Reliability (Độ tin cậy)
- Performance Efficiency (Hiệu năng)
- Operational Excellence (Vận hành)
- Cost Optimization (Tối ưu chi phí)

Hệ thống sử dụng các dịch vụ:

- Amazon Cognito
- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- Amazon EventBridge
- Amazon SQS
- Amazon SNS
- Amazon SES
- AWS Location Service
- AWS Step Functions
- Amazon CloudWatch

### Lợi ích mang lại

Giải pháp mang lại nhiều lợi ích như:

- Giảm chi phí vận hành nhờ kiến trúc Serverless.
- Tự động mở rộng theo lưu lượng sử dụng.
- Đảm bảo tính sẵn sàng cao.
- Xác thực người dùng an toàn bằng Amazon Cognito.
- Xử lý bất đồng bộ thông qua kiến trúc Event-Driven.
- Hỗ trợ mô hình Multi-Tenant dễ dàng mở rộng trong tương lai.

Ngoài ra, kiến trúc còn đóng vai trò là mô hình tham khảo cho các doanh nghiệp mong muốn hiện đại hóa hệ thống chấm công trên nền tảng AWS.

---

## 3. Kiến trúc giải pháp

Smart Attendance SaaS được xây dựng theo kiến trúc AWS Serverless hoàn toàn.

Người dùng xác thực thông qua Amazon Cognito trước khi truy cập các dịch vụ Backend được cung cấp bởi Amazon API Gateway.

Toàn bộ nghiệp vụ được xử lý bởi AWS Lambda, trong khi dữ liệu chấm công được lưu trên Amazon DynamoDB theo mô hình Pooled Multi-Tenant.

Các tác vụ xử lý nền được thực hiện thông qua Amazon EventBridge và Amazon SQS, đồng thời Amazon SNS và Amazon SES được sử dụng để gửi thông báo và báo cáo.

Thông tin vị trí GPS của nhân viên được kiểm tra bằng AWS Location Service trước khi chấp nhận bản ghi chấm công.

Sơ đồ kiến trúc được minh họa bên dưới.

![Smart Attendance SaaS Architecture](/images/2-Proposal/SaaS_Serverless.jpg)

### Các dịch vụ AWS sử dụng

- Amazon Route 53
- AWS WAF
- Amazon CloudFront
- Amazon S3
- Amazon Cognito
- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- Amazon EventBridge
- Amazon SQS
- Amazon SNS
- Amazon SES
- AWS Location Service
- AWS Step Functions
- Amazon CloudWatch
- AWS IAM
- AWS CloudFormation

### Thiết kế các thành phần

**Frontend**

- Ứng dụng React được lưu trữ trên Amazon S3.
- Amazon CloudFront phân phối nội dung.

**Xác thực**

- Amazon Cognito User Pool.
- Xác thực bằng JWT.

**Backend**

- Amazon API Gateway.
- AWS Lambda.

**Cơ sở dữ liệu**

- Amazon DynamoDB theo mô hình Pooled Multi-Tenant.

**Hệ thống nhắn tin**

- Amazon EventBridge.
- Amazon SQS.
- Amazon SNS.
- Amazon SES.

**Kiểm tra vị trí**

- AWS Location Service.

**Giám sát**

- Amazon CloudWatch.

---

## 4. Kế hoạch triển khai

### Các giai đoạn thực hiện

Dự án được chia thành bốn giai đoạn.

**Giai đoạn 1**

- Nghiên cứu yêu cầu nghiệp vụ.
- Tìm hiểu các dịch vụ AWS.
- Thiết kế kiến trúc Serverless ban đầu.

**Giai đoạn 2**

- Thiết kế xác thực bằng Amazon Cognito.
- Thiết kế RESTful API.
- Xây dựng mô hình dữ liệu DynamoDB.

**Giai đoạn 3**

- Thiết kế kiến trúc Event-Driven.
- Tích hợp AWS Location Service.
- Thiết kế quy trình gửi thông báo.

**Giai đoạn 4**

- Tối ưu kiến trúc tổng thể.
- Ước tính chi phí triển khai.
- Hoàn thiện tài liệu kỹ thuật.
- Chuẩn bị báo cáo và thuyết trình.

### Yêu cầu kỹ thuật

Dự án yêu cầu kiến thức về:

- AWS Serverless Architecture
- Amazon Cognito
- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- Amazon EventBridge
- Amazon SQS
- Amazon SNS
- Amazon SES
- AWS Location Service
- AWS Step Functions
- Amazon CloudWatch

---

## 5. Tiến độ thực hiện

### Kế hoạch theo từng tuần

**Tuần 1**

Tìm hiểu AWS Cloud và yêu cầu dự án.

**Tuần 2**

Nghiên cứu các dịch vụ AWS.

**Tuần 3**

Thiết kế kiến trúc ban đầu.

**Tuần 4**

Thiết kế xác thực bằng Amazon Cognito.

**Tuần 5**

Thiết kế Backend và cơ sở dữ liệu.

**Tuần 6**

Thiết kế kiến trúc Event-Driven.

**Tuần 7**

Tích hợp chức năng xác thực vị trí GPS.

**Tuần 8**

Thiết kế quy trình tạo báo cáo.

**Tuần 9**

Tăng cường bảo mật và giám sát hệ thống.

**Tuần 10**

Ước tính chi phí bằng AWS Pricing Calculator.

**Tuần 11**

Hoàn thiện sơ đồ kiến trúc và tài liệu kỹ thuật.

**Tuần 12**

Hoàn thiện báo cáo và chuẩn bị bảo vệ.

---

## 6. Ước tính chi phí

Chi phí hạ tầng được ước tính bằng AWS Pricing Calculator với quy mô triển khai nhỏ phục vụ mục đích học tập và trình diễn.

### Chi phí các dịch vụ

- Amazon Route 53: **0.90 USD/tháng**
- AWS WAF: **8.03 USD/tháng**
- Amazon CloudFront: **2.50 USD/tháng**
- Amazon S3: **0.35 USD/tháng**
- Amazon Cognito: **0.00 USD/tháng**
- Amazon API Gateway: **0.21 USD/tháng**
- AWS Lambda: **0.81 USD/tháng**
- Amazon DynamoDB: **0.70 USD/tháng**
- AWS Location Service: **1.00 USD/tháng**
- Amazon EventBridge: **0.05 USD/tháng**
- Amazon SQS: **0.04 USD/tháng**
- Amazon SNS: **0.02 USD/tháng**
- Amazon SES: **0.50 USD/tháng**
- AWS Step Functions: **0.25 USD/tháng**
- Amazon CloudWatch Logs: **3.80 USD/tháng**
- CloudWatch Metrics & Alarms: **1.00 USD/tháng**
- CloudWatch Dashboard: **3.00 USD/tháng**
- AWS Shield Standard: **0.00 USD/tháng**
- AWS CloudFormation / AWS SAM: **0.00 USD/tháng**

---

**Tổng chi phí ước tính:** **Khoảng 23.16 USD/tháng**

**Chi phí ước tính mỗi năm:** **Khoảng 277.92 USD/năm**

Mức chi phí này phù hợp với một hệ thống thử nghiệm (Prototype) và có thể tăng khi số lượng doanh nghiệp, nhân viên hoặc lưu lượng sử dụng hệ thống tăng lên.

---

## 7. Đánh giá rủi ro

### Các rủi ro

- Cấu hình sai dịch vụ AWS.
- Giả mạo vị trí GPS khi chấm công.
- AWS Lambda vượt thời gian thực thi.
- Lỗi hàng đợi Amazon SQS.
- Phân vùng nóng (Hot Partition) trên DynamoDB.

### Biện pháp giảm thiểu

- Áp dụng nguyên tắc IAM Least Privilege.
- Kiểm tra vị trí bằng AWS Location Service.
- Sử dụng Dead Letter Queue cho Amazon SQS.
- Theo dõi CloudWatch Metrics và Alarms.
- Tối ưu Partition Key của DynamoDB.

### Kế hoạch dự phòng

- Thiết lập CloudWatch Alarm.
- Thực hiện Retry thông qua Amazon SQS.
- Khôi phục dữ liệu bằng DynamoDB Backup.
- Điều chỉnh kiến trúc dựa trên phản hồi của Mentor.

---

## 8. Kết quả mong đợi

### Kết quả kỹ thuật

Dự án hướng tới các kết quả sau:

- Kiến trúc AWS Serverless hoàn chỉnh.
- Hệ thống SaaS đa tenant an toàn.
- Kiến trúc Event-Driven.
- Chức năng xác thực vị trí GPS.
- Quy trình gửi thông báo tự động.
- Ước tính chi phí bằng AWS Pricing Calculator.
- Tài liệu kỹ thuật theo AWS Well-Architected Framework.

### Giá trị lâu dài

Giải pháp là mô hình tham khảo cho các doanh nghiệp muốn triển khai hệ thống chấm công trên nền tảng AWS Serverless, đồng thời tạo nền tảng để phát triển các ứng dụng SaaS Cloud-Native trong tương lai.