---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
### Mục tiêu tuần 7:
* Tích hợp thư viện thanh toán VNPay, Momo, Stripe.
* Xây dựng API sinh link thanh toán và kiểm tra chữ ký bảo mật Checksum.
* Triển khai AWS Lambda làm nhiệm vụ thu nhận Webhook (IPN) độc lập an toàn.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tích hợp SDK và viết code sinh URL thanh toán VNPay, MoMo, Stripe dựa trên thông tin đơn hàng. | 16/06/2026 | 17/06/2026 | Payment Gateway Docs |
| Thứ 3 | Xây dựng hàm băm bảo mật (Checksum) để xác thực chữ ký bảo mật do cổng thanh toán gửi về. | 17/06/2026 | 18/06/2026 | Security Hash Guides |
| Thứ 4 | Viết mã nguồn cho hàm AWS Lambda xử lý Webhook IPN bằng Node.js. | 18/06/2026 | 19/06/2026 | AWS Lambda Nodejs |
| Thứ 5 | Triển khai hàm Lambda tại Private Subnet 5 (Integration Tier) bảo mật cao để cô lập luồng nhận webhook. | 19/06/2026 | 20/06/2026 | AWS Network Integration |
| Thứ 6 | Kiểm thử liên kết luồng gọi webhook IPN giả lập từ các nhà cung cấp dịch vụ thanh toán. | 20/06/2026 | 20/06/2026 | Payment API Testing |

### Kết quả đạt được tuần 7:
* APIs sinh link thanh toán hoạt động tốt trên cả Momo, VNPay, Stripe.
* Thiết lập thành công AWS Lambda xử lý webhook IPN ở lớp mạng riêng biệt (Integration Tier).
* Luồng xử lý thanh toán bất đồng bộ tách biệt giúp máy chủ backend chính không bị quá tải khi chịu lượng request lớn.
