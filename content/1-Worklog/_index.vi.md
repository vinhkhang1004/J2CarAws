---
title: "Nhật ký công việc"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

### Tổng quan dự án

Hệ thống J2Car AutoParts được thiết kế theo mô hình Micro-services/Containerized chạy trên nền tảng điện toán đám mây Amazon Web Services (AWS), đảm bảo tính sẵn sàng cao (High Availability), bảo mật tuyệt đối và khả năng tự động mở rộng theo tải (Auto Scaling).

**Luồng xử lý chính:**
* **Truy cập phía người dùng (Frontend):** Ứng dụng Single Page Application (SPA) React được biên dịch và lưu trữ trên Amazon S3 Web Bucket, phân phối toàn cầu qua Amazon CloudFront và bảo vệ bởi AWS WAF.
* **Xử lý logic nghiệp vụ (Backend):** Các API REST và kết nối Socket.io được định tuyến thông qua Application Load Balancer (ALB) (hỗ trợ Sticky Sessions) đến các container ECS Backend Task (NodeJS + Express) chạy trên AWS Fargate nằm trong các Private Subnets bảo mật.
* **Thanh toán bất đồng bộ (Payment Integration):** Cổng thanh toán bên ngoài (Momo, VNPay, Stripe) gọi Webhook IPN đến AWS Lambda. Lambda tiếp nhận, kiểm tra tính hợp lệ và đẩy log hóa đơn sạch vào Amazon SQS (Payment Queue). Các Backend Tasks (ECS Fargate) đóng vai trò Worker rút tin nhắn từ hàng đợi SQS để xử lý chốt đơn và thông báo trạng thái thời gian thực thông qua Socket.io.
* **Lưu trữ dữ liệu:** Dữ liệu Document được lưu trữ tại Amazon DocumentDB (tương thích MongoDB) với cấu trúc Cluster gồm Primary Node (đọc/ghi) và Replica Node (chỉ đọc) tự động đồng bộ. Bộ nhớ đệm và quản lý phiên kết nối Socket.io sử dụng Amazon ElastiCache Redis (Primary/Replica).

---

### Nhật ký công việc (12 Tuần)

Dưới đây là tiến độ chi tiết theo từng tuần thực hiện dự án:

**Tuần 1 (05/05/2026 - 10/05/2026):** [Làm quen với môi trường thực tập, văn hóa làm việc tại FCAJ và quy trình thực hiện dự án. Tìm hiểu tổng quan về AWS, các dịch vụ điện toán đám mây và hoàn thành một số bài tập cơ bản nhằm làm quen với công nghệ và môi trường làm việc.](1.1-week1/)

**Tuần 2 (11/05/2026 - 17/05/2026):** [Tiếp tục thực hiện các task nhỏ và nghiên cứu các dịch vụ nền tảng của AWS như IAM, EC2, S3. Tìm hiểu cách quản lý tài nguyên, lưu trữ dữ liệu và cơ chế phân quyền trên hệ thống AWS thông qua thực hành các bài lab cơ bản.](1.2-week2/)

**Tuần 3 (18/05/2026 - 24/05/2026):** [Tham gia làm việc trực tiếp tại văn phòng, tiếp tục nghiên cứu các dịch vụ AWS và thực hiện các bài thực hành liên quan đến VPC, RDS, CloudWatch nhằm hiểu rõ hơn về mạng, cơ sở dữ liệu và cơ chế giám sát hệ thống.](1.3-week3/)

**Tuần 4 (25/05/2026 - 31/05/2026):** [Tiếp tục tìm hiểu các kiến thức chuyên sâu trên AWS và thực hiện các bài lab liên quan đến Elastic Load Balancer, Auto Scaling, Route 53, Lambda và các dịch vụ Container như ECS, EKS. Qua đó nắm được kiến trúc triển khai và khả năng mở rộng của hệ thống trên nền tảng đám mây.](1.4-week4/)

**Tuần 5 (01/06/2026 - 07/06/2026):** [Nghiên cứu thêm các kiến thức về nghiệp vụ và hệ sinh thái doanh nghiệp. Tìm hiểu các nguyên tắc thiết kế hệ thống, bảo mật, kiến trúc phần mềm và quy trình phát triển sản phẩm trong môi trường thực tế thông qua các dịch vụ serverless và lưu trữ bảo mật.](1.5-week5/)

**Tuần 6 (08/06/2026 - 14/06/2026):** [Bắt đầu tham gia phân tích nghiệp vụ và xây dựng ý tưởng cho dự án thực hành (Workshop). Nghiên cứu yêu cầu hệ thống cho ứng dụng thương mại điện tử phụ tùng ô tô J2Car AutoParts, thiết kế các API cơ bản và xây dựng tính năng phân tích hình ảnh AI Scan Image nhận diện linh kiện hỏng.](1.6-week6/)

**Tuần 7 (15/06/2026 - 21/06/2026):** [Tiếp tục hoàn thiện giai đoạn phân tích và thiết kế kiến trúc hệ thống J2Car AutoParts. Xây dựng mô hình dữ liệu, thiết kế các module chức năng, tích hợp cổng thanh toán ngoài (Momo, VNPay, Stripe) và triển khai hàm AWS Lambda Serverless làm webhook IPN trong lớp mạng an toàn.](1.7-week7/)

**Tuần 8 (22/06/2026 - 28/06/2026):** [Tiếp tục hoàn thiện thiết kế dự án J2Car AutoParts, xây dựng luồng xử lý giao dịch bất đồng bộ bằng Amazon SQS để giảm tải hệ thống. Phát triển module Backend Worker kết nối SQS để polling tin nhắn, chốt đơn tự động, xóa cache giỏ hàng trong Redis, đồng thời gửi email thông báo qua Nodemailer và Socket.io realtime.](1.8-week8/)

**Tuần 9 (29/06/2026 - 05/07/2026):** [Bắt đầu phát triển hệ thống J2Car AutoParts dựa trên tài liệu thiết kế. Xây dựng các module Backend và Frontend, đóng gói container Backend bằng Docker và triển khai chạy cluster không máy chủ trên Amazon ECS Fargate, cấu hình ALB với Sticky Sessions để đảm bảo kết nối chat thời gian thực hoạt động ổn định.](1.9-week9/)

**Tuần 10 (06/07/2026 - 12/07/2026):** [Triển khai toàn diện hệ thống J2Car AutoParts lên AWS: host React SPA Frontend trên S3 Web Hosting, cấu hình định tuyến qua CloudFront CDN mã hóa HTTPS. Áp dụng AWS WAFv2 thiết lập các rule bảo mật ngăn chặn SQL Injection, XSS bảo vệ an toàn cho hệ thống.](1.10-week10/)

**Tuần 11 (13/07/2026 - 19/07/2026):** [Thực hiện kiểm thử chức năng và kiểm thử tích hợp trên toàn bộ hệ thống J2Car AutoParts sau khi triển khai. Giả lập kịch bản sập Availability Zone (AZ) để kiểm tra khả năng tự động khôi phục thảm họa (Disaster Recovery), phát hiện và khắc phục các lỗi phát sinh trong quá trình failover.](1.11-week11/)

**Tuần 12 (20/07/2026 - 27/07/2026):** [Hoàn thiện dự án J2Car AutoParts thông qua kiểm thử tải (Load Testing), rà soát toàn bộ chức năng và tối ưu hiệu năng hệ thống bằng chỉ mục MongoDB, tách biệt Đọc/Ghi qua DocumentDB/Redis Replicas và cấu hình CloudWatch Dashboard theo dõi tài nguyên.](1.12-week12/)
