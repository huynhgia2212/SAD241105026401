### Lab 3. Identify design elements
#### 1. Subsystem context diagrams
- **Biểu đồ ngữ cảnh của hệ thống con PrintService:**

  ![Diagram](https://www.planttext.com/api/plantuml/png/R91D2eCm48NtESKiMsWl82A2tRWBv0IffX0m6PcCfJbR5prIhz34gb3gQdxUl6-6UJzVTM1DFBb1Z2dQpexQCqYodXlqJ3WCXa07aCtFH3kFA4DtsvcijrBz8rGCRDniLr2M4APh-BP6maU4gXB6i-K85-mcb_Ardks6Mdz3SfejUY5a0-SgBogIFSdGhwRKozAc7FJAApRo2HWNQh63FuhCI93jagNUkQGslayl-m000F__0m00)

  **Mô tả Hệ thống Con PrintService và Interface của nó**
**Hệ thống Con PrintService là gì?**
- Hệ thống con PrintService là một phần của một hệ thống lớn hơn, có chức năng cụ thể là quản lý các hoạt động in ấn. Nó đóng vai trò như một trung gian giữa ứng dụng cần in và máy in vật lý.

**Chức năng chính:**

- Tiếp nhận yêu cầu in: Nhận các yêu cầu in từ các ứng dụng khác nhau trong hệ thống.
- Xử lý yêu cầu: Phân tích yêu cầu, chuyển đổi dữ liệu cần in sang định dạng phù hợp với máy in.
- Gửi lệnh in: Gửi lệnh in đến máy in và quản lý quá trình in.
- Theo dõi trạng thái: Theo dõi trạng thái của quá trình in và thông báo kết quả cho ứng dụng.
**Interface của Hệ thống Con PrintService**
- Interface của PrintService định nghĩa một hợp đồng (contract) giữa PrintService và các thành phần khác trong hệ thống. Nó xác định các phương thức mà các thành phần khác có thể gọi để tương tác với PrintService.

**Các phương thức điển hình trong interface của PrintService:**

- print(document): Phương thức này nhận một đối tượng document (tài liệu) và thực hiện in tài liệu đó.
- setPrinter(printer): Thiết lập máy in mặc định cho các yêu cầu in tiếp theo.
- getPrinters(): Trả về danh sách các máy in có sẵn trong hệ thống.
- getPrintStatus(): Trả về trạng thái hiện tại của quá trình in.
- cancelPrintJob(): Hủy bỏ một công việc in đang thực hiện.

 - **Biểu đồ ngữ cảnh của hệ thống con ProjectManagementDatabase:**

   ![Diagram](https://www.planttext.com/api/plantuml/png/Z951QiD034NtSmej6sWkO8m999j03LwaPAqu8ftMdZ4ZXTPdwo97oXKgEHwQKYXTZRxqz2Knry_BYWMJdFlE3VhwrWyO19eKNwcL6WEUgASWwnWanQwZ1CZGrEiV-FONlq710p8PlMtgpT_kzxJ2K9R0vmEFBDJ3aEB725Nb5FGovkuiTyXlENvcIZckVKSiCP0p0fRBwZi51Hnfe71aYC4vFGUqR7iMq2P28PjgK-3Tomk8Eh2pkd5tsBpBNY6RmWyuPugyvkEjkO0dpr8QL2tSP6HEyobPJ_jdCHsMnV-lMMcWt_a5003__mC0)
   
