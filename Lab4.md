### Thiết kế các ca sử dụng cho hệ thống
#### 1. Đăng Nhập (Login)

- Mục tiêu: Cho phép người dùng đăng nhập vào hệ thống.
  
- Người dùng: Tất cả người dùng (nhân viên, quản trị viên).

- Luồng chính:
- Người dùng nhập tên đăng nhập và mật khẩu.
- Hệ thống xác thực thông tin.
- Nếu thông tin hợp lệ, hệ thống chuyển hướng đến bảng điều khiển chính.

- Lý do thiết kế: Đăng nhập là cần thiết để bảo mật thông tin và đảm bảo rằng chỉ những người có quyền hạn mới có thể truy cập vào hệ thống. Hệ thống sử dụng tên người dùng và mật khẩu để xác thực.
  
#### 2. Duy Trì Thời Gian Làm Việc (Maintain Timecard)

- Mục tiêu: Giúp nhân viên cập nhật thời gian làm việc của họ.
  
- Người dùng: Nhân viên.
  
- Luồng chính:
- Nhân viên mở mẫu thời gian làm việc.
- Nhân viên nhập giờ làm việc và mã dự án.
- Hệ thống lưu thông tin thời gian làm việc.
- Nhân viên có thể xem và chỉnh sửa thông tin nếu cần.

- Lý do thiết kế: Việc duy trì thời gian công là rất quan trọng trong việc tính toán lương. Ca sử dụng này giúp nhân viên dễ dàng theo dõi và cập nhật thông tin cá nhân.
#### 3. Chạy Bảng Lương (Run Payroll)
- Mục tiêu: Tính toán và phát hành bảng lương cho nhân viên.
- Người dùng: Quản trị viên.
- Luồng chính:
- Quản trị viên chọn tùy chọn chạy bảng lương.
- Hệ thống thu thập dữ liệu từ các mẫu thời gian làm việc và thông tin nhân viên.
- Hệ thống tính toán số tiền lương dựa trên loại nhân viên (theo giờ, theo tháng, theo hoa hồng).
- Hệ thống tạo bảng lương và gửi thông tin vào ngân hàng.
- Lý do thiết kế: Chạy bảng lương là chức năng chính của hệ thống. Nó tự động tính toán lương cho nhân viên và đảm bảo rằng các khoản thanh toán được thực hiện đúng hạn. Việc tích hợp với các ca sử dụng khác như "Duy Trì Thời Gian Công" giúp hệ thống hoạt động mượt mà hơn.
#### 4. Quản Lý Thông Tin Nhân Viên (Manage Employee Information)
- Mục tiêu: Cung cấp khả năng cho quản trị viên cập nhật thông tin nhân viên.
- Người dùng: Quản trị viên.
- Luồng chính:
- Quản trị viên truy cập vào phần quản lý nhân viên.
- Quản trị viên thêm, sửa hoặc xóa thông tin nhân viên.
- Hệ thống lưu lại các thay đổi và cập nhật thông tin.
- Lý do thiết kế:
- Tính chính xác: Đảm bảo thông tin về nhân viên luôn được cập nhật và chính xác, giúp cho việc tính toán lương và quản lý nhân sự hiệu quả hơn.
- Quản lý hiệu quả: Dễ dàng theo dõi và quản lý thông tin nhân viên, từ đó hỗ trợ các quyết định về nhân sự và báo cáo.
- Đảm bảo bảo mật: Chỉ những người có quyền hạn mới có thể truy cập và thay đổi thông tin, bảo vệ dữ liệu nhạy cảm của nhân viên.
#### 5. In Bảng Lương (Print Payroll)
- Mục tiêu: In bảng lương đã được tính toán.
- Người dùng: Quản trị viên.
- Luồng chính:
- Quản trị viên chọn bảng lương cần in.
- Hệ thống kết nối với máy in.
- Hệ thống in bảng lương cho nhân viên.
- Lý do thiết kế:
- Tính minh bạch: Cung cấp cho nhân viên bảng lương chi tiết, giúp họ hiểu rõ về các khoản thanh toán và khấu trừ.
- Tiện lợi: Cho phép in bảng lương nhanh chóng và dễ dàng, phục vụ cho các nhu cầu lưu trữ và báo cáo.
- Đảm bảo tuân thủ: Hỗ trợ việc lưu trữ và cung cấp thông tin cần thiết cho các yêu cầu pháp lý và kiểm toán.
#### 6. Truy Xuất Thông Tin Bảng Lương (Access Payroll Information)
- Mục tiêu: Cho phép nhân viên truy cập thông tin bảng lương của họ.
- Người dùng: Nhân viên.
- Luồng chính:
- Nhân viên đăng nhập vào hệ thống.
- Nhân viên chọn tùy chọn truy cập thông tin bảng lương.
- Hệ thống hiển thị thông tin bảng lương hiện tại và lịch sử bảng lương.
- Lý do thiết kế:
- Dễ dàng truy cập: Giúp người dùng nhanh chóng lấy thông tin cần thiết mà không phải tìm kiếm thủ công, tiết kiệm thời gian.
- Hỗ trợ ra quyết định: Cung cấp dữ liệu cần thiết cho việc phân tích và ra quyết định liên quan đến chi phí lao động và hiệu suất làm việc.
- Tính linh hoạt: Cho phép người dùng tùy chỉnh truy xuất thông tin theo nhu cầu cụ thể, giúp cải thiện khả năng báo cáo và phân tích.

#### Biểu đồ ca sử dụng
![Diagram](https://www.planttext.com/api/plantuml/png/R96_IWD14CRxVOhX-XJcNodHA284KJp5ThbRxnRsviBkNh68bOMjBo0OnKOKBAno18iBUOzx0b_1IJWb6xBTD_FxlXbcVyhlWR5Sso9JJ8bh2pO7BPFKGYorYApCaV78vXeEix7AdH2Dt8ipYOmj6Ow94X2SSgTpfU3S6Iko06uOq2kCYBYXzlnXVeS9dAJrz6CS03TmCTpnaOF2GQYhTmZJkdoKS2GvmgXwok1IrkLzrBZQlcj8YHC7-_NqXV97Yy_519C6xVZeMR64A7968welmaE9j5BrZ3IYUiF6rlLjnxWzlUTZeQRzhsZ4grsFtshjirl6_auAhTRkwXeRXVPceSzMP__drrN7KrrFzTX0O4n__0i00F__0m00)
