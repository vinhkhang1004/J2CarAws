---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:
* Tìm hiểu và thiết lập mạng ảo Amazon VPC (Virtual Private Cloud).
* Thực hành tạo và quản lý máy chủ EC2 (Elastic Compute Cloud).
* Thiết lập quyền truy cập cho EC2 qua IAM Roles.
* Tạo và lưu trữ mã nguồn web tĩnh bằng Amazon S3 Static Website Hosting.
* Khởi tạo cơ sở dữ liệu quan hệ với Amazon RDS (Relational Database Service).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thực hành bài Lab "Networking Essentials with Amazon VPC" - Tạo VPC, Subnets, Route Tables, Internet Gateway. | 11/05/2026 | 11/05/2026 | VPC Lab Guide |
| Thứ 3 | Thực hành bài Lab "Compute Essentials with Amazon EC2" - Khởi tạo EC2 instance Linux và SSH từ máy cá nhân. | 12/05/2026 | 12/05/2026 | EC2 Lab Guide |
| Thứ 4 | Thực hành bài Lab "Instance Profiling with IAM Roles for EC2" - Tạo IAM Role cấp quyền gọi S3 và gắn vào EC2. | 13/05/2026 | 13/05/2026 | IAM Role Lab Guide |
| Thứ 5 | Thực hành bài Lab "Static Website Hosting with Amazon S3" - Tạo S3 bucket, upload file index.html và cấu hình hosting. | 14/05/2026 | 15/05/2026 | S3 Hosting Guide |
| Thứ 6 | Thực hành bài Lab "Database Essentials with Amazon RDS" - Khởi tạo cụm database RDS MySQL trong subnet. | 15/05/2026 | 15/05/2026 | RDS MySQL Lab Guide |

### Kết quả đạt được tuần 2:
* Thiết lập thành công VPC cô lập với các dải phân vùng mạng con Public/Private.
* Vận hành máy chủ EC2, kiểm soát lưu lượng truy cập inbound/outbound qua Security Groups.
* Gắn IAM Roles cho EC2 giúp ứng dụng truy cập S3 an toàn không cần hard-code credentials.
* Triển khai trang web tĩnh HTML/CSS trên S3 thành công.
* Kết nối thành công tới database RDS từ EC2 instance nội bộ.
