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

**7. Cơ chế Tích Hợp với Hệ Thống Khác:**

**Lý do:** Tích hợp với hệ thống quản lý dự án hiện có để truy xuất thông tin về chi tiêu.

**Giải pháp:** Sử dụng các ứng dụng tích hợp dữ liệu như ODBC, JDBC để kết nối với cơ sở dữ liệu.

**8. Cơ chế Bảo Mật:**

**Lý do:** Bảo vệ thông tin của nhân viên như thông tin lương, thông tin cá nhân.

**Giải pháp:** Mã hóa dữ liệu, kiểm soát quyền truy cập, tạo nhật ký hoạt động.

**9. Cơ chế Lưu Trữ:**

**Lý do:** Lưu trữ dữ liệu một cách hiệu quả, đảm bảo tính sẵn sàng của dữ liệu.

**Giải pháp:** Sử dụng cơ sở dữ liệu quan hệ để lưu trữ dữ liệu, sao lưu dữ liệu định kỳ.

#### **3. Phân tích ca sử dụng payment**
Dựa trên ca sử dụng Payment, ta có thể xác định các lớp phân tích sau:

**Customer:** Đại diện cho khách hàng, lưu trữ thông tin cá nhân, lịch sử giao dịch.

**Product:** Đại diện cho sản phẩm, lưu trữ thông tin về sản phẩm (tên, giá, số lượng).

**Order:** Đại diện cho một đơn hàng, lưu trữ thông tin về khách hàng, giao dịch, tổng tiền.

**Payment:** Đại diện cho một phương thức thanh toán, lưu trữ thông tin về phương thức thanh toán (tiền mặt, thẻ tín dụng, chuyển khoản).

**PaymentMethod:** Đại diện cho một phương thức thanh toán cụ thể (ví dụ: Thẻ tín dụng).

**PaymentGateway:** Đại diện cho cổng thanh toán, thực hiện việc xử lý giao dịch thanh toán.

 #### Mô tả bằng biểu đồ sequence:
 ![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bS1aCvCpYn8p2jHS2ujBidFJIr24VGlIa4J2KYip4tDAt5FB4ajJwp49iN51JDAGTSEOeALGd9HAb07n3Wm2P93DSjAeQ0eFpcrk1Xc3geqaWOhXSJIaepyeiogL9WYRCOLfHQNvc0p1kgc0eX444GPt5KmrmCTdP-NbbcK2t4rbqDgNWemq000003__mC0)

 **Xác Định Nhiệm Vụ Của Từng Lớp**
 
- **Customer:** Quản lý thông tin cá nhân, tạo đơn hàng, theo dõi đơn hàng.
- **Product:** Lưu trữ thông tin sản phẩm, tính giá trị đơn hàng.
- **Order:** Quản lý thông tin đơn hàng, thực hiện thanh toán, cập nhật trạng thái đơn hàng.
- **Payment:** Lưu trữ thông tin về phương thức thanh toán, thực hiện các nghiệp vụ liên quan đến thanh toán.
- **PaymentMethod:** Định nghĩa các phương thức thanh toán cụ thể và các nghiệp vụ liên quan.
- **PaymentGateway:** Kết nối với các cổng thanh toán thứ ba để xử lý giao dịch.

  #### Xác Định Thuộc Tính Và Quan Hệ Giữa Các Lớp Bằng Biểu Đồ

  ![Diagram](https://www.planttext.com/api/plantuml/png/T54n3i8m3Dpp2giZ4WDh9oHc15-m4akDr2HLx0m8yJ86diGNSDkK8X1BpfRlpfVaUN_iMJ1B2RsnFJB3eR2aG1ck1i0xFI86Kg20lbT4vp8nQvMoeypcPghqd9ChLdwKG_PsH4Tiin_4fxYAJgF9Ah5r_IIRxCPD0ru2HT5Aqqhvt3bFLWCCgKpCgZcITCdzLyxphynAUhz3isjWkuLcqzIiBNJ8Pgu_XiljMx0f2lhupL5OqiuMI_TBgA5QA4nip9wYqnzw0G00__y30000)

  **Biểu đồ lớp trên đã mô tả các lớp, thuộc tính và quan hệ giữa các lớp trong hệ thống thanh toán.**

  #### Phân tích ca sử dụng Maintain Timecard
Dựa trên ca sử dụng Maintain Timecard, ta có thể xác định các lớp phân tích sau:

**Employee:** Đại diện cho nhân viên, lưu trữ thông tin cá nhân.

**Timecard:** Đại diện cho thẻ chấm công, lưu trữ thông tin về giờ làm việc, ngày làm việc.

**Department:** Đại diện cho phòng ban, lưu trữ thông tin về phòng ban.

**Project:** Đại diện cho dự án, lưu trữ thông tin về dự án.

**Role:** Đại diện cho vai trò của người dùng (nhân viên, quản lý).

#### Mô Tả Hành Vi Thông Qua Biểu Đồ Sequence

![Diagram](https://www.planttext.com/api/plantuml/png/V91D3W8X38Ntd88BU04MPZQUG3r00vsa2J08nOIpkV18Nc767p0OughDb_TUN_gutQV443axAy8sILC0p_BWWbqAOWTFv513D1qybiJeXAWEkTj_c98HBnaJDz-RFnKLAJcJDqrGbpw4S_I3Z7fHIKCfM2XDCooJWm76lrr-9ACs2QwZZ6yNlVYPeZk_eeIOq9ljkIi0003__mC0)

 #### Xác Định Nhiệm Vụ Của Từng Lớp
 
- **Employee:** Xem, cập nhật thông tin thẻ chấm công của mình.
- **Timecard:** Lưu trữ thông tin về giờ làm việc, ngày làm việc, liên kết với nhân viên và dự án.
- **Department**: Lưu trữ thông tin về phòng ban.
- **Project:** Lưu trữ thông tin về dự án.
- **Role:** Xác định quyền truy cập của người dùng vào hệ thống.

 #### Xác Định Thuộc Tính Và Quan Hệ Giữa Các Lớp

 ![Diagram](https://www.planttext.com/api/plantuml/png/X90z3i8m38NtdCBAYDI1jLC7s1bwWT1O9IW_LUCE274o1ex45N15caPqO8cT-7lFTjxFLnD9ZJGvApghOeIZ6sou8S9T01ZDXrSEEMWS67JeYIza77Pgr54yH18USdqZnUHPq6qoMDa5cbifceFnCyL9c2XbmnYksD7gS_e-_BJaSjv3xYLK5SYTN9lMS55nYt0ejgZXZ3RuFhP1P6M1Pla_S9cn1fxOz1urWw91h_dRFm000F__0m00)

 **Biểu đồ lớp trên đã mô tả các lớp, thuộc tính và quan hệ giữa các lớp trong hệ thống quản lý thẻ chấm công.**

 ## Hợp nhất kết quả phân tích
#### Ta có biểu đồ sau

![Diagram](https://www.planttext.com/api/plantuml/png/T9AnRiGW38PtdW9bh7H3rqmtj6FL3FS25AmxgW0HDiEfwfDrw2Fr5MeA8UXoNMA8Vt-sV_7pzNr4Kf6IcuMU5Q9yTiiShW3oGqXf3N-ySi31mC921vxuGjQ1Lj4WdqCq455yYafuQi8T0ogyKvygQTEkejnJKGxMPrLkbQYUbXZUGTF6cSgFcvOj_Pg7t98w8GK7iP1CqfGtMTIrxiUcKEgcd4fc0oWNqf-orhm0NOBvlxBazzCrkuV7GHuESdWODaj6UL6ubt3eF1xb6yp1d_4KxjBAvWNLo1sgrVIWUyBLuL7oNlRimR2mqBjsKx6JLJfuKjRZZIQJgfjbgFMs5rJJHfcGdumuWZVyK7y1003__mC0)

**Giải Thích biểu đồ:**
- **Employee:** Giữ vai trò trung tâm, liên kết với cả Timecard và Order, thể hiện việc nhân viên vừa làm việc, vừa có thể thực hiện các giao dịch mua hàng.
- **Timecard:** Liên quan đến công việc của nhân viên, bao gồm thông tin về giờ làm, dự án.
- **Order:** Liên quan đến hoạt động mua hàng của nhân viên, bao gồm thông tin về sản phẩm, phương thức thanh toán.
- **Payment:** Mô tả thông tin về một lần thanh toán, liên kết với Order.
- **PaymentMethod:** Định nghĩa các phương thức thanh toán khác nhau.
- **Department:** Lưu trữ thông tin về phòng ban mà nhân viên thuộc về.
- **Project:** Lưu trữ thông tin về dự án mà nhân viên tham gia.

 ### Các Hành Vi Chính Trong Kết Quả Phân Tích
 
- **Quản lý thông tin nhân viên:** Thêm, sửa, xóa thông tin nhân viên.
- **Quản lý thẻ chấm công:** Xem, cập nhật, tạo báo cáo về thẻ chấm công.
- **Quản lý đơn hàng:** Tạo đơn hàng, xem trạng thái đơn hàng, thực hiện thanh toán.
- **Quản lý sản phẩm:** Quản lý danh sách sản phẩm, cập nhật giá cả.
- **Quản lý phương thức thanh toán:** Cấu hình các phương thức thanh toán.

