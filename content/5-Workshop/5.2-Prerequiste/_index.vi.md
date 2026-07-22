---
title : "Điều kiện chuẩn bị"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---

#### Chuẩn bị môi trường

Trước khi triển khai **nền tảng Smart Attendance SaaS**, hãy đảm bảo rằng máy tính cá nhân hoặc môi trường AWS Cloud9 đã được cấu hình đầy đủ. Workshop này yêu cầu cài đặt một số công cụ phát triển, cấu hình thông tin xác thực AWS và cấp quyền cần thiết để triển khai các tài nguyên Serverless.

Các công cụ cần được cài đặt trước khi bắt đầu bao gồm:

+ **AWS CLI v2** – Công cụ dòng lệnh dùng để tương tác với các dịch vụ AWS.
+ **AWS SAM CLI** – Công cụ hỗ trợ xây dựng, kiểm thử và triển khai ứng dụng Serverless.
+ **Node.js (phiên bản 20 trở lên)** và **npm** – Sử dụng để phát triển giao diện React và quản lý các thư viện của AWS Lambda.
+ **Git** – Công cụ quản lý mã nguồn và tải dự án từ GitHub.

Kiểm tra các công cụ đã được cài đặt thành công bằng các lệnh sau:

```bash
aws --version
sam --version
node -v
npm -v
git --version
```

Sau khi xác nhận tất cả các công cụ đã được cài đặt đầy đủ, bạn có thể tiếp tục cấu hình tài khoản AWS.

---

#### Tạo IAM User

Để đảm bảo an toàn cho tài khoản AWS, AWS khuyến nghị **không sử dụng Root Account** trong quá trình phát triển và triển khai ứng dụng.

Hãy tạo một tài khoản IAM User với quyền quản trị bằng các bước sau:

+ Đăng nhập vào **AWS Management Console**.
+ Truy cập dịch vụ **IAM → Users**.
+ Chọn **Create user**.
+ Nhập tên người dùng, ví dụ: **WorkshopAdmin**.
+ (Tùy chọn) Cấp quyền đăng nhập vào AWS Management Console.
+ Nhấn **Next**.

Tiếp theo, cấp quyền cho người dùng:

+ Chọn **Attach policies directly**.
+ Tìm và chọn chính sách **AdministratorAccess**.
+ Kiểm tra lại thông tin.
+ Nhấn **Create user**.

Tài khoản IAM này sẽ được sử dụng để triển khai toàn bộ hạ tầng AWS trong workshop thông qua AWS SAM.

---

#### Tạo Access Key

Sau khi tạo IAM User:

+ Mở thông tin người dùng vừa tạo.
+ Chọn tab **Security credentials**.
+ Tại mục **Access keys**, chọn **Create access key**.
+ Chọn mục đích sử dụng là **Command Line Interface (CLI)**.
+ Xác nhận các khuyến nghị của AWS.
+ (Tùy chọn) Thêm mô tả như **Workshop AWS CLI**.
+ Nhấn **Create access key**.

Ngay sau khi tạo thành công, hãy tải file **CSV** chứa thông tin xác thực và lưu trữ ở nơi an toàn.

Thông tin nhận được bao gồm:

+ Access Key ID
+ Secret Access Key

Đây là thông tin sẽ được sử dụng để cấu hình AWS CLI.

---

#### Cấu hình AWS CLI

Mở Terminal hoặc Command Prompt và thực hiện lệnh:

```bash
aws configure
```

Sau đó nhập các thông tin sau:

```text
AWS Access Key ID:
AWS Secret Access Key:
Default region:
ap-southeast-1

Default output format:
json
```

Kiểm tra việc cấu hình đã thành công bằng lệnh:

```bash
aws sts get-caller-identity
```

Nếu hệ thống trả về các thông tin như **UserId**, **Account** và **ARN**, điều đó chứng tỏ AWS CLI đã được cấu hình chính xác.

---

#### Sao chép mã nguồn Workshop

Di chuyển đến thư mục làm việc và tải mã nguồn của dự án:

```bash
cd ~/Documents/AWS

git clone https://github.com/your-repository/smart-attendance-saas.git

cd smart-attendance-saas
```

Cấu trúc thư mục của dự án như sau:

```text
smart-attendance-saas/
│
├── backend/
│   ├── src/
│   ├── template.yaml
│   └── samconfig.toml
│
├── frontend/
│   ├── src/
│   └── package.json
│
└── platform_architecture.drawio
```

Trong đó:

+ **backend/** chứa mã nguồn Backend Serverless triển khai bằng AWS SAM.
+ **frontend/** chứa ứng dụng React Single Page Application.
+ **template.yaml** mô tả toàn bộ hạ tầng AWS theo mô hình Infrastructure as Code.
+ **samconfig.toml** lưu các tham số triển khai của AWS SAM.
+ **platform_architecture.drawio** chứa sơ đồ kiến trúc của hệ thống.

---

#### Sẵn sàng triển khai

Sau khi hoàn thành tất cả các bước chuẩn bị ở trên, môi trường phát triển đã được cấu hình đầy đủ và sẵn sàng để triển khai ứng dụng.

Trong phần tiếp theo của workshop, bạn sẽ tiến hành triển khai Backend của hệ thống **Smart Attendance SaaS** bằng **AWS SAM**, đồng thời cấu hình các dịch vụ như **Amazon Cognito**, **Amazon API Gateway**, **AWS Lambda**, **Amazon DynamoDB** cùng các thành phần Serverless khác để xây dựng hoàn chỉnh hệ thống.