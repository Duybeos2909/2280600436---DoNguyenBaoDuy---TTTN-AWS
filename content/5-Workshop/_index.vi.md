---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Xây dựng nền tảng chấm công đa tenant với kiến trúc AWS Serverless

#### Tổng quan

Workshop này hướng dẫn từng bước xây dựng một **nền tảng Smart Attendance SaaS** dành cho nhiều doanh nghiệp (Multi-Tenant) dựa trên **kiến trúc AWS Serverless**.

Thông qua workshop, người thực hiện sẽ được thực hành triển khai một hệ thống quản lý chấm công hoàn chỉnh trên AWS, từ việc xây dựng hạ tầng, thiết kế cơ sở dữ liệu, xác thực người dùng, xử lý bất đồng bộ cho đến triển khai giao diện người dùng.

Các nội dung chính được thực hành bao gồm:

+ Triển khai hạ tầng Serverless bằng **AWS SAM (Serverless Application Model)** theo mô hình Infrastructure as Code (IaC).
+ Cấu hình xác thực và phân quyền người dùng với **Amazon Cognito User Pool**.
+ Thiết kế cơ sở dữ liệu **Amazon DynamoDB** theo mô hình **Single-Table Design**, đảm bảo cô lập dữ liệu giữa các doanh nghiệp thông qua **tenantId**.
+ Xây dựng quy trình xử lý bất đồng bộ bằng **AWS Step Functions Express Workflow**, **Amazon SQS** và **Amazon SES** để tạo báo cáo và gửi thông báo.
+ Triển khai giao diện **React Single Page Application (SPA)** trên **Amazon S3** kết hợp với **Amazon CloudFront** nhằm phân phối nội dung toàn cầu, đồng thời tăng cường bảo mật bằng **Custom Origin Verification Headers**.

#### Nội dung Workshop

1. [Tổng quan Workshop](5.1-Workshop-overview/)
2. [Điều kiện chuẩn bị](5.2-Prerequiste/)
3. [Triển khai Backend Serverless với AWS SAM](5.3-Deploy-SAM/)
4. [Thiết kế DynamoDB Single-Table và DynamoDB Streams](5.4-DynamoDB/)
5. [Xây dựng quy trình tạo báo cáo bất đồng bộ](5.5-Reporting-Workflow/)
6. [Triển khai React SPA và Amazon CloudFront](5.6-Frontend/)
7. [Kiểm thử toàn bộ hệ thống và dọn dẹp tài nguyên](5.7-Cleanup/)