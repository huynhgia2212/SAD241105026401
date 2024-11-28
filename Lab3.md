### Lab 3. Identify design elements
#### 1. Subsystem context diagrams
 **1.1 Biểu đồ ngữ cảnh của hệ thống con PrintService:**

  ![Diagram](https://www.planttext.com/api/plantuml/png/R91D2eCm48NtESKiMsWl82A2tRWBv0IffX0m6PcCfJbR5prIhz34gb3gQdxUl6-6UJzVTM1DFBb1Z2dQpexQCqYodXlqJ3WCXa07aCtFH3kFA4DtsvcijrBz8rGCRDniLr2M4APh-BP6maU4gXB6i-K85-mcb_Ardks6Mdz3SfejUY5a0-SgBogIFSdGhwRKozAc7FJAApRo2HWNQh63FuhCI93jagNUkQGslayl-m000F__0m00)

  **Mô tả Hệ thống Con PrintService và Interface của nó**
  
**Hệ thống Con PrintService là gì?**
- Hệ thống con PrintService là một phần của một hệ thống lớn hơn, có chức năng cụ thể là quản lý các hoạt động in ấn. 

**Chức năng chính:**

- Tiếp nhận yêu cầu in: Nhận các yêu cầu in từ các ứng dụng khác nhau trong hệ thống.
- Xử lý yêu cầu: Phân tích yêu cầu, chuyển đổi dữ liệu cần in sang định dạng phù hợp với máy in.
- Gửi lệnh in: Gửi lệnh in đến máy in và quản lý quá trình in.
- Theo dõi trạng thái: Theo dõi trạng thái của quá trình in và thông báo kết quả cho ứng dụng.
**Interface của Hệ thống Con PrintService**
- Interface của PrintService liên quan giữa PrintService và các thành phần khác trong hệ thống. Nó xác định các phương thức mà các thành phần khác có thể gọi để tương tác với PrintService.

**Các phương thức điển hình trong interface của PrintService:**

- Print(document): Phương thức này nhận một tài liệu và thực hiện in tài liệu đó.
- SetPrinter(printer): Thiết lập máy in mặc định cho các yêu cầu in tiếp theo.
- GetPrinters(): Trả về danh sách các máy in có sẵn trong hệ thống.
- GetPrintStatus(): Trả về trạng thái hiện tại của quá trình in.
- CancelPrintJob(): Hủy bỏ một công việc in đang thực hiện.
  

**1.2 Biểu đồ ngữ cảnh của hệ thống con ProjectManagementDatabase:**

   ![Diagram](https://www.planttext.com/api/plantuml/png/Z951QiD034NtSmej6sWkO8m999j03LwaPAqu8ftMdZ4ZXTPdwo97oXKgEHwQKYXTZRxqz2Knry_BYWMJdFlE3VhwrWyO19eKNwcL6WEUgASWwnWanQwZ1CZGrEiV-FONlq710p8PlMtgpT_kzxJ2K9R0vmEFBDJ3aEB725Nb5FGovkuiTyXlENvcIZckVKSiCP0p0fRBwZi51Hnfe71aYC4vFGUqR7iMq2P28PjgK-3Tomk8Eh2pkd5tsBpBNY6RmWyuPugyvkEjkO0dpr8QL2tSP6HEyobPJ_jdCHsMnV-lMMcWt_a5003__mC0)


**Mô tả Hệ thống Con ProjectManagementDatabase và Interface của nó**

**Hệ thống Con ProjectManagementDatabase là gì?**

- Hệ thống con ProjectManagementDatabase là một phần không thể thiếu trong các ứng dụng quản lý dự án. Nó chịu trách nhiệm lưu trữ, truy xuất và quản lý toàn bộ dữ liệu liên quan đến các dự án, công việc, tài nguyên trong dự án.

**Chức năng chính:**

- Lưu trữ thông tin dự án: Bao gồm tên dự án, mô tả, ngày bắt đầu, ngày kết thúc, ngân sách,...
- Quản lý công việc: Lưu trữ thông tin về các công việc con của dự án, mối quan hệ giữa các công việc, người phụ trách, tiến độ hoàn thành,...
- Quản lý tài nguyên: Theo dõi các tài nguyên được sử dụng trong dự án như nhân lực, thiết bị, vật liệu.
- Quản lý người dùng: Lưu trữ thông tin về các thành viên tham gia dự án, quyền truy cập,...
- Cung cấp các báo cáo: Tạo các báo cáo về tiến độ dự án, sử dụng tài nguyên, rủi ro,...
  
**Interface của Hệ thống Con ProjectManagementDatabase**

**Các phương thức điển hình:**

- Tạo dự án mới: Thêm một dự án mới vào cơ sở dữ liệu.
- Cập nhật thông tin dự án: Sửa đổi thông tin của một dự án đã tồn tại.
- Xóa dự án: Xóa một dự án khỏi cơ sở dữ liệu.
- Tìm kiếm dự án: Tìm kiếm các dự án dựa trên các tiêu chí nhất định (ví dụ: theo tên dự án, trạng thái, người quản lý).
- Thêm, cập nhật, xóa công việc: Thực hiện các thao tác tương tự đối với các công việc con của dự án.
- Phân công công việc: Gán một công việc cho một người dùng cụ thể.
- Theo dõi tiến độ: Cập nhật tiến độ hoàn thành của các công việc.
- Quản lý tài nguyên: Thêm, xóa, cập nhật thông tin về các tài nguyên được sử dụng trong dự án.
- Quản lý người dùng: Thêm, xóa, cập nhật thông tin về người dùng, cấp quyền truy cập.

  #### **2. Analysis class to design element map**
  **Ánh xạ các lớp phân tích của PrintService đến các phần tử thiết kế**

 - Lớp phân tích (PrintService): PrintJob/Printer/Document/PrintQueue/PrintController
  
 - Phần tử thiết kế: PrintJob/HPPrinter, EpsonPrinter/PDFDocument, WordDocument, ImageDocument/PriorityQueue/PrintController

**Ánh xạ các lớp phân tích của ProjectManagementDatabase đến các phần tử thiết kế**

- Lớp phân tích: Project/Task/User/Resource

- Phần tử thiết kế: Project/Task/User/Resource
           
   
