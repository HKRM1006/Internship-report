---
title: "Event 2"
date: 2026-07-26
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch “FCAJ - Agentic AI Build Week”

### Mục Đích Của Sự Kiện

- Tạo không gian để các đội đã tham gia **Agentic AI Build Week (AABW)** quay lại chia sẻ hành trình thực tế: từ lúc lên ý tưởng, xây dựng sản phẩm, đến lúc demo và nhận kết quả
- Lan tỏa kinh nghiệm thực chiến khi làm việc với Agentic AI trên AWS thay vì chỉ dừng ở lý thuyết
- Truyền cảm hứng và trang bị góc nhìn thực tế cho những người sắp/đang tự học, tự làm workshop cá nhân về Agentic AI
- Chỉ ra những sai lầm, khó khăn và cách vượt qua áp lực thời gian khi xây dựng sản phẩm AI trong thời gian ngắn
- Gợi mở cách áp dụng quy trình, tư duy thiết kế và kinh nghiệm của các đội vào việc tự thực hành, tự xây dựng dự án cá nhân

### Danh Sách Các Đội Chia Sẻ

- **OneTeam** (Anh Duy, Trần Đông, Đoàn Trung, Minh Việt, Anshul Roy) - chia sẻ hành trình xây dựng **KFC Bot Agent**
- **3KA** (Huỳnh An Khương, Nguyễn Quốc Huy, Ngô Quang Khôi, Hoàng Lê Thành Đức, Đặng Nguyễn Phước Lộc, Đặng Trường Hưng) - chia sẻ hành trình 24 giờ xây dựng **S.H.E.P.H.E.R.D**
- **Plan V** (Phạm Tiến Thuận Phát, Huỳnh Hoàng Long, Lê Minh Nghĩa, Trần Đại Vi, Nguyễn An) - chia sẻ quá trình xây dựng **Solution Architect Professional Native App**
- **Signal Scout Team** (Lê Tấn Lực, Đỗ Hoàng Hiếu, Triệu Quốc Hào, Nguyễn Văn Duy Khiêm, Nguyễn Công Minh, Nguyễn Trần Minh Quân) - chia sẻ hành trình xây dựng **Signal Scout**

### Nội Dung Nổi Bật

#### Hành trình cảm xúc khi làm hackathon (3KA)

- Trước ngày thi, cả đội đều mang tâm lý chung của người lần đầu: sợ chưa đủ giỏi, sợ thất bại, chưa biết bắt đầu từ đâu, và sợ không đủ thời gian
- Trong 24 giờ, cảm xúc đi qua 3 giai đoạn rõ rệt: **Doubt** (hoang mang, không biết bắt đầu từ đâu) - **Flow** (tập trung, ý tưởng bắt đầu thành hình) - **Pride** (tự hào vì thực sự làm ra được sản phẩm)
- Thử thách lớn nhất không phải là thiếu kiến thức AI hay lần đầu dùng AWS, mà là duy trì được sự tỉnh táo và tinh thần làm việc nhóm khi thiếu ngủ và code liên tục lỗi
- Bài học: **kết quả cuối cùng không quan trọng bằng những gì học được trong quá trình** - đây cũng là tinh thần chủ đạo mà cả buổi chia sẻ muốn truyền tải

#### Từ bài toán thực tế đến sản phẩm - cách các đội tư duy vấn đề (OneTeam, Signal Scout)

- OneTeam xuất phát từ một bài học có thật (McDonald's dừng thử nghiệm AI drive-thru) để chỉ ra rằng: vấn đề không nằm ở "AI có làm được không" mà ở việc **hiểu đúng bản chất bài toán hệ thống** đằng sau (dữ liệu lộn xộn, quy tắc nghiệp vụ chặt, phải xác thực trước khi thực thi)
- Cách đội xử lý: thiết kế Agent theo vòng lặp rõ ràng **Goal → Plan → Tools → Act → Verify**, và kiến trúc theo hướng "thêm chứ không xây lại" (thêm kênh = thêm adapter, thêm nghiệp vụ = thêm connector) - một tư duy có thể áp dụng cho bất kỳ dự án cá nhân nào muốn mở rộng về sau
- Signal Scout chia sẻ cách dùng **Value Creation & Delivery Canvas** để làm rõ bài toán kinh doanh trước khi bắt tay viết code, và đặc biệt là thói quen **ước tính chi phí vận hành theo nhiều kịch bản (Min/Mid/Max)** ngay từ giai đoạn ý tưởng - một việc nhiều người tự học thường bỏ qua

#### Làm việc dưới áp lực thời gian và nguồn lực hạn chế (3KA, Plan V)

- 3KA chia sẻ thật về những khó khăn kỹ thuật gặp phải: video trực tiếp không ổn định, độ trễ suy luận cao, mất dấu đối tượng giữa các khung hình, chưa từng biết dùng AWS trước đó - nhưng vẫn hoàn thành được sản phẩm nhờ chia nhỏ vấn đề và ưu tiên phần lõi trước
- Plan V chia sẻ kinh nghiệm chuyển từ quy trình thủ công (đọc tài liệu yêu cầu tay, vẽ kiến trúc từ đầu, đoán chi phí theo kinh nghiệm) sang quy trình có AI hỗ trợ từng bước - cho thấy giá trị của việc **tự động hóa phần lặp lại để dồn thời gian cho phần cần tư duy**

### Những Gì Học Được

#### Bắt đầu từ bài toán, không bắt đầu từ công nghệ

Tất cả các đội đều dành thời gian đầu để hiểu rõ vấn đề thực tế trước khi chọn công cụ AWS nào để dùng. Khi tự làm workshop cá nhân, nên viết rõ "vấn đề mình đang giải là gì" trước khi mở IDE

#### Thiết kế Agent theo vòng lặp Goal - Plan - Tools - Act - Verify

Đây là khung tư duy dễ áp dụng nhất để tự xây dựng một Agent thật sự "hành động" thay vì chỉ trả lời - có thể dùng làm khung sườn cho bất kỳ project cá nhân nào về Agentic AI

#### Ước tính chi phí và thiết kế để mở rộng ngay từ đầu

Dù chỉ là dự án cá nhân hay workshop nhỏ, nên tập thói quen phác thảo chi phí vận hành sơ bộ và thiết kế kiến trúc theo module/adapter, thay vì viết code chỉ đủ chạy demo một lần

#### Chấp nhận sai và học từ tốc độ, không phải từ sự hoàn hảo

Bài học lớn nhất từ phần chia sẻ của 3KA: cứ bắt tay làm dù chưa có nền tảng vững, sai ở đâu sửa ở đó - tinh thần này áp dụng trực tiếp được vào cách tự luyện tập, tự làm workshop một mình mà không chờ "đủ giỏi mới bắt đầu"

### Trải nghiệm trong event

- Không khí buổi chia sẻ rất gần gũi và thật: các đội không chỉ show sản phẩm đẹp mà kể lại cả phần "hậu trường" - những lúc code lỗi, thiếu ngủ, hoang mang - giúp người nghe (đặc biệt là người mới) bớt áp lực và có động lực tự bắt tay làm hơn là chỉ ngồi học lý thuyết
- Học được cách nhìn một dự án Agentic AI trọn vẹn từ góc độ người trong cuộc: từ ý tưởng, kiến trúc, chi phí, đến cảm xúc thật khi làm - điều mà đọc tài liệu hay xem demo đơn thuần không truyền tải được

#### Một số hình ảnh khi tham gia sự kiện

![Event2-1](/images/Event2-1.png)
![Event2-2](/images/Event2-2.png)

