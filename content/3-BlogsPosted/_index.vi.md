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

# Các bài Blog dịch

Trong quá trình thực tập, bên cạnh việc tự nghiên cứu và chia sẻ các bài viết, tôi còn tìm hiểu và dịch một số bài viết kỹ thuật từ **AWS Official Blog**. Việc dịch các tài liệu này giúp tôi hiểu rõ hơn về các tính năng mới của AWS cũng như cách áp dụng chúng trong các hệ thống thực tế.

### Blog 1 - Session Policies trong Amazon EKS Pod Identity

Bài viết giới thiệu tính năng **Session Policies** mới của Amazon EKS Pod Identity. Nội dung giải thích cách kết hợp IAM Role với Session Policy để giới hạn quyền truy cập của từng Pod trong Kubernetes theo nguyên tắc **Least Privilege**, giúp giảm số lượng IAM Role cần quản lý, tăng tính linh hoạt trong phân quyền và đơn giản hóa việc vận hành các cụm Amazon EKS quy mô lớn.

### Blog 2 - AWS Backup Search và Item-Level Recovery cho Amazon EBS và Amazon S3

Bài viết trình bày chi tiết cơ chế hoạt động của tính năng **AWS Backup Search** và **Item-Level Recovery**, bao gồm cách AWS lập chỉ mục dữ liệu trong quá trình sao lưu, tìm kiếm tệp theo metadata và khôi phục trực tiếp từng tệp dữ liệu. Nội dung cũng đề cập đến các lưu ý khi triển khai Backup Indexing, quy trình khôi phục và các phương pháp tối ưu chiến lược sao lưu trong môi trường doanh nghiệp.

### Blog 3 - Chuyển đổi Amazon EBS từ gp2 sang gp3 để tiết kiệm tới 20% chi phí

Bài viết phân tích những cải tiến của Amazon EBS **gp3** so với **gp2**, đặc biệt là khả năng tách biệt giữa dung lượng lưu trữ, IOPS và Throughput. Nội dung giới thiệu các lợi ích về tối ưu chi phí, cải thiện hiệu năng, quy trình chuyển đổi không gây gián đoạn dịch vụ (Zero Downtime), cũng như các phương pháp tự động hóa việc nâng cấp bằng AWS Systems Manager, AWS Lambda và Infrastructure as Code.