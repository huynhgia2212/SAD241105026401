### LAB1
## Phân tích kiến trúc, cơ chế, ca sử dụng

#### **1. Đề xuất kiến trúc**
**1.1 Kiến trúc ba lớp (Three-tier architecture):**
 - Lớp trình bày (Presentation layer): Giao diện người dùng (GUI) được xây dựng bằng các công nghệ như Windows Forms, WPF hoặc các framework web như ASP.NET. Giao diện này cung cấp cho người dùng các chức năng nhập liệu, truy vấn và tạo báo cáo.
 -  Lớp nghiệp vụ (Business logic layer): Chứa các lớp chứa logic nghiệp vụ của hệ thống như tính lương, tạo phiếu lương, kiểm tra quyền truy cập. Lớp này sẽ tương tác với lớp dữ liệu để truy xuất và cập nhật dữ liệu.
 - Lớp dữ liệu (Data access layer): Chứa các lớp truy cập cơ sở dữ liệu. Lớp này sẽ sử dụng các công nghệ như ADO.NET, Entity Framework để tương tác với cơ sở dữ liệu SQL Server hoặc Oracle
   
**1.2 Giải thích lý do lựa chọn**
- Kiến trúc 3 lớp được chọn vì nó giúp tách biệt các phần khác nhau của hệ thống, tăng tính bảo trì và dễ dàng mở rộng.

**1.3 Ý nghĩa từng thành phần trong kiến trúc**

**Lớp Trình bày (Presentation Layer)**
- **Chức năng**: Giao tiếp trực tiếp với người dùng thông qua giao diện đồ họa (GUI).
- **Thành phần**: Các form, control, menu, các thành phần trực quan khác.
- **Vai trò**:
- Thu thập dữ liệu đầu vào từ người dùng.
- Hiển thị kết quả xử lý từ lớp nghiệp vụ.
- Kiểm tra tính hợp lệ của dữ liệu đầu vào.

- **Ví dụ**: Các form nhập liệu thông tin nhân viên, bảng lương, các biểu đồ thống kê.
2. Lớp Nghiệp vụ (Business Logic Layer)
Chức năng: Chứa các quy tắc kinh doanh, logic xử lý của hệ thống.
Thành phần: Các lớp, interface, các hàm thực hiện các nghiệp vụ.
Vai trò:
Xử lý các yêu cầu từ lớp trình bày.
Truy xuất dữ liệu từ lớp dữ liệu.
Thực hiện các tính toán, so sánh, kiểm tra theo quy tắc kinh doanh.
Trả về kết quả cho lớp trình bày.
Ví dụ: Tính lương, tính hoa hồng, kiểm tra quyền truy cập, in báo cáo.
3. Lớp Dữ liệu (Data Access Layer)
Chức năng: Truy cập và quản lý dữ liệu trong cơ sở dữ liệu.
Thành phần: Các lớp truy cập cơ sở dữ liệu, các câu lệnh SQL.
Vai trò:
Kết nối với cơ sở dữ liệu.
Thực hiện các câu lệnh SQL để đọc, ghi, cập nhật, xóa dữ liệu.
Trả về kết quả truy vấn cho lớp nghiệp vụ.
Ví dụ: Truy vấn thông tin nhân viên, cập nhật thông tin lương, xóa một bản ghi.
