---
title: "Các bài Blog đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Trong thời gian thực tập, tôi đã nghiên cứu, tổng hợp và chia sẻ các bài viết liên quan đến các dịch vụ AWS trên nhóm **AWS Study Group**. Nội dung các bài viết tập trung vào các chủ đề về bảo mật, lưu trữ, sao lưu dữ liệu và tối ưu chi phí trên nền tảng AWS, giúp người đọc cập nhật những thay đổi mới nhất cũng như các phương pháp triển khai theo khuyến nghị từ AWS.

### [Blog 1 - Amazon S3 vô hiệu hóa mặc định SSE-C trên Bucket mới](3.1-Blog1/)

Bài viết giới thiệu thay đổi quan trọng của Amazon S3 khi **Server-Side Encryption with Customer-Provided Keys (SSE-C)** sẽ bị vô hiệu hóa mặc định đối với các General Purpose Bucket được tạo mới từ tháng 04/2026. Nội dung bài viết phân tích nguyên nhân của thay đổi này, những ảnh hưởng đối với các hệ thống đang sử dụng SSE-C và các khuyến nghị từ AWS trong việc chuyển sang **SSE-S3** hoặc **SSE-KMS** nhằm tăng cường bảo mật, đơn giản hóa việc quản lý khóa mã hóa và giảm thiểu rủi ro cấu hình.

### [Blog 2 - AWS Backup Search và Item-Level Recovery cho Amazon EBS & Amazon S3](3.2-Blog2/)

Bài viết giới thiệu tính năng **AWS Backup Search** và **Item-Level Recovery**, cho phép tìm kiếm và khôi phục trực tiếp từng tệp dữ liệu từ các bản sao lưu của Amazon EBS và Amazon S3 thay vì phải khôi phục toàn bộ Snapshot hoặc Volume. Bài viết trình bày các trường hợp sử dụng thực tế, cơ chế lập chỉ mục dữ liệu (Backup Indexing), quy trình khôi phục và những lợi ích trong việc giảm thời gian phục hồi (RTO), tối ưu chi phí vận hành và nâng cao hiệu quả quản trị dữ liệu.

### [Blog 3 - Tối ưu chi phí Amazon EBS: Chuyển đổi từ gp2 sang gp3](3.3-Blog3/)

Bài viết phân tích lợi ích của việc chuyển đổi Amazon EBS từ **gp2** sang **gp3** theo khuyến nghị của AWS. Nội dung so sánh sự khác biệt về chi phí, hiệu năng, IOPS, Throughput cũng như khả năng cấu hình linh hoạt giữa hai loại ổ đĩa. Ngoài ra, bài viết còn hướng dẫn quy trình rà soát, tự động hóa việc chuyển đổi bằng Infrastructure as Code (IaC) và theo dõi hiệu năng bằng Amazon CloudWatch nhằm giúp doanh nghiệp tiết kiệm chi phí lưu trữ mà vẫn đảm bảo hiệu suất và không làm gián đoạn hệ thống.

---

