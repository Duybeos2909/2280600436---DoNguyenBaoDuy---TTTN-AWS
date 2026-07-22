---
title: "Blog 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Nội dung dưới đây chỉ mang tính chất tham khảo. Vui lòng **không sao chép nguyên văn** vào báo cáo của bạn, bao gồm cả phần cảnh báo này.
{{% /notice %}}

# AWS COST OPTIMIZATION – Tối ưu chi phí Amazon EBS: Vì sao doanh nghiệp nên chuyển từ gp2 sang gp3?

Xin chào mọi người!

Amazon EBS (Elastic Block Store) là dịch vụ lưu trữ dạng block được sử dụng phổ biến cùng Amazon EC2 trong nhiều hệ thống Production. Qua nhiều năm, không ít doanh nghiệp vẫn đang vận hành số lượng lớn EBS Volume sử dụng loại **gp2 (General Purpose SSD)** bởi đây từng là lựa chọn mặc định của AWS.

Tuy nhiên, kể từ khi **gp3** được giới thiệu, AWS đã nhiều lần khuyến nghị người dùng chuyển đổi sang loại ổ đĩa thế hệ mới này. Không chỉ có chi phí thấp hơn, gp3 còn mang đến hiệu năng ổn định và khả năng cấu hình linh hoạt hơn đáng kể. Theo **AWS Cost Optimization Hub**, chỉ riêng việc chuyển đổi từ gp2 sang gp3 có thể giúp doanh nghiệp tiết kiệm tới **20% chi phí lưu trữ Amazon EBS**, đồng thời cải thiện hiệu năng hệ thống mà không cần thay đổi kiến trúc ứng dụng hay gây gián đoạn dịch vụ.

---

## 1. SO SÁNH KIẾN TRÚC VÀ HIỆU NĂNG: gp2 VS gp3

Sự khác biệt lớn nhất giữa hai thế hệ ổ đĩa nằm ở cách phân bổ hiệu năng.

### gp2 – Hiệu năng phụ thuộc vào dung lượng

Ở gp2, hiệu năng được tính theo công thức **3 IOPS/GB**.

Điều này có nghĩa là nếu ứng dụng cần nhiều IOPS hơn thì bắt buộc phải tăng dung lượng của Volume, ngay cả khi không có nhu cầu sử dụng thêm dung lượng lưu trữ.

Ví dụ, để đạt khoảng **3.000 IOPS**, Volume cần có dung lượng khoảng **1.000 GB**, dẫn đến việc phải trả thêm chi phí cho phần dung lượng không thực sự sử dụng.

### gp3 – Tách biệt giữa dung lượng và hiệu năng

Khác với gp2, gp3 thiết kế độc lập giữa:

- Dung lượng lưu trữ.
- IOPS.
- Throughput.

Mặc định, mỗi Volume gp3 đã cung cấp:

- **3.000 IOPS**
- **125 MB/s Throughput**

mà không phụ thuộc vào kích thước ổ đĩa.

Khi cần hiệu năng cao hơn, người dùng chỉ cần tăng riêng IOPS hoặc Throughput mà không cần mở rộng dung lượng Volume.

### So sánh nhanh

- Chi phí lưu trữ của gp3 thấp hơn khoảng **20%** so với gp2.
- gp2 cung cấp **3 IOPS/GB**, trong khi gp3 mặc định đã có **3.000 IOPS**.
- Throughput của gp3 có thể mở rộng lên tới **1.000 MB/s**.
- gp3 cho phép cấu hình độc lập giữa dung lượng, IOPS và Throughput, giúp tối ưu chi phí linh hoạt hơn.

---

## 2. LỢI ÍCH CỐT LÕI VÀ CÁC WORKLOAD PHÙ HỢP

### Tiết kiệm chi phí ngay lập tức

Do đơn giá lưu trữ của gp3 thấp hơn gp2 khoảng 20%, doanh nghiệp có thể giảm đáng kể chi phí vận hành, đặc biệt với những hệ thống đang sử dụng hàng trăm hoặc hàng nghìn Volume.

### Không gây gián đoạn dịch vụ

Thông qua tính năng **Amazon EBS Elastic Volumes**, việc chuyển đổi từ gp2 sang gp3 có thể được thực hiện trực tiếp trên Volume đang hoạt động.

Quá trình chuyển đổi:

- Không cần dừng EC2.
- Không cần khởi động lại máy chủ.
- Không cần restore dữ liệu.
- Không ảnh hưởng đến ứng dụng đang chạy.

### Những workload nên ưu tiên chuyển đổi

- Web Application.
- API Server.
- MySQL.
- PostgreSQL.
- SQL Server.
- MongoDB.
- Bastion Host.
- Monitoring Server.
- Jenkins.
- GitLab Runner.
- File Server.
- Storage Node.

---

## 3. QUY TRÌNH RÀ SOÁT VÀ TỰ ĐỘNG HÓA CHO DEVOPS

### Bước 1: Rà soát các Volume gp2

Có thể sử dụng:

- AWS Cost Optimization Hub.
- AWS Cost Explorer.
- AWS CLI.

để xác định các Volume đang sử dụng gp2 và ước tính khoản chi phí có thể tiết kiệm sau khi chuyển đổi.

### Bước 2: Tự động hóa quá trình nâng cấp

Đối với môi trường có nhiều Volume, nên sử dụng các công cụ tự động hóa thay vì thao tác thủ công.

Có thể triển khai bằng:

- AWS Systems Manager Automation.
- AWS Lambda.
- AWS CLI.
- Terraform.
- AWS CloudFormation.
- AWS CDK.

Nếu hạ tầng được quản lý bằng Infrastructure as Code, cần cập nhật thuộc tính:

`volume_type = "gp3"`

để đảm bảo các lần triển khai sau không ghi đè lại cấu hình cũ.

### Bước 3: Theo dõi sau khi chuyển đổi

Sau khi hoàn tất nâng cấp, nên theo dõi các chỉ số trên Amazon CloudWatch trong khoảng **7–14 ngày**.

Các chỉ số quan trọng gồm:

- **VolumeReadOps**
- **VolumeWriteOps**
- **VolumeThroughputPercentage**
- **VolumeConsumedReadWriteOps**

Thông qua các Metrics này, nhóm DevOps có thể đánh giá mức sử dụng thực tế của hệ thống và quyết định có cần tăng thêm IOPS hoặc Throughput hay không.

---

## KẾT LUẬN

Việc chuyển đổi từ **gp2 sang gp3** được xem là một trong những giải pháp tối ưu chi phí mang lại hiệu quả nhanh nhất trên AWS.

Doanh nghiệp vừa có thể giảm khoảng **20% chi phí lưu trữ**, vừa sở hữu khả năng cấu hình hiệu năng linh hoạt hơn mà không làm gián đoạn hoạt động của hệ thống.

Nếu hạ tầng của bạn vẫn đang sử dụng Amazon EBS gp2, đây là thời điểm phù hợp để xây dựng kế hoạch tự động hóa quá trình chuyển đổi sang gp3 nhằm tối ưu cả chi phí lẫn hiệu năng trong dài hạn.

---

## Tài liệu tham khảo

https://aws.amazon.com/blogs/storage/migrate-your-amazon-ebs-volumes-from-gp2-to-gp3-and-save-up-to-20-on-costs/