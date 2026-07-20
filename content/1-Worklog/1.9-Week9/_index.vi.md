---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
### Mục tiêu tuần 9:
* Đóng gói ứng dụng NodeJS Express bằng Dockerfile tối ưu dung lượng.
* Cấu hình ECS Task Definitions, chạy cluster service trên AWS Fargate.
* Thiết lập Application Load Balancer (ALB) hỗ trợ Sticky Sessions.
* Thiết lập Auto Scaling và NAT Gateways chịu lỗi cao.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Viết Dockerfile sử dụng multi-stage build để tối thiểu dung lượng container image cho Backend Express. | 29/06/2026 | 29/06/2026 | Docker Guide |
| Thứ 3 | Đẩy Docker image lên Amazon ECR và viết tệp cấu hình ECS Task Definitions (CPU, RAM, ENV Variables). | 30/06/2026 | 30/06/2026 | AWS ECR & Task Definitions |
| Thứ 4 | Cấu hình Application Load Balancer (ALB) hỗ trợ Sticky Sessions để Socket.io hoạt động ổn định. | 01/07/2026 | 02/07/2026 | AWS ALB Documentation |
| Thứ 5 | Triển khai dịch vụ ECS, chạy 2 Tasks Backend NodeJS ở Private Subnet 1 và Private Subnet 2 trên 2 AZs khác nhau. | 02/07/2026 | 03/07/2026 | AWS ECS Fargate Deploy |
| Thứ 6 | Thiết lập chính sách ECS Auto Scaling (scale-out khi CPU > 70%) và cấu hình 2 NAT Gateways phục vụ outbound traffic. | 03/07/2026 | 03/07/2026 | AWS NAT Gateway & Scaling |

### Kết quả đạt được tuần 9:
* Container Backend được đóng gói nhỏ gọn (< 150MB) và lưu trữ bảo mật trên ECR.
* Ứng dụng chạy trên Amazon ECS Fargate không máy chủ (Serverless Container), dễ bảo trì và vận hành.
* Load Balancer điều phối tải thông minh, giữ kết nối chat realtime ổn định nhờ Sticky Sessions.
* Outbound traffic (gửi mail, cổng thanh toán) chạy an toàn từ Private Subnets qua NAT Gateways.
