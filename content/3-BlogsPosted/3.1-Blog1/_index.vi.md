---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Cập nhật bảo mật Amazon S3: SSE-C sẽ bị vô hiệu hóa mặc định từ tháng 04/2026

Amazon S3 từ lâu đã là một trong những dịch vụ lưu trữ dữ liệu phổ biến nhất trên AWS, được sử dụng rộng rãi trong nhiều hệ thống như lưu trữ website tĩnh, Data Lake, sao lưu dữ liệu, lưu trữ đa phương tiện và các ứng dụng Trí tuệ nhân tạo (AI/ML). Bên cạnh khả năng mở rộng gần như không giới hạn và độ bền dữ liệu cao, bảo mật luôn là một trong những ưu tiên hàng đầu của AWS.

Mới đây, AWS đã công bố một thay đổi quan trọng liên quan đến cơ chế mã hóa **Server-Side Encryption with Customer-Provided Keys (SSE-C)**. Bắt đầu từ **tháng 04/2026**, các **Amazon S3 General Purpose Bucket** được tạo mới sẽ **không còn hỗ trợ SSE-C theo mặc định**. Thay đổi này nhằm tăng cường tính bảo mật, giảm nguy cơ cấu hình sai và khuyến khích người dùng chuyển sang các giải pháp mã hóa được AWS quản lý như **SSE-S3** hoặc **SSE-KMS**.

---

## Vì sao AWS thực hiện thay đổi này?

SSE-C cho phép khách hàng tự cung cấp khóa mã hóa khi tải dữ liệu lên Amazon S3. Điều này giúp doanh nghiệp có toàn quyền kiểm soát khóa mã hóa, tuy nhiên cũng đồng nghĩa với việc toàn bộ trách nhiệm quản lý khóa thuộc về phía người dùng.

Nếu khóa mã hóa bị thất lạc, lưu trữ không đúng hoặc không được cung cấp khi truy xuất dữ liệu thì đối tượng đã mã hóa sẽ không thể được giải mã.

Để giảm thiểu những rủi ro trong quá trình vận hành, AWS sẽ áp dụng chính sách mới từ tháng 04/2026 với các thay đổi sau:

- Các Amazon S3 General Purpose Bucket được tạo mới sẽ mặc định vô hiệu hóa SSE-C.
- Đối với các AWS Account chưa từng sử dụng SSE-C, một số Bucket hiện có cũng có thể bị vô hiệu hóa tính năng này.
- Nếu ứng dụng vẫn gửi các request sử dụng SSE-C khi Bucket chưa được bật lại, Amazon S3 sẽ trả về lỗi **HTTP 403 Access Denied**.

Các Header thường được sử dụng với SSE-C bao gồm:

- `x-amz-server-side-encryption-customer-algorithm`
- `x-amz-server-side-encryption-customer-key`
- `x-amz-server-side-encryption-customer-key-MD5`

Những yêu cầu này sẽ không còn được chấp nhận nếu SSE-C chưa được cấu hình lại cho Bucket.

---

## Ảnh hưởng đối với Developer và DevOps

Các ứng dụng đang sử dụng SSE-C cần được rà soát trước khi chính sách mới chính thức được áp dụng.

Một số hệ thống có thể chịu ảnh hưởng gồm:

- Pipeline sao lưu dữ liệu.
- Hệ thống quản lý tài liệu.
- Dịch vụ chia sẻ tệp.
- Data Lake.
- Các ứng dụng sử dụng AWS SDK phiên bản cũ.

Nếu các ứng dụng này vẫn tiếp tục gửi Header SSE-C sau thời điểm AWS thay đổi chính sách mà chưa cập nhật cấu hình, các thao tác tải dữ liệu lên Amazon S3 sẽ thất bại ngay lập tức.

---

## Hướng xử lý được khuyến nghị

### Chỉ bật SSE-C khi thật sự cần thiết

Nếu hệ thống vẫn bắt buộc phải sử dụng SSE-C, quản trị viên cần chủ động kích hoạt lại tính năng này trước khi triển khai ứng dụng.

Việc cấu hình có thể được thực hiện thông qua:

- AWS Management Console
- AWS CLI
- AWS SDK
- AWS CloudFormation
- AWS CDK
- Terraform

Đồng thời, nên cập nhật các kịch bản Infrastructure as Code (IaC) để đảm bảo cấu hình được triển khai đồng nhất giữa các môi trường.

---

### Rà soát toàn bộ ứng dụng

Các nhóm phát triển và vận hành nên kiểm tra lại toàn bộ hệ thống nhằm xác định ứng dụng nào đang sử dụng SSE-C.

Một số nội dung cần kiểm tra bao gồm:

- Mã nguồn của ứng dụng.
- Cấu hình AWS SDK.
- Các Header được gửi trong yêu cầu Upload.
- Các Bucket đang sử dụng Customer-Provided Keys.
- Kiểm thử lại quy trình Upload trước khi chính sách mới có hiệu lực.

---

### Chuyển sang SSE-S3 hoặc SSE-KMS

AWS khuyến nghị người dùng chuyển sang một trong hai cơ chế mã hóa được quản lý sau.

#### SSE-S3

SSE-S3 là cơ chế mã hóa mặc định của Amazon S3.

Ưu điểm:

- Không cần cấu hình phức tạp.
- Không phải tự quản lý khóa mã hóa.
- Không phát sinh thêm chi phí mã hóa.
- Phù hợp với phần lớn các hệ thống.

#### SSE-KMS

Đối với môi trường Production yêu cầu mức độ bảo mật cao, AWS khuyến nghị sử dụng SSE-KMS.

Một số lợi ích nổi bật:

- Quản lý khóa tập trung thông qua AWS Key Management Service (KMS).
- Kiểm soát quyền truy cập bằng IAM.
- Theo dõi lịch sử sử dụng khóa thông qua AWS CloudTrail.
- Hỗ trợ xoay vòng khóa tự động.
- Đáp ứng nhiều tiêu chuẩn bảo mật như PCI DSS, HIPAA và ISO 27001.

---

## Một số khuyến nghị

Để chuẩn bị cho thay đổi này, các tổ chức nên:

- Kiểm tra cấu hình mã hóa của toàn bộ Amazon S3 Bucket.
- Rà soát các kịch bản Infrastructure as Code.
- Cập nhật các ứng dụng cũ đang sử dụng SSE-C.
- Kiểm thử quy trình Upload trên môi trường Development và Staging.
- Ưu tiên sử dụng SSE-KMS cho các hệ thống yêu cầu bảo mật cao.
- Theo dõi các Pipeline triển khai để kịp thời phát hiện lỗi liên quan đến mã hóa.

---

## Kết luận

Việc Amazon S3 vô hiệu hóa SSE-C theo mặc định là một thay đổi quan trọng mà các nhóm phát triển và vận hành cần lưu ý.

Chủ động rà soát hệ thống, cập nhật kịch bản triển khai và xây dựng lộ trình chuyển đổi sang SSE-S3 hoặc SSE-KMS sẽ giúp giảm thiểu rủi ro vận hành, nâng cao tính bảo mật và đảm bảo các ứng dụng tiếp tục hoạt động ổn định khi chính sách mới của AWS chính thức được áp dụng.

---

## Tài liệu tham khảo

https://aws.amazon.com/blogs/storage/advanced-notice-amazon-s3-to-disable-the-use-of-sse-c-encryption-by-default-for-all-new-buckets-and-select-existing-buckets-in-april-2026/