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

#### **Lớp Trình bày (Presentation Layer)**
- **Chức năng**: Giao tiếp trực tiếp với người dùng thông qua giao diện đồ họa (GUI).
- **Thành phần**: Các form, control, menu, các thành phần trực quan khác.
- **Vai trò**:
- Thu thập dữ liệu đầu vào từ người dùng.
- Hiển thị kết quả xử lý từ lớp nghiệp vụ.
- Kiểm tra tính hợp lệ của dữ liệu đầu vào.

- **Ví dụ**: Các form nhập liệu thông tin nhân viên, bảng lương, các biểu đồ thống kê.
#### **Lớp Nghiệp vụ (Business Logic Layer)**
- **Chức năng**: Chứa các quy tắc kinh doanh, logic xử lý của hệ thống.
- **Thành phần**: Các lớp, interface, các hàm thực hiện các nghiệp vụ.
- **Vai trò**:
- Xử lý các yêu cầu từ lớp trình bày.
- Truy xuất dữ liệu từ lớp dữ liệu.
- Thực hiện các tính toán, so sánh, kiểm tra theo quy tắc kinh doanh.
- Trả về kết quả cho lớp trình bày.
- **Ví dụ**: Tính lương, tính hoa hồng, kiểm tra quyền truy cập, in báo cáo.
#### **Lớp Dữ liệu (Data Access Layer)**
- **Chức năng**: Truy cập và quản lý dữ liệu trong cơ sở dữ liệu.
- **Thành phần**: Các lớp truy cập cơ sở dữ liệu, các câu lệnh SQL.
- **Vai trò**:
- Kết nối với cơ sở dữ liệu.
- Thực hiện các câu lệnh SQL để đọc, ghi, cập nhật, xóa dữ liệu.
- Trả về kết quả truy vấn cho lớp nghiệp vụ.
- **Ví dụ**: Truy vấn thông tin nhân viên, cập nhật thông tin lương, xóa một bản ghi.

  **1.4 Vẽ biểu đồ package mô tả kiến trúc**
  
  ![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bT1Od9sOdggWb90KMfnQbv9OabcVfw2Js9bQf6IGZMN0X0avoGM5okuXteYyKABKuiyyqfIYz8IarEvQhaGvZYL5cVcfGAL-EIdPoPZCmcc0gm0IJmujQWi4yqqbyIIH0N7v6ImWPX6WQGXicY2IOd5O8E0hbRGrRL3inE51vP7CeZB8JKl1HWq00000F__0m00)

  #### **2. Đề xuất cơ chế**

  **2.1 Các Cơ Chế Cần Giải Quyết và Lý Do:**
Để xây dựng một hệ thống lương đáp ứng đầy đủ các yêu cầu trên, cần phải thiết kế và triển khai các cơ chế sau:

**1. Cơ chế Xác thực và Ủy quyền:**
**Lý do:** Đảm bảo chỉ những người có quyền hạn mới được truy cập và thực hiện các thao tác trên hệ thống.
**Giải pháp:** Sử dụng cơ chế đăng nhập bằng tên tài khoản và mật khẩu, phân quyền truy cập dựa trên vai trò của người dùng (nhân viên, quản lý, kế toán,...).

**2. Cơ chế Quản lý Dữ liệu Nhân Viên:**
**Lý do:** Lưu trữ và quản lý thông tin chi tiết của từng nhân viên (họ tên, mã nhân viên, thông tin lương, thông tin liên lạc,...).
**Giải pháp:** Sử dụng cơ sở dữ liệu quan hệ để lưu trữ thông tin nhân viên, thiết kế các bảng và mối quan hệ phù hợp.

**3. Cơ chế Quản Lý Chấm Công:**
**Lý do:** Thu thập và lưu trữ thông tin về giờ làm việc của nhân viên, tính toán số giờ làm việc thực tế.
**Giải pháp:** Cho phép nhân viên tự nhập liệu giờ làm việc hoặc tích hợp với hệ thống chấm công tự động.

**4. Cơ chế Tính Lương:**
**Lý do:** Tính toán lương dựa trên các quy tắc phức tạp (lương cơ bản, phụ cấp, thưởng, thuế,...).
**Giải pháp:** Xây dựng các thuật toán tính lương linh hoạt, có thể tùy chỉnh theo từng loại hợp đồng lao động.

**5. Cơ chế Báo Cáo:**
**Lý do:** Cung cấp các báo cáo chi tiết về tình hình chi tiêu,...
**Giải pháp:** Xây dựng các báo cáo cho phép người dùng tùy chỉnh theo nhu cầu.
7. Cơ chế Tích Hợp với Hệ Thống Khác:
Lý do: Tích hợp với hệ thống quản lý dự án hiện có để truy xuất thông tin về dự án và mã phí.
Giải pháp: Sử dụng các công nghệ tích hợp dữ liệu như ODBC, JDBC để kết nối với cơ sở dữ liệu DB2.
8. Cơ chế Bảo Mật:
Lý do: Bảo vệ thông tin nhạy cảm của nhân viên như thông tin lương, thông tin cá nhân.
Giải pháp: Mã hóa dữ liệu, kiểm soát quyền truy cập, tạo nhật ký hoạt động.
9. Cơ chế Lưu Trữ:
Lý do: Lưu trữ dữ liệu một cách hiệu quả, đảm bảo tính sẵn sàng của dữ liệu.
Giải pháp: Sử dụng cơ sở dữ liệu quan hệ để lưu trữ dữ liệu, sao lưu dữ liệu định kỳ.
  
