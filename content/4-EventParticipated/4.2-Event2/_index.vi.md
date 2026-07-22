---
title: "Sự kiện 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Nội dung dưới đây chỉ mang tính chất tham khảo. Vui lòng **không sao chép nguyên văn** vào báo cáo của bạn, bao gồm cả phần cảnh báo này.
{{% /notice %}}

# Báo cáo tóm tắt: “FCJ Community Day - From Zero to Cloud Hero”

### Mục tiêu sự kiện

- Chia sẻ những kinh nghiệm thực tế về lộ trình nghề nghiệp trong các lĩnh vực Quản trị hệ thống, Điện toán đám mây và An ninh mạng.
- Giới thiệu các công nghệ hiện đại như Docker, GraphRAG, Amazon Bedrock, Amazon Neptune và AWS WAF.
- Trình bày cách trí tuệ nhân tạo có thể được ứng dụng trong quản trị hạ tầng và phát hiện các mối đe dọa an ninh mạng.
- Giúp người tham dự hiểu rõ tầm quan trọng của kinh nghiệm thực hành, dự án cá nhân và sản phẩm thực tế trong quá trình phát triển nghề nghiệp.
- Truyền cảm hứng cho sinh viên chủ động học tập, xây dựng portfolio kỹ thuật và từng bước phát triển năng lực Cloud.

### Diễn giả

- **Trần Trung Vinh** – Quản trị viên hệ thống tại Central Retail Group
- **Lê Hoàng Gia Đại** – Sinh viên năm cuối Đại học HUTECH, định hướng AWS Cloud và Cyber Security
- **Việt Phát** – Sinh viên chuyên ngành Trí tuệ nhân tạo tại Swinburne University of Technology
- Các thành viên của **Cộng đồng FCJ AI**

---

## Nội dung nổi bật

### Hành trình từ IT Helpdesk đến Senior System Administrator

Phần trình bày mở đầu tập trung vào hành trình nghề nghiệp thực tế của diễn giả, bắt đầu từ vị trí IT Helpdesk, sau đó phát triển lên System Administrator và tiếp tục mở rộng sang Cloud và DevOps.

Thông qua câu chuyện này, người tham dự hiểu rõ hơn rằng một vị trí khởi đầu tưởng chừng đơn giản vẫn có thể tạo ra nền tảng rất tốt cho sự nghiệp kỹ thuật về sau.

Một số kinh nghiệm quan trọng được chia sẻ gồm:

- Rèn luyện khả năng xử lý sự cố trong môi trường có áp lực cao.
- Học cách giao tiếp rõ ràng với người dùng cuối.
- Phát triển tư duy tìm nguyên nhân thay vì chỉ xử lý biểu hiện.
- Tìm hiểu cách các hệ thống CNTT vận hành trong thực tế.
- Chủ động học Linux, Networking và các công nghệ hạ tầng.
- Xây dựng môi trường lab cá nhân để luyện tập.
- Tập trung vào dự án thực tế thay vì chỉ học lý thuyết.
- Chuẩn bị kỹ trước các buổi phỏng vấn kỹ thuật.

Diễn giả cũng chia sẻ về quá trình phỏng vấn tại Central Retail Group, bao gồm:

- Nghiên cứu trước hệ thống và định hướng công nghệ của doanh nghiệp.
- Chuẩn bị các dự án thực tế có thể trình bày.
- Luyện tập thiết kế kiến trúc.
- Chuẩn bị tình huống xử lý sự cố.
- Thực hành các bài troubleshooting.

Một thông điệp để lại nhiều ấn tượng là:

> **"Nơi bạn bắt đầu không quyết định nơi bạn sẽ kết thúc. Hãy tiếp tục tiến lên, vì mỗi bước nhỏ đều có ý nghĩa."**

Phần chia sẻ cũng chỉ ra một số sai lầm phổ biến của người mới:

- Học quá nhiều công nghệ cùng lúc.
- Chỉ xem tài liệu nhưng không thực hành.
- Ngại đặt câu hỏi.
- Sợ thất bại hoặc sợ bị đánh giá.
- Chỉ tập trung lấy chứng chỉ mà không xây dựng sản phẩm.

Thay vào đó, diễn giả khuyến nghị nên tập trung đào sâu một hoặc hai kỹ năng cốt lõi trước, sau đó áp dụng chúng vào các dự án thực tế để tạo ra một portfolio có giá trị.

---

### Các trường hợp sử dụng Docker và nhóm lệnh thực tế

Phần tiếp theo giới thiệu Docker theo hướng thực hành, thay vì chỉ trình bày khái niệm container ở mức lý thuyết.

Docker được sử dụng phổ biến trong nhiều tình huống như:

- Xây dựng CI/CD pipeline.
- Triển khai kiến trúc Microservices.
- Chuẩn hóa môi trường phát triển.
- Tạo môi trường kiểm thử độc lập.
- Xây dựng ứng dụng Cloud-native.
- Đóng gói các ứng dụng cũ để phục vụ hiện đại hóa hệ thống.
- Giảm khác biệt giữa môi trường Development, Staging và Production.

Buổi chia sẻ cũng tổng hợp các nhóm lệnh Docker thường gặp.

#### Quản lý Image

- `docker image ls`
- `docker pull`
- `docker push`
- `docker build`

Các lệnh này được sử dụng để kiểm tra image hiện có, tải image từ registry, đẩy image lên registry và tạo image mới từ Dockerfile.

#### Quản lý vòng đời Container

- `docker create`
- `docker run`
- `docker start`
- `docker stop`
- `docker restart`
- `docker rm`

Nhóm lệnh này giúp tạo, khởi chạy, dừng, khởi động lại và xóa container.

#### Tương tác và kiểm tra Container

- `docker exec`
- `docker attach`
- `docker logs`
- `docker top`
- `docker inspect`

Những lệnh này hỗ trợ truy cập vào container, kiểm tra log, xem tiến trình đang chạy và theo dõi cấu hình chi tiết.

#### Quản lý Network

- `docker network create`
- `docker network ls`
- `docker network connect`
- `docker network disconnect`

Docker Network cho phép các container giao tiếp với nhau theo từng mô hình mạng riêng biệt.

#### Quản lý Volume

- `docker volume create`
- `docker volume inspect`
- `docker volume rm`
- `docker volume prune`

Volume được sử dụng để lưu trữ dữ liệu tách biệt khỏi vòng đời của container.

#### Docker Compose

- `docker-compose build`
- `docker-compose up`
- `docker-compose down`
- `docker-compose ls`
- `docker-compose logs`

Docker Compose đặc biệt hữu ích khi một ứng dụng có nhiều thành phần như frontend, backend, database và message broker.

Phần này giúp em củng cố cách Docker được sử dụng trong quy trình phát triển hằng ngày, đồng thời cung cấp một bộ lệnh tham khảo có thể áp dụng trực tiếp vào các dự án cá nhân và dự án thực tập.

---

### Xây dựng ứng dụng GraphRAG với Amazon Bedrock và Amazon Neptune

Một trong những phần đáng chú ý nhất của sự kiện là nội dung về **GraphRAG**.

GraphRAG là mô hình kết hợp giữa:

- Graph Database.
- Retrieval-Augmented Generation.
- Large Language Model.
- Cơ chế tìm kiếm dựa trên mối quan hệ giữa các thực thể.

Khác với RAG truyền thống, vốn thường tập trung vào độ tương đồng giữa các vector, GraphRAG bổ sung khả năng biểu diễn mối quan hệ giữa các đối tượng trong dữ liệu.

Ví dụ, trong một hệ thống tri thức doanh nghiệp, GraphRAG có thể xác định mối liên hệ giữa:

- Nhân viên.
- Phòng ban.
- Dự án.
- Tài liệu.
- Công nghệ.
- Khách hàng.
- Sự kiện.
- Quy trình nghiệp vụ.

Điều này giúp mô hình AI không chỉ tìm ra nội dung gần giống về mặt ngữ nghĩa mà còn hiểu được ngữ cảnh và các mối quan hệ phức tạp trong dữ liệu.

Buổi chia sẻ giới thiệu hai hướng triển khai:

#### Hướng Fully Managed

Sử dụng:

- Amazon Bedrock.
- Amazon Neptune Analytics.
- Các dịch vụ AWS được quản lý hoàn toàn.

Hướng này giúp giảm khối lượng công việc vận hành và phù hợp với doanh nghiệp muốn triển khai nhanh.

#### Hướng Open-source

Sử dụng:

- GraphRAG Toolkit.
- Amazon Neptune Analytics.
- Amazon Bedrock.
- LlamaIndex.
- Các thư viện mã nguồn mở hỗ trợ xây dựng pipeline tùy chỉnh.

Hướng này linh hoạt hơn và phù hợp khi đội ngũ phát triển cần kiểm soát sâu kiến trúc hoặc logic truy xuất dữ liệu.

Phần chia sẻ giúp em hiểu rằng GraphRAG phù hợp với các bài toán cần xử lý nhiều lớp thông tin và các mối quan hệ phức tạp, chẳng hạn:

- Hệ thống hỏi đáp doanh nghiệp.
- Tìm kiếm tri thức nội bộ.
- Phân tích tài liệu pháp lý.
- Quản lý tài sản và nhân sự.
- Phát hiện gian lận.
- Hỗ trợ quyết định dựa trên dữ liệu liên kết.

---

### Kết hợp Machine Learning với AWS WAF để phát hiện tấn công mạng

Một nội dung quan trọng khác tập trung vào việc kết hợp **AWS WAF** với **Machine Learning** nhằm tăng khả năng phát hiện tấn công mạng.

AWS WAF có thể bảo vệ ứng dụng khỏi nhiều dạng tấn công phổ biến thông qua:

- Managed Rules.
- IP filtering.
- Rate-based rules.
- Geographic restrictions.
- Bot control.
- Rule matching dựa trên request.

Tuy nhiên, cơ chế dựa trên chữ ký và luật cố định vẫn có những giới hạn nhất định.

Các cuộc tấn công mới hoặc hành vi bất thường chưa có mẫu nhận diện sẵn có thể vượt qua lớp phòng thủ truyền thống. Vì vậy, phần trình bày đề xuất sử dụng Machine Learning để phân tích hành vi mạng.

Giải pháp được trình bày bao gồm:

- Thu thập dữ liệu lưu lượng mạng.
- Tiền xử lý dữ liệu.
- Huấn luyện mô hình phát hiện xâm nhập.
- Sử dụng bộ dữ liệu CSE-CIC-IDS2018.
- Nhận diện lưu lượng bình thường và bất thường.
- Hiển thị kết quả trên dashboard theo thời gian thực.
- Đối chiếu dự đoán của mô hình với sự kiện từ AWS WAF.
- Gửi cảnh báo khi phát hiện dấu hiệu tấn công.

Cách tiếp cận này cho phép hệ thống kết hợp hai lớp phòng vệ:

- AWS WAF xử lý request ở tầng ứng dụng.
- Mô hình Machine Learning phân tích hành vi để phát hiện bất thường.

Điều em rút ra từ phần này là một hệ thống bảo mật hiệu quả không nên chỉ dựa vào một công cụ duy nhất. Việc kết hợp nhiều lớp bảo vệ giúp cải thiện độ chính xác và giảm nguy cơ bỏ sót các cuộc tấn công mới.

---

### Hệ thống phát hiện xâm nhập mạng NIDS

Phần tiếp theo tập trung vào thiết kế và triển khai **Network Intrusion Detection System**, viết tắt là NIDS.

NIDS là hệ thống được xây dựng để theo dõi lưu lượng mạng và nhận diện các hoạt động có dấu hiệu bất thường hoặc tấn công.

Các chức năng cốt lõi của NIDS gồm:

#### Giám sát lưu lượng

Theo dõi:

- Network traffic.
- Web traffic.
- HTTP và HTTPS traffic.
- Kết nối giữa các máy trong mạng.
- Lưu lượng vào và ra khỏi hệ thống.

#### Phân tích hành vi

NIDS có thể sử dụng:

- Signature-based detection.
- Rule-based detection.
- Anomaly detection.
- Machine Learning.

Cơ chế signature phù hợp với các mẫu tấn công đã biết, trong khi anomaly detection giúp phát hiện những hành vi mới chưa từng xuất hiện.

#### Phát hiện và cảnh báo

Khi phát hiện dấu hiệu đáng ngờ, hệ thống có thể:

- Gửi cảnh báo theo thời gian thực.
- Ghi nhận mức độ nghiêm trọng.
- Phân loại loại tấn công.
- Chuyển thông tin đến hệ thống giám sát.

#### Ghi log và phản ứng

NIDS lưu lại:

- Thời điểm xảy ra sự cố.
- Địa chỉ IP nguồn và đích.
- Cổng mạng liên quan.
- Loại giao thức.
- Dạng hành vi bất thường.
- Kết quả phân tích.

Dữ liệu này có thể phục vụ điều tra sau sự cố và cải thiện chính sách bảo mật.

#### Khả năng tích hợp

NIDS có thể kết nối với:

- Firewall.
- SIEM.
- IDS hoặc IPS khác.
- Cloud monitoring.
- Security dashboard.
- Alerting system.

Phần trình bày giúp em hiểu rõ hơn rằng NIDS không chỉ là một phần mềm độc lập mà còn là một thành phần trong kiến trúc bảo mật nhiều lớp của doanh nghiệp.

---

### Ứng dụng Machine Learning và AWS trong Cybersecurity

Phần cuối trình bày cách Machine Learning và AWS có thể phối hợp trong các hệ thống bảo mật hiện đại.

Machine Learning mang lại một số lợi ích:

- Học từ hành vi mạng thực tế.
- Phát hiện mẫu tấn công mới.
- Phân tích khối lượng dữ liệu lớn.
- Tự động hóa quá trình nhận diện bất thường.
- Thích ứng với sự thay đổi của các mối đe dọa.
- Hỗ trợ ưu tiên sự kiện có mức độ nguy hiểm cao.

AWS cung cấp nền tảng hạ tầng và các dịch vụ có khả năng:

- Mở rộng theo nhu cầu.
- Quản lý hạ tầng vật lý.
- Tích hợp logging và monitoring.
- Tăng cường bảo mật theo nhiều lớp.
- Xử lý dữ liệu lớn.
- Triển khai mô hình Machine Learning.
- Tự động hóa phản ứng sự cố.

Một điểm quan trọng được nhấn mạnh là Machine Learning không nên được xem như công cụ thay thế hoàn toàn các biện pháp bảo mật truyền thống.

Thay vào đó, Machine Learning nên bổ sung cho:

- AWS WAF.
- Firewall.
- IAM.
- Logging.
- Monitoring.
- Threat intelligence.
- IDS và IPS.
- Quy trình ứng phó sự cố.

---

## Kiến thức tiếp thu

### Định hướng nghề nghiệp

Thông qua câu chuyện của anh Trần Trung Vinh, em hiểu rõ hơn rằng kinh nghiệm thực tế là yếu tố rất quan trọng trong ngành CNTT.

Chứng chỉ có thể hỗ trợ xác nhận kiến thức, nhưng portfolio và khả năng giải quyết vấn đề thực tế mới thể hiện rõ năng lực của một ứng viên.

Em cũng hiểu rõ hơn lộ trình:

- IT Helpdesk.
- System Administrator.
- Cloud Engineer.
- DevOps Engineer.

Hành trình này cho thấy việc bắt đầu ở một vị trí cơ bản không giới hạn cơ hội phát triển trong tương lai.

### Docker và Containerization

Buổi chia sẻ giúp em:

- Hiểu rõ hơn các trường hợp sử dụng Docker.
- Biết cách quản lý image và container.
- Nắm được vai trò của Docker Network và Volume.
- Hiểu cách Docker hỗ trợ CI/CD và Microservices.
- Có thêm nhóm lệnh thực tế để sử dụng khi phát triển phần mềm.

### GraphRAG và AI trên AWS

Em hiểu được cách kết hợp Graph Database với Large Language Model nhằm tạo ra hệ thống hỏi đáp có ngữ cảnh sâu hơn.

Amazon Bedrock và Amazon Neptune có thể được sử dụng để xây dựng các ứng dụng AI xử lý dữ liệu nhiều mối quan hệ.

Phần này giúp em mở rộng góc nhìn ngoài RAG truyền thống và nhận thấy tiềm năng của GraphRAG trong các hệ thống tri thức phức tạp.

### Bảo mật mạng trên AWS

Em hiểu rõ hơn vai trò của:

- AWS WAF.
- NIDS.
- Machine Learning.
- Dashboard giám sát.
- Logging.
- Alerting.
- Phân tích hành vi.

Việc kết hợp nhiều công cụ có thể tạo ra một hệ thống bảo vệ toàn diện hơn so với việc chỉ phụ thuộc vào một lớp phòng thủ.

---

## Khả năng áp dụng vào công việc

Kiến thức từ sự kiện có thể được áp dụng vào dự án thực tập theo nhiều hướng.

### Áp dụng Docker

Docker có thể được sử dụng để:

- Chuẩn hóa môi trường phát triển.
- Chạy frontend và backend nhất quán.
- Tạo môi trường test.
- Giảm lỗi do khác biệt cấu hình giữa các máy.
- Hỗ trợ CI/CD trong tương lai.

### Áp dụng AWS WAF

Trong kiến trúc Smart Attendance SaaS, AWS WAF có thể được đặt trước Amazon CloudFront và API Gateway nhằm:

- Chặn IP bất thường.
- Giới hạn số lượng request.
- Giảm nguy cơ bot attack.
- Chặn các mẫu request độc hại.
- Tăng cường bảo vệ cho frontend và API.

### Nghiên cứu GraphRAG

GraphRAG có thể được nghiên cứu cho các tính năng tương lai như:

- Trợ lý hỏi đáp nội bộ.
- Tìm kiếm tài liệu.
- Truy vấn quy định chấm công.
- Liên kết người dùng, công ty, ca làm và báo cáo.
- Phân tích dữ liệu có nhiều mối quan hệ.

### Xây dựng portfolio thực tế

Một bài học quan trọng từ sự kiện là không nên chỉ tập trung vào chứng chỉ.

Em cần tiếp tục:

- Hoàn thiện source code.
- Viết tài liệu dự án.
- Xây dựng kiến trúc.
- Thực hành Docker.
- Tạo các bài lab AWS.
- Đưa sản phẩm lên GitHub.
- Ghi lại quá trình học tập và triển khai.

---

## Trải nghiệm tham gia sự kiện

Tham gia **FCJ Community Day – From Zero to Cloud Hero** mang lại cho em nhiều kiến thức thực tế về Cloud Computing, DevOps, Artificial Intelligence và Cybersecurity.

Không gian sự kiện có quy mô vừa phải, tạo điều kiện thuận lợi để người tham dự theo dõi nội dung, đặt câu hỏi và trao đổi trực tiếp với diễn giả.

### Ấn tượng về hành trình nghề nghiệp thực tế

Câu chuyện từ IT Helpdesk đến Senior System Administrator là phần để lại cho em nhiều ấn tượng nhất.

Nội dung này giúp em nhận ra rằng sự nghiệp kỹ thuật không nhất thiết phải bắt đầu từ một vị trí cao hoặc một công nghệ phức tạp. Điều quan trọng là liên tục học hỏi, thực hành và không ngại bắt đầu từ những công việc nền tảng.

### Docker theo hướng thực hành

Phần Docker không chỉ trình bày khái niệm mà còn cung cấp nhiều nhóm lệnh có thể sử dụng ngay.

Điều này giúp em hình dung rõ hơn cách container được áp dụng trong môi trường phát triển và triển khai phần mềm thực tế.

### Lần đầu tiếp cận GraphRAG

GraphRAG là một khái niệm mới đối với em.

Việc kết hợp Amazon Neptune với Amazon Bedrock mở ra một cách tiếp cận mới cho những bài toán cần liên kết nhiều lớp tri thức.

Phần này tạo động lực để em tìm hiểu thêm về Graph Database, RAG và các dịch vụ AI trên AWS.

### Góc nhìn rộng hơn về Cybersecurity

Các nội dung liên quan đến AWS WAF, NIDS và Machine Learning giúp em hiểu rằng bảo mật Cloud không chỉ là cấu hình một vài rule.

Một hệ thống thực tế cần kết hợp:

- Phòng thủ tại tầng ứng dụng.
- Giám sát lưu lượng.
- Phát hiện bất thường.
- Logging.
- Cảnh báo.
- Phân tích dữ liệu.
- Quy trình phản ứng.

### Động lực tiếp tục học tập

Sự kiện củng cố cho em niềm tin rằng kiến thức chỉ thực sự có giá trị khi được áp dụng vào dự án.

Thay vì chỉ học nhiều công nghệ một cách rời rạc, em cần tập trung vào những kỹ năng cốt lõi, tạo sản phẩm thực tế và cải thiện chúng theo thời gian.

## Một số hình ảnh của sự kiện

![FCJ Community Day – From Zero to Cloud Hero](/images/anhevent6-6-2026.jpg)

> Nhìn chung, sự kiện đã giúp em mở rộng hiểu biết về Cloud Computing, Docker, trí tuệ nhân tạo và an ninh mạng. Quan trọng hơn, chương trình truyền cảm hứng để em tiếp tục xây dựng các dự án thực tế, hoàn thiện portfolio kỹ thuật và chuẩn bị tốt hơn cho định hướng nghề nghiệp trong lĩnh vực AWS Cloud và Cybersecurity.