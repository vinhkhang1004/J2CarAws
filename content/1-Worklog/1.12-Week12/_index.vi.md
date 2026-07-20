---
title: "Worklog Tuần 12"
date: 2024-01-01
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---
### Mục tiêu tuần 12:
* Tối ưu hóa truy vấn MongoDB và cấu hình Replica Instances giảm tải đọc cho Database.
* Đo lường hiệu năng chịu tải hệ thống thanh toán qua SQS.
* Thiết lập AWS CloudWatch dashboard theo dõi tài nguyên và cảnh báo tự động về Email.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 4 | Tối ưu hóa các truy vấn tìm kiếm bằng cách thêm chỉ mục phức hợp (Compound Index) trên DocumentDB. | 21/07/2026 | 23/07/2026 | DB Query Tuning |
| Thứ 5 | Kiểm thử đo lường hiệu năng (Load Testing) hệ thống khi có hàng ngàn đơn hàng thanh toán qua SQS. | 24/07/2026 | 27/07/2026 | Load Testing Tools |
| Thứ 6 | Thiết lập DocumentDB Replica Node (Private Subnet 4) và Redis Replica Node để đồng bộ hóa và phân chia truy vấn đọc. | 28/07/2026 | 30/07/2026 | AWS Replication Setup |
| Thứ 6 | Tạo Dashboard trên AWS CloudWatch để giám sát CPU, RAM, Network I/O và cấu hình cảnh báo tự động về Email quản trị. | 28/07/2026 | 30/07/2026 | AWS CloudWatch Alerts |

### Kết quả đạt được tuần 12:
* Tách biệt luồng Đọc/Ghi cơ sở dữ liệu giúp tốc độ đọc tải trang tăng 40% nhờ Replica Nodes.
* Compound Indexes giúp giảm thời gian query từ hàng trăm ms xuống dưới 10ms.
* Hệ thống xử lý thành công tải đỉnh với hàng ngàn tin nhắn SQS mà không gặp lỗi nghẽn cổ chai.
* Giám sát hệ thống chủ động thông qua AWS CloudWatch Dashboard và Email cảnh báo tự động.
