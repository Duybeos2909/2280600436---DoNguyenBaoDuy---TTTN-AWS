---
title : "Deploy Serverless Backend"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

#### Triển khai Backend Serverless bằng AWS SAM

Trong phần này, bạn sẽ xây dựng và triển khai toàn bộ hạ tầng Backend của hệ thống **Smart Attendance SaaS** bằng **AWS Serverless Application Model (AWS SAM)**. Sau khi hoàn thành, hệ thống sẽ bao gồm các thành phần như **Amazon Cognito**, **Amazon API Gateway**, **AWS Lambda**, **Amazon DynamoDB** và **AWS KMS**.

---

#### 1. Kiểm tra tệp hạ tầng (template.yaml)

Tệp **template.yaml** là nơi định nghĩa toàn bộ hạ tầng AWS theo mô hình **Infrastructure as Code (IaC)**.

Các thành phần chính bao gồm:

+ **Amazon Cognito User Pool** dùng để quản lý đăng ký, đăng nhập và cấp JWT Token cho người dùng.
+ **Amazon API Gateway HTTP API** cung cấp các API REST và tích hợp **JWT Authorizer** để xác thực người dùng.
+ **AWS KMS Customer Managed Key (CMK)** dùng để mã hóa dữ liệu lưu trữ trên DynamoDB và Amazon S3.
+ **Amazon DynamoDB** được thiết kế theo mô hình **Single-Table Design**, sử dụng khóa phân vùng (PK), khóa sắp xếp (SK), chế độ **On-Demand Billing** và bật **DynamoDB Streams**.
+ **AWS Lambda Functions** xử lý toàn bộ nghiệp vụ của hệ thống, bao gồm:

- AuthFunction – Xử lý đăng nhập và đăng ký.
- CheckInFunction – Ghi nhận chấm công vào.
- CheckOutFunction – Ghi nhận chấm công ra.
- AttendanceHistoryFunction – Truy vấn lịch sử chấm công.
- AdminFunction – Quản lý doanh nghiệp và người dùng.
- ReportFunction – Tạo báo cáo bất đồng bộ.
- WebhookFunction – Xử lý webhook thanh toán và các sự kiện từ bên ngoài.

---

#### 2. Build ứng dụng Serverless

Di chuyển đến thư mục Backend và thực hiện lệnh:

```bash
cd backend

sam build
```

Nếu quá trình Build thành công, màn hình sẽ hiển thị:

```text
Build Succeeded

Built Artifacts  : .aws-sam/build
Valid Templates  : .aws-sam/build/template.yaml
```

Điều này cho thấy AWS SAM đã biên dịch và chuẩn bị đầy đủ các tài nguyên cần thiết để triển khai lên AWS.

---

#### 3. Triển khai hạ tầng lên AWS

Thực hiện lệnh:

```bash
sam deploy --guided
```

Trong lần triển khai đầu tiên, nhập các thông tin cấu hình như sau:

```text
Configuring SAM deploy
======================

Stack Name:
smart-attendance-backend

AWS Region:
ap-southeast-1

AllowedOrigin:
https://localhost:3000

OriginVerifySecret:
SaaS-Secure-Verification-Token-2026

Confirm changes before deploy:
n

Allow SAM CLI IAM role creation:
Y

Disable rollback:
N

Save arguments to configuration file:
Y

SAM configuration file:
samconfig.toml

SAM configuration environment:
default
```

Sau khi xác nhận, AWS CloudFormation sẽ tự động tạo toàn bộ tài nguyên cần thiết.

Thời gian triển khai khoảng **2–5 phút** tùy thuộc vào tốc độ tạo tài nguyên của AWS.

---

#### 4. Xử lý lỗi thường gặp

Trong một số trường hợp, AWS SAM có thể hiển thị lỗi:

```text
Error: S3 Bucket does not exist
```

Nguyên nhân là Stack quản lý của AWS SAM vẫn còn tồn tại trong khi Deployment Bucket đã bị xóa.

Để khắc phục, thực hiện lệnh:

```bash
aws cloudformation delete-stack \
--stack-name aws-sam-cli-managed-default \
--region ap-southeast-1
```

Sau khi Stack được xóa hoàn toàn, chạy lại:

```bash
sam deploy --guided
```

AWS SAM sẽ tự động tạo lại Deployment Bucket mới.

---

#### 5. Lưu thông tin Output

Sau khi triển khai thành công, CloudFormation sẽ trả về các thông tin Output như sau:

```text
AttendanceApiUrl
https://xxxxxxxx.execute-api.ap-southeast-1.amazonaws.com/prod

CognitoUserPoolId
ap-southeast-1_xxxxxxxxx

CognitoUserPoolClientId
xxxxxxxxxxxxxxxxxxxxxxxx
```

Các thông tin này sẽ được sử dụng để cấu hình giao diện React trong các bước tiếp theo của workshop.

**Lưu ý:** Hãy lưu lại các giá trị:

+ AttendanceApiUrl
+ CognitoUserPoolId
+ CognitoUserPoolClientId

để sử dụng trong quá trình triển khai Frontend và kết nối ứng dụng với Backend Serverless.