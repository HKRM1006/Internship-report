---
title: "Worklog Tuần 5"
date: 2026-06-29
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5

* Cùng nhóm triển khai bản chạy đầu tiên của Workshop.
* Rà soát và lên kiến trúc tích hợp lớp AI (nhận diện ảnh, trích xuất văn bản, hỏi đáp) vào luồng upload.

### Các công việc trong tuần (29/06 - 03/07/2026)

| Thứ | Công việc | Bắt đầu | Hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Khởi tạo dự án backend, xây dựng chức năng upload/liệt kê file cơ bản và đưa lưu trữ lên Amazon S3 với presigned URL. | 29/06/2026 | 29/06/2026 | [FastAPI](https://fastapi.tiangolo.com/), [Amazon S3](https://000057.awsstudygroup.com) |
| 3 | Rà soát các dịch vụ AI trên AWS phù hợp với Workshop; so sánh chi phí và khả năng đáp ứng. | 30/06/2026 | 30/06/2026 | [AI services](https://000056.awsstudygroup.com) |
| 4 | Lên kiến trúc tích hợp lớp AI vào luồng upload: xác định vị trí kích hoạt, luồng dữ liệu vào/ra và cách lưu kết quả phân tích. | 01/07/2026 | 01/07/2026 |  |
| 5 | Viết script thử nghiệm độc lập gọi thử các dịch vụ AI với vài file mẫu để kiểm tra định dạng phản hồi. | 02/07/2026 | 02/07/2026 |  |
| 6 | Đánh giá kết quả thử nghiệm. | 03/07/2026 | 03/07/2026 |  |

### Kết quả đạt được

1. Có ứng dụng chạy được ở local với chức năng upload/liệt kê file, dữ liệu lưu an toàn trên Amazon S3 qua cơ chế URL tạm thời.
2. Đã chọn được bộ dịch vụ AI phù hợp (nhận diện ảnh, trích xuất văn bản, hỏi đáp) và lên được kiến trúc tích hợp vào luồng upload.
3. Có kết quả thử nghiệm ban đầu với các dịch vụ AI.

