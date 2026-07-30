---
title: "GIÁM SÁT SAGEMAKER PIPELINES ĐA TÀI KHOẢN – TÍCH HỢP CLOUDWATCH DASHBOARD TÙY CHỈNH"
date: 2026-07-30
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# GIÁM SÁT SAGEMAKER PIPELINES ĐA TÀI KHOẢN – TÍCH HỢP CLOUDWATCH DASHBOARD TÙY CHỈNH

Trong các tổ chức áp dụng MLOps, Amazon SageMaker Pipelines thường được dùng để tự động hóa quy trình huấn luyện và triển khai mô hình, đồng thời phân tán khối lượng công việc này trên nhiều tài khoản và khu vực AWS khác nhau nhằm tách biệt môi trường phát triển, kiểm thử và sản xuất. Tuy nhiên, sự phân tán này lại tạo ra thách thức lớn về giám sát: đội vận hành phải liên tục chuyển đổi qua lại giữa nhiều tài khoản và Region để theo dõi tiến trình từng pipeline, gây tốn thời gian và dễ bỏ sót vấn đề.

Các điểm chính cần nắm:

* **Kiến trúc hub-and-spoke:** Một tài khoản/Region chính đóng vai trò trung tâm giám sát (hub), còn các thành phần nhẹ được triển khai ở từng tài khoản/Region phụ (spoke) để thu thập dữ liệu pipeline và chuyển tiếp về trung tâm.
* **Serverless, hướng sự kiện:** Giải pháp phản hồi ngay khi có sự kiện từ SageMaker Pipeline thay vì polling hay duy trì hệ thống giám sát chạy thường trực, giúp giảm chi phí vận hành và công sức bảo trì.
* **Dashboard stack (tại hub):** Gồm CloudWatch dashboard, bảng lưu trữ Amazon DynamoDB và các hàm AWS Lambda xử lý/hiển thị dữ liệu - chỉ triển khai duy nhất tại tài khoản/Region trung tâm.
* **Forwarder stack (tại spoke):** Triển khai tại các tài khoản được giám sát, dùng Amazon EventBridge để gửi dữ liệu đã xử lý về trung tâm giám sát.
* **Luồng sự kiện xuyên tài khoản:** Khi một bước trong pipeline đổi trạng thái, SageMaker AI phát sinh sự kiện kèm siêu dữ liệu (thời gian, ARN pipeline, trạng thái bước...); EventBridge tại tài khoản nguồn bắt sự kiện, Lambda xử lý và làm giàu thông tin, rồi chuyển tiếp qua EventBridge tới tài khoản trung tâm - toàn bộ được bảo vệ bởi vai trò và chính sách AWS IAM.
* **Lưu trữ và hiển thị tại hub:** Lambda tại trung tâm tiếp nhận dữ liệu, lưu vào DynamoDB (Region, account ID, thời gian tạo/bắt đầu/kết thúc, tên hiển thị, trạng thái từng lần thực thi và từng bước), đồng thời đóng vai trò backend cho dashboard, trả về giao diện HTML hiển thị dưới dạng custom widget trên CloudWatch.
* **Trải nghiệm người dùng:** Cho phép lọc theo tên pipeline, xem chi tiết từng bước (tên, loại, thời gian, trạng thái) ngay trong AWS Management Console mà không cần chuyển đổi tài khoản/Region.
* **Cảnh báo tự động:** CloudWatch có thể kích hoạt alarm và gửi thông báo qua Amazon SNS khi phát hiện hoạt động bất thường từ người dùng dashboard.

**Ví dụ thực tế:**

Một tổ chức có 3 tài khoản AWS riêng biệt cho môi trường Dev, Test và Production, mỗi tài khoản chạy các SageMaker Pipeline huấn luyện mô hình khác nhau. Thay vì đội vận hành phải đăng nhập lần lượt vào từng tài khoản để kiểm tra trạng thái pipeline, kiến trúc hub-and-spoke cho phép toàn bộ trạng thái - từ Dev đến Production - được tổng hợp và hiển thị trên một CloudWatch dashboard duy nhất tại tài khoản trung tâm, giúp phát hiện pipeline lỗi hoặc chạy chậm ngay lập tức mà không cần rời khỏi console.

### Tài liệu tham khảo

* [AWS Machine Learning Blog - Monitor Amazon SageMaker Pipelines Cross-Account with Custom Amazon CloudWatch Dashboards](https://aws.amazon.com/blogs/machine-learning/monitor-amazon-sagemaker-pipelines-cross-account-with-custom-amazon-cloudwatch-dashboards/)

### Link bài viết

[AWS STUDY GROUP | GIÁM SÁT SAGEMAKER PIPELINES ĐA TÀI KHOẢN: TÍCH HỢP CLOUDWATCH DASHBOARD TÙY CHỈNH](https://www.facebook.com/groups/awsstudygroupfcj/posts/2228796084552018/)

### Ảnh

![Blog3](/images/blog3.PNG)

