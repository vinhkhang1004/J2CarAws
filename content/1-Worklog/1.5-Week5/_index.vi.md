---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:
* Thiết lập kiến trúc Serverless xử lý sự kiện với AWS Lambda.
* Sử dụng hàng đợi tin nhắn Amazon SQS & Amazon SNS.
* Đóng gói Docker container cho ứng dụng.
* Vận hành Docker containers trên Amazon ECS (Elastic Container Service).
* **Lên văn phòng AWS tại TP.HCM (07/06/2026)**: Tham dự buổi đào tạo trực tiếp nâng cao về IAM Policies nâng cao, bảo mật Cognito và phân quyền chéo tài khoản.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thực hành bài Lab "Serverless Automation with AWS Lambda" - Tạo Lambda function NodeJS và trigger. | 02/06/2026 | 02/06/2026 | AWS Lambda Guide |
| Thứ 3 | Thực hành bài Lab "Messaging Systems with SQS and SNS" - Thiết lập hàng đợi đệm tin nhắn. | 03/06/2026 | 03/06/2026 | SQS/SNS Lab Guide |
| Thứ 4 | Tìm hiểu về Containerization - Tạo Dockerfile, build image và vận hành Docker container cục bộ. | 04/06/2026 | 04/06/2026 | Docker documentation |
| Thứ 5 | Thực hành bài Lab "Container Orchestration with Amazon ECS and AWS Fargate". | 05/06/2026 | 05/06/2026 | Amazon ECS Guide |
| Chủ Nhật | **Lên văn phòng AWS Việt Nam (07/06/2026)**: Học thực hành on-site nâng cao về quản lý chính sách IAM nâng cao và xác thực người dùng bằng Amazon Cognito. | 07/06/2026 | 07/06/2026 | AWS HCMC Office Training |

### Kết quả đạt được tuần 5:
* Viết và chạy thành công hàm Serverless Lambda tự động phản hồi theo sự kiện.
* Tách biệt các thành phần ứng dụng nhờ hàng đợi SQS và hệ thống push SNS.
* Đóng gói hoàn chỉnh NodeJS Express backend vào Docker image gọn nhẹ.
* Triển khai chạy container không máy chủ (Serverless Container) thành công trên ECS Fargate.
* Tham dự buổi đào tạo tại văn phòng AWS, học về IAM Policies, Cognito và các chuẩn mực bảo mật hệ thống (khớp với Hình 2).
