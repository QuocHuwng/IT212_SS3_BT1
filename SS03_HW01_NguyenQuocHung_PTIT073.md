# BÀI 1: Phân tích & Lựa chọn (Áp dụng 5 thành phần Prompt để giải quyết nghiệp vụ)

## Đáp án lựa chọn

**Phương án B**

## Phân tích chi tiết

Phương án B là lựa chọn tối ưu nhất vì áp dụng đầy đủ 5 thành phần cốt lõi của một prompt hiệu quả gồm: **Role, Goal, Context, Constraint và Format**. Nhờ đó AI có thể hiểu chính xác yêu cầu nghiệp vụ và sinh ra mã nguồn phù hợp ngay từ lần đầu tiên.

### 1. Role (Vai trò)

> "Hãy đóng vai trò là một Java Developer chuyên nghiệp."

Phần này giúp AI xác định góc nhìn và chuyên môn cần sử dụng khi trả lời. AI sẽ ưu tiên các thực hành tốt trong phát triển phần mềm, tuân thủ chuẩn OOP và kiến trúc Spring Boot.

### 2. Goal (Mục tiêu)

> "Nhiệm vụ của bạn là viết class UserService xử lý đăng ký tài khoản (registerUser)."

Prompt mô tả rõ mục tiêu cần đạt được là xây dựng lớp dịch vụ đăng ký tài khoản. AI không phải suy đoán yêu cầu nên khả năng tạo ra kết quả đúng mục đích sẽ cao hơn.

### 3. Context (Bối cảnh)

> "Dự án sử dụng Spring Boot 3.x và Java 17."

Thông tin này cung cấp môi trường kỹ thuật cụ thể. AI sẽ sinh mã nguồn phù hợp với phiên bản framework và ngôn ngữ đang sử dụng, tránh tạo ra các API lỗi thời hoặc không tương thích.

### 4. Constraint (Ràng buộc)

> "Phải kiểm tra trùng email qua userRepository.existsByEmail(), nếu trùng ném ra DuplicateEmailException; mật khẩu phải được mã hóa bằng PasswordEncoder."

Đây là phần quan trọng nhất của nghiệp vụ. Prompt đã mô tả đầy đủ các quy tắc bắt buộc mà AI phải tuân thủ khi viết mã nguồn.

### 5. Format (Định dạng đầu ra)

> "Hãy trình bày kết quả dưới dạng khối mã nguồn Java kèm chú thích tiếng Việt rõ ràng ở từng bước."

Prompt chỉ rõ hình thức đầu ra mong muốn nên AI sẽ tạo kết quả đúng định dạng, dễ đọc và dễ sử dụng.

## Tại sao phương án A chưa đạt chuẩn

### Nội dung

> "Hãy viết code Java Spring Boot xử lý đăng ký tài khoản người dùng, nhớ mã hóa mật khẩu và kiểm tra xem email đã tồn tại chưa."

### Các thành phần còn thiếu

* Thiếu **Role**
* Thiếu **Context** chi tiết (không nêu Java 17, Spring Boot 3.x)
* Thiếu **Constraint** cụ thể (không yêu cầu sử dụng `userRepository.existsByEmail()`, không yêu cầu ném `DuplicateEmailException`)
* Thiếu **Format**

### Hệ quả

AI có thể:

* Viết theo nhiều cách khác nhau.
* Sử dụng cơ chế kiểm tra email không đúng yêu cầu.
* Không tạo Custom Exception.
* Không có chú thích tiếng Việt.
* Trả về giải thích thay vì mã nguồn hoàn chỉnh.

## Tại sao phương án C chưa đạt chuẩn

### Nội dung

> "Tôi có một dự án Spring Boot. Hãy tạo hàm đăng ký tài khoản. Ràng buộc là phải check trùng email và ném lỗi DuplicateEmailException. Định dạng là code Java."

### Các thành phần còn thiếu

* Thiếu **Role**
* Thiếu **Context** kỹ thuật cụ thể (không nêu Java 17, Spring Boot 3.x)
* Thiếu ràng buộc về **PasswordEncoder**
* Goal chưa đầy đủ (chỉ nói tạo hàm, không nói tạo UserService)
* Format còn đơn giản, không yêu cầu chú thích

### Hệ quả

AI có thể:

* Bỏ sót bước mã hóa mật khẩu.
* Sinh mã nguồn không đúng kiến trúc dịch vụ.
* Không giải thích logic bằng tiếng Việt.
* Tạo kết quả không đồng nhất giữa các lần chạy.

## Kết luận

Theo mô hình **Role – Goal – Context – Constraint – Format**, **Phương án B** là prompt đầy đủ và chính xác nhất. Nó cung cấp đầy đủ vai trò, mục tiêu, bối cảnh kỹ thuật, ràng buộc nghiệp vụ và định dạng đầu ra, giúp AI tạo mã nguồn Java Spring Boot đúng yêu cầu ngay từ lần đầu tiên và giảm tối đa nhu cầu chỉnh sửa thủ công.
