---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---
### Mục tiêu tuần 6:
* Xây dựng API tiếp nhận ảnh chụp phụ tùng bị hỏng từ người dùng.
* Phát triển thuật toán phân tích file name, metadata, từ khóa để nhận diện loại phụ tùng.
* Kết nối truy vấn DocumentDB để đưa ra các gợi ý phụ tùng thay thế tương đương.
* Cấu hình lưu trữ ảnh quét tạm thời trên Amazon S3.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Xây dựng endpoint API `/api/upload/scan-image` để nhận file ảnh phụ tùng bị hỏng từ thiết bị client. | 08/06/2026 | 08/06/2026 | Express Upload API |
| Thứ 3 | Viết thuật toán phân tích tên file, EXIF metadata và trích xuất các từ khóa (keywords) để phân loại loại phụ tùng ô tô. | 09/06/2026 | 10/06/2026 | Image Parsing Logic |
| Thứ 4 | Xây dựng các câu lệnh truy vấn MongoDB để tự động tra cứu danh sách sản phẩm thay thế tương đương trong DocumentDB. | 10/06/2026 | 11/06/2026 | DocumentDB Query Builders |
| Thứ 5 | Cấu hình đẩy ảnh quét tạm thời lên Amazon S3 Media Bucket phục vụ cải thiện chất lượng nhận diện sau này. | 11/06/2026 | 12/06/2026 | AWS S3 Integration |
| Thứ 6 | Kiểm thử đầu cuối tính năng quét ảnh và gợi ý sản phẩm thay thế phù hợp với hình ảnh mẫu. | 12/06/2026 | 12/06/2026 | Feature Testing |

### Kết quả đạt được tuần 6:
* Hoàn thành API AI Scan Image.
* Thuật toán phân tích từ khóa nhận diện chính xác các nhóm phụ tùng thông dụng (Hệ thống phanh, Lọc gió, Bugi, Lốp xe, Đèn pha).
* Hệ thống hiển thị các sản phẩm gợi ý tương thích chính xác, nâng cao trải nghiệm mua sắm của người dùng.
* Ảnh quét được lưu trữ gọn gàng trên Amazon S3.
