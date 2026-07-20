---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:
* Tìm hiểu giải pháp tự động co giãn tài nguyên EC2 Auto Scaling và Application Load Balancer.
* Quản lý tên miền và cấu hình bản ghi DNS với Amazon Route 53.
* Thiết lập đường truyền nội bộ bảo mật kết nối S3 qua VPC Gateway Endpoints.
* Bảo vệ ứng dụng biên trước tấn công độc hại bằng AWS WAF.
* Quản lý và bảo mật chuỗi kết nối cơ sở dữ liệu qua AWS Secrets Manager.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thực hành bài Lab "Scaling Applications with EC2 Auto Scaling" và Application Load Balancer (ALB). | 26/05/2026 | 26/05/2026 | Auto Scaling Guide |
| Thứ 3 | Thực hành bài Lab "Hybrid DNS Management with Amazon Route 53" - Tạo private hosted zone, cấu hình record DNS. | 27/05/2026 | 27/05/2026 | Route 53 Documentation |
| Thứ 4 | Thực hành bài Lab "Private Access to S3 with VPC Endpoints" - Cấu hình VPC Endpoint trỏ tới S3 từ Private Subnet. | 28/05/2026 | 28/05/2026 | S3 Endpoint Lab Guide |
| Thứ 5 | Thực hành bài Lab "Application Protection with AWS WAF" - Viết Web ACL chặn IP và lọc request SQLi, XSS. | 29/05/2026 | 29/05/2026 | AWS WAF Lab Guide |
| Thứ 6 | Thực hành bài Lab "Credentials Management with AWS Secrets Manager" - Tạo secret lưu URI và cấu hình xoay khóa tự động. | 30/05/2026 | 30/05/2026 | Secrets Manager Guide |

### Kết quả đạt được tuần 4:
* Cấu hình thành công Auto Scaling Group tự co giãn dựa trên mức tải CPU thực tế.
* Thiết lập DNS phân giải tên miền thông suốt qua Route 53.
* Kết nối nội bộ ECS sang S3 không mất phí NAT Gateway nhờ VPC Gateway Endpoint.
* Triển khai Web ACL chặn đứng các cuộc tấn công SQL Injection và XSS phổ biến.
* Mã hóa và lưu trữ an toàn các biến môi trường nhạy cảm trong Secrets Manager.
