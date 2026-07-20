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

**Tuần 1 (05/05/2026 - 11/05/2026):** [Khởi tạo Tài khoản & Cơ bản AWS Explore](1.1-week1/)

**Tuần 2 (12/05/2026 - 18/05/2026):** [Thực hành VPC, EC2 & Database cơ bản](1.2-week2/)

**Tuần 3 (19/05/2026 - 25/05/2026):** [DynamoDB, CDN CloudFront & Lên Văn Phòng AWS (24/05)](1.3-week3/)

**Tuần 4 (26/05/2026 - 01/06/2026):** [Auto Scaling, DNS Route 53 & Bảo mật WAF/Secrets Manager](1.4-week4/)

**Tuần 5 (02/06/2026 - 08/06/2026):** [Serverless Lambda, SQS & Lên Văn Phòng AWS (07/06)](1.5-week5/)

**Tuần 6 (09/06/2026 - 15/06/2026):** [Tích hợp Thuật toán Quét & Phân tích Hình ảnh (AI Scan Image)](1.6-week6/)

**Tuần 7 (16/06/2026 - 22/06/2026):** [Tích hợp Cổng Thanh toán Ngoài & Xử lý Webhook (IPN)](1.7-week7/)

**Tuần 8 (23/06/2026 - 29/06/2026):** [Xây dựng Hàng đợi Xử lý Giao dịch & Worker Bất đồng bộ](1.8-week8/)

**Tuần 9 (30/06/2026 - 06/07/2026):** [Đóng gói Docker & Triển khai Lên ECS Fargate](1.9-week9/)

**Tuần 10 (07/07/2026 - 13/07/2026):** [Triển khai Frontend, Cấu hình CDN & Thiết lập Tường lửa Bảo mật](1.10-week10/)

**Tuần 11 (14/07/2026 - 20/07/2026):** [Kiểm thử Phục hồi Thảm họa & Xác minh Tính Sẵn sàng Cao](1.11-week11/)

**Tuần 12 (21/07/2026 - 27/07/2026):** [Tối ưu hóa Hiệu năng, Mở rộng Database & Giám sát Hệ thống](1.12-week12/)
