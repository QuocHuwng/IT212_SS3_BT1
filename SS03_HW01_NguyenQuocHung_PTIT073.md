# BÀI 1: PHÂN TÍCH & LỰA CHỌN CHIẾN LƯỢC TÀI LIỆU HÓA

## 1. Lựa chọn phương án tối ưu

**Chọn phương án B (Antigravity).**

### Lý do

Antigravity có thể index toàn bộ dự án Guai-api nên AI hiểu được luồng xử lý hoàn chỉnh từ Controller → Service → Repository → JWT Security Filter. Nhờ đó, AI có thể tự động tổng hợp thành tài liệu SRS với các phần như Pre-conditions, Main Flow và Exceptions.

Phương án này phát huy tốt sức mạnh của công cụ học trong Session 10 vì có khả năng phân tích mã nguồn ở phạm vi toàn dự án, giữ được ngữ cảnh lớn và giảm thời gian đọc code thủ công.

---

## 2. Hạn chế của phương án A

**Mở từng file trong VSCode và dùng Copilot giải thích.**

* Chỉ hiểu từng đoạn code riêng lẻ.
* Dễ bị mất ngữ cảnh giữa các file (Context Loss).
* Người dùng phải tự ghép thông tin để viết SRS.
* Tốn thời gian khi dự án lớn.

---

## 3. Hạn chế của phương án C

**Copy nhiều file vào ChatGPT/Gemini để tạo SRS.**

* Dễ bỏ sót file quan trọng.
* AI chỉ phân tích phần code được dán vào.
* Nguy cơ Context Loss cao.
* Tài liệu có thể thiếu các luồng xử lý hoặc ngoại lệ.

---

## 4. Kết luận

Phương án B là lựa chọn tốt nhất vì AI có thể phân tích toàn bộ hệ thống, hiểu đầy đủ luồng Checkout và tạo tài liệu SRS chính xác hơn. Trong khi đó, phương án A và C đều có rủi ro thất thoát ngữ cảnh, dễ dẫn đến tài liệu không đầy đủ hoặc sai lệch.
