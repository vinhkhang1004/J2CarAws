---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
### Mục tiêu tuần 8:
* Thiết lập Amazon SQS làm hàng đợi trung gian lưu hóa đơn.
* Phát triển module Worker kết nối SQS để xử lý chốt đơn hàng loạt bất đồng bộ.
* Gửi email thông báo đơn hàng thành công qua Nodemailer và cập nhật Socket.io realtime.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Khởi tạo hàng đợi Amazon SQS (Payment Queue) để làm trung gian lưu trữ giao dịch. | 23/06/2026 | 23/06/2026 | AWS SQS Console |
| Thứ 3 | Viết mã nguồn từ hàm Lambda đẩy thông tin giao dịch thành công (hóa đơn sạch) vào SQS. | 24/06/2026 | 24/06/2026 | AWS SDK SQS publisher |
| Thứ 4 | Phát triển mô-đun Worker trên Backend liên tục lắng nghe và polling tin nhắn từ hàng đợi SQS. | 25/06/2026 | 26/06/2026 | SQS Consumer Module |
| Thứ 5 | Viết logic cập nhật trạng thái đơn hàng thành 'Đã thanh toán' trong DocumentDB và xóa cache giỏ hàng tương ứng trong Redis. | 26/06/2026 | 27/06/2026 | Order Management Docs |
| Thứ 6 | Cấu hình gửi mail xác nhận tự động (Nodemailer) và bắn tín hiệu Socket.io realtime thông báo cho quản trị viên. | 27/06/2026 | 27/06/2026 | Nodemailer & Socket.io |

### Kết quả đạt được tuần 8:
* Khởi tạo hàng đợi Amazon SQS hoạt động tốt giúp giảm tải, ngắt kết nối trực tiếp (Decoupling) giữa Webhook Lambda và Backend Server.
* Module Worker rút tin nhắn xử lý chốt đơn chạy ổn định, không bị trùng lặp đơn hàng.
* Khách hàng nhận được email xác nhận ngay lập tức, Admin nhận thông báo Realtime chốt đơn trên Dashboard.
