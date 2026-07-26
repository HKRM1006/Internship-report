---
title: "Worklog Tuần 7"
date: 2026-07-13
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7

* Cùng nhóm tích hợp DynamoDB để lưu metadata file.
* Tích hợp chính thức lớp AI (nhận diện ảnh, trích xuất văn bản) vào luồng upload, lưu kết quả gắn với metadata.

### Các công việc trong tuần (13/07 - 17/07/2026)

| Thứ | Công việc | Bắt đầu | Hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Tạo cơ sở dữ liệu DynamoDB lưu thông tin file, kết nối backend để ghi/truy xuất metadata. | 13/07/2026 | 13/07/2026 | [DynamoDB lab](https://000078.awsstudygroup.com) |
| 3 | Thiết kế schema lưu kết quả phân tích AI (nhãn ảnh, văn bản trích xuất) trong DynamoDB, đảm bảo tách biệt và nhất quán với metadata gốc của file. | 14/07/2026 | 14/07/2026 |  |
| 4 | Tích hợp chính thức dịch vụ nhận diện nội dung ảnh vào luồng upload để tự động gắn nhãn, lưu kết quả cùng metadata file. | 15/07/2026 | 15/07/2026 | [AI services](https://000056.awsstudygroup.com) |
| 5 | Tích hợp chính thức dịch vụ trích xuất văn bản cho tài liệu và ảnh chứa chữ, lưu văn bản trích xuất kèm metadata. | 16/07/2026 | 16/07/2026 |  |
| 6 | Kiểm thử toàn bộ luồng nhận diện ảnh và trích xuất văn bản với nhiều loại file, xử lý trường hợp file không được hỗ trợ. | 17/07/2026 | 17/07/2026 |  |

### Kết quả đạt được

1. Thông tin file được lưu và truy vấn từ DynamoDB, tách khỏi nội dung file trên nền tảng lưu trữ.
2. Thiết kế được schema lưu kết quả AI riêng biệt, nhất quán với metadata gốc.
3. Ảnh upload được tự động gắn nhãn và tài liệu được tự động trích xuất văn bản, đã kiểm thử với nhiều loại file và các trường hợp không hỗ trợ.

