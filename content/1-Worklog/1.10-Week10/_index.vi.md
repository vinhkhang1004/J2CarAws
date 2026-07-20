---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---
### Mục tiêu tuần 10:
* Build mã nguồn React SPA và upload lên S3 Web Bucket (Static Website Hosting).
* Tạo CloudFront Distribution tăng tốc độ tải trang toàn cầu.
* Cấu hình CORS an toàn trên Express Backend.
* Cài đặt SSL/TLS HTTPS và cấu hình AWS WAF ngăn chặn các tấn công mạng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Build React SPA thành tệp tĩnh và tải lên Amazon S3 Web Bucket, kích hoạt Static Website Hosting. | 06/07/2026 | 06/07/2026 | React Build & S3 Hosting |
| Thứ 3 | Cấu hình CORS trên Express Backend chỉ cho phép tên miền chính thức của website kết nối. | 07/07/2026 | 07/07/2026 | Express CORS Docs |
| Thứ 4 | Thiết lập Amazon CloudFront liên kết với S3 Web Bucket, cấu hình SSL/TLS (HTTPS) thông qua AWS Certificate Manager (ACM). | 08/07/2026 | 09/07/2026 | AWS ACM & CloudFront |
| Thứ 5 | Tạo và cấu hình AWS WAF (Web Application Firewall) trước CloudFront và ALB. | 09/07/2026 | 10/07/2026 | AWS WAF Ruleset |
| Thứ 6 | Thiết lập các Rule bảo mật trong WAF ngăn chặn SQL Injection, Cross-Site Scripting (XSS) và giảm thiểu DDoS. | 10/07/2026 | 10/07/2026 | OWASP Top 10 WAF |

### Kết quả đạt được tuần 10:
* Giao diện người dùng React chạy tốc độ cao, phân phối tĩnh qua CloudFront có độ trễ cực thấp.
* Toàn bộ hệ thống chạy qua HTTPS bảo mật (mã hóa SSL).
* AWS WAF chặn đứng các đợt scan lỗi bảo mật tự động và SQL Injection/XSS bảo vệ ứng dụng.
