### LAB1
## Phân tích kiến trúc, cơ chế, ca sử dụng

#### **1. Đề xuất kiến trúc**
**1.1 Kiến trúc ba lớp (Three-tier architecture):**
 - Lớp trình bày (Presentation layer): Giao diện người dùng (GUI) được xây dựng bằng các công nghệ như Windows Forms, WPF hoặc các framework web như ASP.NET. Giao diện này cung cấp cho người dùng các chức năng nhập liệu, truy vấn và tạo báo cáo.
 -  Lớp nghiệp vụ (Business logic layer): Chứa các lớp chứa logic nghiệp vụ của hệ thống như tính lương, tạo phiếu lương, kiểm tra quyền truy cập. Lớp này sẽ tương tác với lớp dữ liệu để truy xuất và cập nhật dữ liệu.
 - Lớp dữ liệu (Data access layer): Chứa các lớp truy cập cơ sở dữ liệu. Lớp này sẽ sử dụng các công nghệ như ADO.NET, Entity Framework để tương tác với cơ sở dữ liệu SQL Server hoặc Oracle
   
**1.2 Giải thích lý do lựa chọn**
- Kiến trúc 3 lớp được chọn vì nó giúp tách biệt các phần khác nhau của hệ thống, tăng tính bảo trì và dễ dàng mở rộng. 
