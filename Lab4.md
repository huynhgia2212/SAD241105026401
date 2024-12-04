### Thiết kế các ca sử dụng cho hệ thống
#### 1. Đăng Nhập (Login)

- Mục tiêu: Cho phép người dùng đăng nhập vào hệ thống.
  
- Người dùng: Tất cả người dùng (nhân viên, quản trị viên).

- Luồng chính:
- Người dùng nhập tên đăng nhập và mật khẩu.
- Hệ thống xác thực thông tin.
- Nếu thông tin hợp lệ, hệ thống chuyển hướng đến bảng điều khiển chính.
  
#### 2. Duy Trì Thời Gian Làm Việc (Maintain Timecard)

- Mục tiêu: Giúp nhân viên cập nhật thời gian làm việc của họ.
  
- Người dùng: Nhân viên.
  
- Luồng chính:
- Nhân viên mở mẫu thời gian làm việc.
- Nhân viên nhập giờ làm việc và mã dự án.
- Hệ thống lưu thông tin thời gian làm việc.
- Nhân viên có thể xem và chỉnh sửa thông tin nếu cần.
#### 3. Chạy Bảng Lương (Run Payroll)
- Mục tiêu: Tính toán và phát hành bảng lương cho nhân viên.
- Người dùng: Quản trị viên.
- Luồng chính:
- Quản trị viên chọn tùy chọn chạy bảng lương.
- Hệ thống thu thập dữ liệu từ các mẫu thời gian làm việc và thông tin nhân viên.
- Hệ thống tính toán số tiền lương dựa trên loại nhân viên (theo giờ, theo tháng, theo hoa hồng).
- Hệ thống tạo bảng lương và gửi thông tin vào ngân hàng.
#### 4. Quản Lý Thông Tin Nhân Viên (Manage Employee Information)
- Mục tiêu: Cung cấp khả năng cho quản trị viên cập nhật thông tin nhân viên.
- Người dùng: Quản trị viên.
- Luồng chính:
- Quản trị viên truy cập vào phần quản lý nhân viên.
- Quản trị viên thêm, sửa hoặc xóa thông tin nhân viên.
- Hệ thống lưu lại các thay đổi và cập nhật thông tin.
#### 5. In Bảng Lương (Print Payroll)
- Mục tiêu: In bảng lương đã được tính toán.
- Người dùng: Quản trị viên.
- Luồng chính:
- Quản trị viên chọn bảng lương cần in.
- Hệ thống kết nối với máy in.
- Hệ thống in bảng lương cho nhân viên.
#### 6. Truy Xuất Thông Tin Bảng Lương (Access Payroll Information)
- Mục tiêu: Cho phép nhân viên truy cập thông tin bảng lương của họ.
- Người dùng: Nhân viên.
- Luồng chính:
- Nhân viên đăng nhập vào hệ thống.
- Nhân viên chọn tùy chọn truy cập thông tin bảng lương.
- Hệ thống hiển thị thông tin bảng lương hiện tại và lịch sử bảng lương.
