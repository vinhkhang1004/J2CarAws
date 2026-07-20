---
title: "AWS Community Day Vietnam 2026"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Báo cáo thu hoạch: AWS Community Day Vietnam 2026

### Thông tin sự kiện
* **Tên sự kiện:** AWS Community Day Vietnam 2026
* **Thời gian:** 23/05/2026 (08:00 - 17:00)
* **Địa điểm:** Thành phố Hồ Chí Minh, Việt Nam
* **Vai trò:** Người tham dự

---

### Mục Đích Của Sự Kiện
AWS Community Day là sự kiện công nghệ quy mô lớn được tổ chức bởi cộng đồng người dùng AWS (AWS User Group Vietnam). Mục đích chính của sự kiện nhằm:
* Chia sẻ các xu hướng công nghệ mới nhất trong hệ sinh thái điện toán đám mây AWS, đặc biệt là các giải pháp Generative AI (GenAI), Serverless và Kiến trúc ứng dụng hiện đại.
* Kết nối các kỹ sư, chuyên gia kiến trúc giải pháp (SA), các Community Builders và cộng đồng doanh nghiệp công nghệ tại Việt Nam.
* Giới thiệu các bài học thực tiễn (Best Practices), case-study chuyển đổi số và tối ưu hóa chi phí vận hành đám mây từ các doanh nghiệp lớn (GoTymeX, VPBank, Cloud Kinetics...).

---

### Tóm Tắt Nội Dung Các Bài Thuyết Trình Nổi Bật

#### 1. Context Is Everything - Making AI Actually Work for You
* **Diễn giả:** Anh Tịnh Trương (Platform Engineer, GoTymeX)
* **Nội dung chính:**
  * Chỉ ra vấn đề cốt lõi khiến các ứng dụng AI thường xuyên bị ảo giác (hallucination) không phải do mô hình LLM yếu, mà do thiếu ngữ cảnh cụ thể (Context).
  * Giới thiệu kiến trúc "Prompt to Memory Pipeline" - cách thức xây dựng hệ thống ngữ cảnh động (dynamic context injection) và cơ chế lưu trữ bộ nhớ dài hạn cho AI.
  * Chia sẻ tư duy làm việc phối hợp với AI và định hướng phát triển kỹ năng cho các bạn sinh viên, kỹ sư trẻ trong kỷ nguyên AI.

#### 2. Friendly AI Assistant w/ Amazon Quick
* **Diễn giả:** Chị Phạm Ngọc Hải Anh (G-AsiaPacific Vietnam, AWS Community Builder)
* **Nội dung chính:**
  * Phân tích nỗi đau của doanh nghiệp: Người dùng tốn quá nhiều thời gian để tra cứu dữ liệu từ nhiều nguồn phân mảnh khác nhau.
  * Giới thiệu giải pháp trợ lý ảo doanh nghiệp "Amazon Quick" được phát triển dựa trên Amazon Bedrock, tích hợp hơn 40 cổng kết nối dữ liệu bảo mật (databases) và khả năng tìm kiếm web thông minh.
  * Case study thực tế: Trợ lý ảo cho Quản trị dự án (PM) tự động tạo Biên bản họp (Minutes of Meeting - MoM), gửi email nhắc lịch và đồng bộ tiến độ của lập trình viên.

#### 3. From Edge to Origin: CloudFront as Your Foundation
* **Diễn giả:** Anh Nguyễn Tuấn Thịnh (DevOps Engineer, First Cloud AI Journey)
* **Nội dung chính:**
  * Giải quyết bài toán tối ưu chi phí CDN truyền thống (tránh hiện tượng chi phí tăng đột biến không dự đoán được).
  * Giới thiệu mô hình CDN gói cước cố định (Fixed-price CDN) kết hợp Amazon CloudFront, AWS WAF, Route 53 và gói lưu trữ S3.
  * Phân tích các tính năng nâng cao: Bảo mật biên (AWS Shield, WAF, Mutual TLS, chặn địa lý), tự động chuyển vùng chịu lỗi (Origin failover), hỗ trợ giao thức HTTP/3 (QUIC) và tùy biến logic tại vùng biên thông qua CloudFront Functions và Lambda@Edge.

#### 4. 36 hrs with LotusHacks: Building UTMorpho from Idea to Reality
* **Đại diện đội thi:** UTMorpho Team (Thành viên tham dự LotusHacks 2026)
* **Nội dung chính:**
  * Chia sẻ hành trình 36 giờ thiết kế và phát triển ứng dụng Generative Design "UTMorpho" tại cuộc thi LotusHacks.
  * Sơ đồ kiến trúc ứng dụng: Frontend viết bằng React SPA triển khai qua CloudFront + S3; Backend sử dụng API Gateway + Lambda kết nối lưu trữ DynamoDB; Engine GenAI cốt lõi dùng Amazon Bedrock để phân tích bản phác thảo hình ảnh, tự động thiết kế giao diện UI và stream code hiển thị live preview.
  * Bài học về xử lý lỗi mô hình AI sinh dư thừa (overgeneration), vượt giới hạn token và cách quản lý áp lực thời gian.

#### 5. Non-Determinism of 'Deterministic' LLM Settings
* **Diễn giả:** Anh Đức Đào (Solution Architect, Cloud Kinetics)
* **Nội dung chính:**
  * Phân tích thực tế: Dù cấu hình tham số `temperature = 0` trên các API LLM thương mại, kết quả trả về vẫn không hoàn toàn đồng nhất (Non-deterministic).
  * Nguyên nhân kỹ thuật: Do tính chất không kết hợp của phép toán số thực dấu phẩy động trên GPU (floating-point arithmetic) khi tính toán song song, kết hợp cơ chế gom cụm yêu cầu động (dynamic request batching) trên hệ thống inference thương mại.
  * Giải pháp khắc phục: Sử dụng cơ chế bầu chọn đa số (Majority Voting), tự host mô hình riêng với cấu hình deterministic chặt chẽ, và định dạng kết quả đầu ra (JSON Mode / Regex Grammar).

#### 6. Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring
* **Diễn giả:** Chị Vy Lâm (Senior Business Systems Analyst, VPBank)
* **Nội dung chính:**
  * Giải quyết khó khăn trong đánh giá điểm tín dụng doanh nghiệp khởi nghiệp (startups) khi thiếu dữ liệu lịch sử tài chính truyền thống.
  * Hạn chế của hệ thống Single-Agent: Dễ bị nghẽn ngữ cảnh, sai sót cao khi xử lý tác vụ phức tạp.
  * Đề xuất mô hình "Ủy ban tín dụng ảo" (Virtual Credit Committee) sử dụng hệ thống Multi-Agent (Manager, Financial Analyst, Team Evaluator, Risk Assessor...) phối hợp đưa ra quyết định đánh giá đồng thuận.
  * Hiệu năng: Tốc độ xử lý hồ sơ giảm từ vài tuần xuống còn vài giờ (nhanh hơn 95%), giảm 95% thời gian phân tích thủ công và mang lại tỷ lệ ROI cao.

---

### Những Bài Học Rút Ra & Trải Nghiệm Thực Tế

#### 1. Tư Duy Thiết Kế Kiến Trúc
* **Hạ tầng bảo mật & tối ưu chi phí:** CloudFront không chỉ đóng vai trò phân phối nội dung (CDN) đơn thuần mà là một lớp phòng vệ biên thiết yếu cho ứng dụng. Việc cấu hình đúng VPC Gateway Endpoint cho S3 hay sử dụng CDN tối ưu hóa chi phí giúp tiết kiệm tài nguyên rất lớn cho dự án.
* **Tiếp cận Business-First:** Mọi giải pháp công nghệ, đặc biệt là tích hợp AI, đều phải xuất phát từ nhu cầu thực tiễn của doanh nghiệp để tối ưu quy trình vận hành và mang lại giá trị ROI thực sự, chứ không chỉ ứng dụng công nghệ theo xu hướng.

#### 2. Kiến Thức GenAI Chuyên Sâu
* **Nắm bắt hạn chế của LLM:** Hiểu rõ hiện tượng Non-determinism giúp chuẩn bị các phương án dự phòng khi thiết kế API tích hợp AI, tránh tin tưởng tuyệt đối vào kết quả đầu ra.
* **Xu hướng Multi-Agent:** Chuyển dịch từ việc dùng một chatbot đơn lẻ sang phối hợp nhiều AI Agent có vai trò chuyên biệt là chìa khóa để giải quyết các bài toán phức tạp quy mô doanh nghiệp.

---

### Ứng Dụng Thực Tế Vào Dự Án J2Car AutoParts
Kiến thức thu nhận từ sự kiện đã được tôi áp dụng trực tiếp vào việc thiết kế và triển khai backend cho dự án **J2Car AutoParts**:
1. **Kiến trúc bảo mật biên & CloudFront:** Triển khai React Frontend trên S3 và phân phối qua CloudFront CDN kết hợp AWS WAF và SSL/TLS (ACM) theo mô hình tối ưu hóa bảo mật và tốc độ đã học được ở Tuần 10.
2. **Xử lý bất đồng bộ chịu tải cao:** Áp dụng mô hình tách biệt kết nối (decoupling) sử dụng hàng đợi Amazon SQS ở Tuần 8 để nhận log hóa đơn từ Webhook Lambda, tránh nghẽn máy chủ chính Express tương tự giải pháp xử lý giao dịch quy mô lớn của AWS.
3. **Tối ưu hóa chức năng AI Scan Image:** Áp dụng phương pháp phân tích từ khóa và kiểm soát định dạng đầu ra cho chức năng quét ảnh phụ tùng ô tô để hạn chế sai sót từ mô hình AI ở Tuần 6.

---

### Trải Nghiệm Cá Nhân
AWS Community Day Vietnam 2026 mang lại một bầu không khí học tập vô cùng sôi động và nhiệt huyết. Việc được lắng nghe chia sẻ từ các chuyên gia đầu ngành giúp tôi củng cố và mở rộng vốn kiến thức của mình, đồng thời tạo cơ hội kết nối (networking) với những người bạn cùng chung đam mê công nghệ Cloud & AI. Sự kiện đã truyền cảm hứng lớn cho tôi trong suốt chặng đường thực tập tại đơn vị.

---

### Ảnh minh chứng sự kiện
![AWS Community Day Vietnam 2026 Presentation](/images/4-EventParticipated/event1.jpg)
