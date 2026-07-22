---
title: "AMAZON GUARDDUTY – DỊCH VỤ PHÁT HIỆN MỐI ĐE DỌA THÔNG MINH"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

# AMAZON GUARDDUTY – DỊCH VỤ PHÁT HIỆN MỐI ĐE DỌA THÔNG MINH

Amazon GuardDuty là dịch vụ phát hiện mối đe dọa được quản lý hoàn toàn bởi AWS. Nó liên tục giám sát tài khoản, workload và dữ liệu của bạn để tìm kiếm các hành vi bất thường hoặc độc hại. Điểm đặc biệt nhất của Amazon GuardDuty là bạn không cần cài đặt Agent, không cần triển khai thêm hạ tầng hay duy trì server phân tích log — chỉ cần kích hoạt dịch vụ.

Các điểm chính cần nắm:

* **Thu thập tự động:** Tự động gom dữ liệu từ VPC Flow Logs, CloudTrail event logs, DNS logs...
* **Phân tích thông minh:** Đưa dữ liệu qua mô hình Machine Learning và Threat Intelligence của AWS.
* **Phát hiện và Báo động:** So sánh hành vi với các mẫu tấn công đã biết và phát ra cảnh báo kèm mức độ nghiêm trọng.
* **Bắt bài đa dạng rủi ro:** Cảnh báo EC2 bị chiếm quyền, tài khoản IAM nghi lộ credentials, S3 request tăng đột biến từ IP lạ, hay hành vi bất thường trên EKS/Container.
* **Tự động hóa phản ứng:** Tích hợp mượt mà với Amazon EventBridge để tự động cô lập instance bị nhiễm, hoặc gửi thông báo tức thì qua các kênh đã được thiết lập.

**Ví dụ thực tế:**

Giả sử một EC2 instance của bạn bỗng dưng âm thầm gửi traffic tới một địa chỉ IP nằm trong danh sách đen. Thay vì ngồi rà tay hàng triệu dòng log, GuardDuty sẽ tự động phát hiện và gửi thông báo:

`UnauthorizedAccess:EC2/MaliciousIPCaller.Custom`

...kèm theo mức độ nguy hiểm và gợi ý xử lý tức thì cho đội vận hành!

### Tài liệu tham khảo

* [AWS GuardDuty Docs](https://docs.aws.amazon.com/guardduty/)
* [AWS GuardDuty Overview](https://aws.amazon.com/guardduty/)

### Link bài viết

[AWS Study Group VN | AMAZON GUARDDUTY – DỊCH VỤ PHÁT HIỆN MỐI ĐE DỌA THÔNG MINH | Facebook](https://www.facebook.com/groups/awsstudygroupfcj/posts/2219986985432928)

### Ảnh

![Blog1](/images/blog1.png)



