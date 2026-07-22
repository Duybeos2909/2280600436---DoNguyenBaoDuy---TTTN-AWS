---
title: "Event 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo cáo tóm tắt: “FCAJ Community Day - Data Driven, AI Risen”

### Mục tiêu của sự kiện

- Cập nhật các xu hướng mới về Trí tuệ nhân tạo (AI) và Điện toán đám mây trên nền tảng AWS.
- Giới thiệu các ứng dụng AI Agent trong DevOps, Voice AI và tự động hóa vận hành hệ thống.
- Chia sẻ kiến trúc tích hợp AI với doanh nghiệp thông qua Model Context Protocol (MCP).
- Trình bày các giải pháp nâng cao năng suất làm việc bằng AI và Amazon Q.
- Giúp người tham dự có góc nhìn thực tế về việc triển khai AI an toàn trong môi trường doanh nghiệp.

### Diễn giả

- **Trương Trần** – AI Solution Sales, Noventiq
- **Steve Trần** – CTO & Founder, CloudThinker
- **Trung Vũ** – CEO, Revve AI
- **Anh Đặng** – Solution Sales, Noventiq
- **Nghĩ Danh** – AI Engineer, Renova Cloud
- **Kiệt Trần** – AI Engineer, AWS Student Builder Group
- **Bảo Phan** – Cloud Engineer, Cloud Kinetics
- **Nguyễn Nguyễn** – Cloud Engineer, Cloud Kinetics
- **Toàn Nguyễn** – AWS Security Builder

---

## Nội dung nổi bật

### Deep Response Engine – Tự động hóa xử lý sự cố bằng AI

Phiên mở đầu giới thiệu mô hình **Deep Response Engine**, một kiến trúc sử dụng AI để hỗ trợ vận hành và xử lý sự cố trên hạ tầng Cloud.

Thay vì chỉ phát hiện lỗi và gửi cảnh báo, hệ thống còn có khả năng:

- Thu thập log và metrics từ Amazon CloudWatch và AWS CloudTrail.
- Phân tích nguyên nhân gốc (Root Cause Analysis).
- Đề xuất hoặc tự động thực hiện Runbook thông qua AWS Systems Manager.
- Khôi phục dịch vụ bằng các quy trình Infrastructure as Code (IaC).

Giải pháp giúp giảm đáng kể thời gian phát hiện và xử lý sự cố (MTTD và MTTR), đồng thời giảm khối lượng công việc cho đội ngũ vận hành.

---

### Voice Agents – Xây dựng trợ lý giọng nói thông minh

Buổi chia sẻ tiếp theo tập trung vào việc xây dựng **Voice AI** có khả năng giao tiếp tự nhiên với người dùng.

Một số khó khăn được phân tích gồm:

- Độ trễ giữa Speech-to-Text, LLM và Text-to-Speech.
- Khả năng xử lý hội thoại thời gian thực.
- Nhận diện tiếng Việt với nhiều vùng miền và ngữ cảnh.

Giải pháp được đề xuất sử dụng:

- Amazon Bedrock.
- Streaming thời gian thực.
- Model Context Protocol (MCP).
- Các mô hình nhận dạng và tổng hợp giọng nói tối ưu cho tiếng Việt.

Qua đó, người tham dự hiểu rõ hơn cách triển khai tổng đài AI hoặc trợ lý ảo trong doanh nghiệp.

---

### AWS DevOps Agent – Trợ lý AI cho vận hành hệ thống

Một trong những nội dung ấn tượng nhất là **AWS DevOps Agent**.

Thay vì kỹ sư phải tự kiểm tra log và xử lý từng bước, AI Agent có thể:

- Phân tích log ứng dụng.
- Xác định nguyên nhân lỗi.
- Chỉnh sửa cấu hình phù hợp.
- Thực hiện triển khai lại thông qua CI/CD Pipeline.

Demo thực tế trên Amazon ECS cho thấy AI có thể tự động khôi phục dịch vụ trong thời gian rất ngắn, giúp giảm đáng kể thời gian downtime.

---

### AI hỗ trợ doanh nghiệp với Amazon Q

Buổi chia sẻ giới thiệu cách Amazon Q hỗ trợ doanh nghiệp trong nhiều quy trình khác nhau như:

- Tự động sàng lọc CV ứng viên.
- Phân tích khoảng cách kỹ năng của nhân viên.
- Lập kế hoạch nguồn lực.
- Hỗ trợ ra quyết định dựa trên dữ liệu.

Qua đó cho thấy AI không chỉ phục vụ phát triển phần mềm mà còn mang lại giá trị lớn trong quản trị doanh nghiệp.

---

### Bảo mật kết nối MCP với Amazon Q

Phiên cuối tập trung vào vấn đề bảo mật khi tích hợp AI vào hệ thống nội bộ.

Các nội dung chính bao gồm:

- Triển khai Private VPC Endpoint.
- Xây dựng Private MCP Server trên Amazon ECS, Amazon EKS hoặc AWS Lambda.
- Áp dụng nguyên tắc Least Privilege bằng AWS IAM.
- Theo dõi và ghi nhật ký toàn bộ truy cập để phục vụ kiểm toán.

Kiến trúc này giúp đảm bảo dữ liệu doanh nghiệp không bị truyền ra Internet công cộng khi AI truy cập vào hệ thống nội bộ.

---

## Kiến thức thu nhận được

### Trí tuệ nhân tạo

- Hiểu cách AI Agent hỗ trợ tự động hóa vận hành hệ thống.
- Biết quy trình xây dựng các hệ thống xử lý sự cố thông minh.
- Có cái nhìn rõ hơn về ứng dụng của Amazon Bedrock trong các giải pháp AI.

### Cloud Computing và DevOps

- Hiểu vai trò của DevOps Agent trong việc tự động hóa vận hành.
- Biết cách kết hợp CloudWatch, Systems Manager và AI để xử lý sự cố.
- Nhận thấy tầm quan trọng của Infrastructure as Code trong môi trường Cloud.

### AI cho doanh nghiệp

- Hiểu cách Amazon Q hỗ trợ nâng cao năng suất làm việc.
- Biết cách triển khai Voice AI trên nền tảng AWS.
- Có thêm kiến thức về việc tích hợp AI vào các quy trình doanh nghiệp.

### An toàn thông tin

- Hiểu cơ chế hoạt động của Model Context Protocol (MCP).
- Biết cách sử dụng Private VPC Endpoint để bảo vệ dữ liệu.
- Nhận thức được vai trò của IAM, Audit và Logging trong các hệ thống AI doanh nghiệp.

---

## Áp dụng vào công việc

Sau sự kiện, em có thể áp dụng các kiến thức đã học vào dự án thực tập như:

- Tìm hiểu và thử nghiệm Amazon Bedrock cho các tính năng AI.
- Nghiên cứu sử dụng CloudWatch kết hợp Systems Manager để tự động xử lý sự cố.
- Áp dụng các nguyên tắc bảo mật của AWS khi thiết kế hệ thống.
- Tìm hiểu kiến trúc MCP nhằm chuẩn bị cho các ứng dụng AI trong tương lai.
- Tiếp tục nghiên cứu các giải pháp tự động hóa vận hành trên nền tảng AWS.

---

## Trải nghiệm tham gia sự kiện

Tham gia **FCAJ Community Day – Data Driven, AI Risen** mang lại cho em nhiều kiến thức mới về AI, Cloud Computing và DevOps trong môi trường doanh nghiệp.

### Hiểu rõ hơn về AI trong vận hành

Các phiên trình bày giúp em nhận ra AI hiện nay không chỉ được sử dụng để tạo chatbot mà còn có thể hỗ trợ giám sát, phân tích và tự động xử lý sự cố cho hạ tầng Cloud.

### Tiếp cận các kiến trúc hiện đại

Những nội dung về Deep Response Engine, AWS DevOps Agent và Voice AI giúp em có cái nhìn rõ ràng hơn về cách các doanh nghiệp đang triển khai AI trên AWS để nâng cao hiệu quả vận hành.

### Mở rộng kiến thức về bảo mật

Phần trình bày về Model Context Protocol (MCP) giúp em hiểu rằng khi triển khai AI trong doanh nghiệp, yếu tố bảo mật luôn phải được đặt lên hàng đầu thông qua IAM, VPC và các cơ chế kiểm soát truy cập.

### Định hướng phát triển bản thân

Sau sự kiện, em có thêm động lực để tiếp tục học tập về Cloud Computing, Artificial Intelligence và AWS Security. Đồng thời, em cũng nhận thấy việc xây dựng các dự án thực tế là cách tốt nhất để nâng cao kỹ năng chuyên môn và chuẩn bị cho công việc sau khi tốt nghiệp.

> Nhìn chung, FCAJ Community Day – Data Driven, AI Risen đã mang đến nhiều kiến thức thực tiễn về AI, Cloud Computing, DevOps và bảo mật trên AWS. Những chia sẻ của các diễn giả giúp em hiểu rõ hơn xu hướng ứng dụng AI trong doanh nghiệp, đồng thời tạo động lực để tiếp tục nghiên cứu và phát triển các giải pháp Cloud hiện đại trong tương lai.