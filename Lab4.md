### Thiết kế các ca sử dụng cho hệ thống
#### 1. Đăng Nhập (Login)

- Mục tiêu: Cho phép người dùng đăng nhập vào hệ thống.
  
- Người dùng: Tất cả người dùng (nhân viên, quản trị viên).

- Luồng chính:
- Người dùng nhập tên đăng nhập và mật khẩu.
- Hệ thống xác thực thông tin.
- Nếu thông tin hợp lệ, hệ thống chuyển hướng đến bảng điều khiển chính.

- Lý do thiết kế: Đăng nhập là cần thiết để bảo mật thông tin và đảm bảo rằng chỉ những người có quyền hạn mới có thể truy cập vào hệ thống. Hệ thống sử dụng tên người dùng và mật khẩu để xác thực.

  #### Biểu đồ ca sử dụng:
  ![Diagram](https://www.planttext.com/api/plantuml/png/F4-x3S8m4ErlYbFw52o0G0Y92b700AVaI2mvTcHVYWXHKT3282n02feiaWbO0STAkEvzxZszR_TPUI4dJQL1yrbGB3fLb8AvSfo9iWQ0Ch4EasrLQzio9qWUUGApUA3MMQrndLVAA2-E0XsTD380OngPGZCckw6xux4SkgSfS7fCy08Ohl6SaG-c_j7VWhmlX_UhZa6dpGAk07CpfkaoSh7WZrPiyh3c1m00__y30000)
  
#### 2. Duy Trì Thời Gian Làm Việc (Maintain Timecard)

- Mục tiêu: Giúp nhân viên cập nhật thời gian làm việc của họ.
  
- Người dùng: Nhân viên.
  
- Luồng chính:
- Nhân viên mở mẫu thời gian làm việc.
- Nhân viên nhập giờ làm việc và mã dự án.
- Hệ thống lưu thông tin thời gian làm việc.
- Nhân viên có thể xem và chỉnh sửa thông tin nếu cần.

- Lý do thiết kế: Việc duy trì thời gian công là rất quan trọng trong việc tính toán lương. Ca sử dụng này giúp nhân viên dễ dàng theo dõi và cập nhật thông tin cá nhân.

  #### Biểu đồ ca sử dụng
  ![Diagram](https://www.planttext.com/api/plantuml/png/T92nJiD038PtFyMlx1reTrGK44mLGv5OhSGa9rtkgZjdY10pCm_06y36H0Q6FacUW5VWUag78jMBvT_VRyl-7N_MKJbetrcoygHGZs2QLb6R89KQxuYuKXzGt7GxwmUH0XmXSt5itlCGlBMugZlZJDJ0ISua7nIYmpHsZHKKTzFuYcqxZM-kmMmiy4n8qKUfE2RekX-m3VkF3BuRt1fsAFTVhibJ7ygBKxwSlZztsBGfwLdFyjJpADrPT4KlHCShiLXSvfN_X2Nbw-PgHMjnTNhb7m000F__0m00)
  
#### 3. Chạy Bảng Lương (Run Payroll)
- Mục tiêu: Tính toán và phát hành bảng lương cho nhân viên.
- Người dùng: Quản trị viên.
- Luồng chính:
- Quản trị viên chọn tùy chọn chạy bảng lương.
- Hệ thống thu thập dữ liệu từ các mẫu thời gian làm việc và thông tin nhân viên.
- Hệ thống tính toán số tiền lương dựa trên loại nhân viên (theo giờ, theo tháng, theo hoa hồng).
- Hệ thống tạo bảng lương và gửi thông tin vào ngân hàng.
- Lý do thiết kế: Chạy bảng lương là chức năng chính của hệ thống. Nó tự động tính toán lương cho nhân viên và đảm bảo rằng các khoản thanh toán được thực hiện đúng hạn. Việc tích hợp với các ca sử dụng khác như "Duy Trì Thời Gian Công" giúp hệ thống hoạt động mượt mà hơn.

  #### Biểu đồ ca sử dụng
  ![Diagram](https://www.planttext.com/api/plantuml/png/R90n2i9044NxFSMGFeKvW4H54BHGKB1TaZ5PsEpAxgG8Octj4SGBM2U5dVVO4tW5Do6AWjFDdpUVF_Dixh4bRgWi99Eu8o0DHcGvGIeC9YIqOemdf0q4IruPBIMCqa8eOSbmBmV0BV1MUMFJOYzrXTXDi6yOQzsuoYH2C7FD2TQvQyugWzurW0C3NwN5X5iFJN9NNoeOk_hggSNZzhYehFFSJ0Q_w1OBcBlwJh0gFVv_9s97VqaR5C9ms9byTn5xH_q8CQhK_-K5003__mC0)
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

  #### Biểu đồ ca sử dụng
  ![Diagram](https://www.planttext.com/api/plantuml/png/V90n2i9044NxFSMGFeKnjIYs8efHR8TaJHOs4zZT529UHZl1IYj5BFOadi0hk4dbYZhT7zx_pFpdzTxN1fMfIyaaNnam5IYH5mOoeNXgH4MCOMeg1S44rwgI4WPPAKXeez2j0q0Ds6mOQmn8kUGGJEl7PKymiZT82dkc7191C2xiZc0Xx842s31mKskUedOEXnrAdt39ys77nsQFwn5_PhQEo7SixGc_KDqFYfV_KsEsTKqqZq8Ozjh3tbNagQwdOjRdbBcANm000F__0m00)
  
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

   #### Biểu đồ ca sử dụng
  ![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTEQbg9Gac-Gb5cUaQ9GafcKMfoIMP-7XTNOd99Vf62Ka1YPL5-Jew2OqfkPbvcSKbH8b1OII6nM24H909JvffRa9DVcPeAbac5ShYuGAObvgNdf2eeUUOfE3tSjJWlNS7ds8PZ2_FIbHIgkHI0eBGuDJcn6BiAe66XpePSjK3dW6nJqDMr0ml0R80BEAJcfG2z0m000F__0m00)
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
  ![Diagram](https://www.planttext.com/api/plantuml/png/Z50nJiDG3Drz2Yjx1t80r1OX5eGOGjNrAp69fHz_zBypH8YZC43LfHC3KpimHEezSWAkm4z44EfKJ_PxVizw_ZvypOCQhqrjmTAZeZhqN5QA1NlAbPq0c5oTn-JUjDvPYukYPk6WtaGuGHFG3CYqTbq_MTSIZGpz3W23cv7I4YQPRrfSD_r-gvXLtQUKcB7WijzlOdjx_3Y-IPdWCs2i9b1kGbIjgJvPGQt8HOV-yCfumqR6amzN5-S9xwhkNN35tMuIfl0IqmvXS3Qx79t-JobCSVxe4o25EKaHd_a3003__mC0)

