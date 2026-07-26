---
title: "Worklog Tuần 6"
date: 2026-07-06
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6

* Cùng nhóm đưa back-end lên AWS Lambda, chạy serverless và công khai API qua API Gateway.
* Chuẩn bị quyền truy cập và thử nghiệm gọi các dịch vụ AI từ Lambda.

### Các công việc trong tuần (06/07 - 10/07/2026)

| Thứ | Công việc | Bắt đầu | Hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 |  Chuyển backend sang chạy dưới dạng hàm serverless, công khai API qua API Gateway để frontend gọi tới. | 06/07/2026 | 06/07/2026 | [Serverless lab](https://000078.awsstudygroup.com), [API Gateway lab](https://000079.awsstudygroup.com) |
| 3 | Thiết kế quyền IAM tối thiểu cần thiết để Lambda được phép gọi các dịch vụ AI (nhận diện ảnh, trích xuất văn bản, hỏi đáp). | 07/07/2026 | 07/07/2026 | [IAM Role](https://000048.awsstudygroup.com) |
| 4 | Xây dựng hàm Lambda thử nghiệm gọi dịch vụ nhận diện nội dung ảnh trên file mẫu, đo thời gian phản hồi. | 08/07/2026 | 08/07/2026 |  |
| 5 | Xây dựng hàm thử nghiệm gọi dịch vụ trích xuất văn bản với tài liệu/ảnh chứa chữ, xử lý các định dạng phản hồi khác nhau. | 09/07/2026 | 09/07/2026 |  |
| 6 | Viết cơ chế xử lý khi dịch vụ AI không phản hồi. | 10/07/2026 | 10/07/2026 |  |

### Kết quả đạt được

1. Back-end chạy hoàn toàn serverless, có lớp API công khai để frontend gọi được, đã chuyển hẳn sang gọi API trên cloud.
2. Có cấu trúc quyền truy cập tối thiểu cần thiết để Lambda gọi được các dịch vụ AI.
3. Thử nghiệm thành công việc gọi dịch vụ nhận diện ảnh và trích xuất văn bản từ Lambda, đo được thời gian phản hồi và các giới hạn thực tế.

