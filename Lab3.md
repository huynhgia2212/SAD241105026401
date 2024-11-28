### Lab 3. Identify design elements
#### 1. Subsystem context diagrams
**1.1  Biểu đồ ngữ cảnh của hệ thống con BankSystem.**

![Diagram](https://www.planttext.com/api/plantuml/png/P9112eCm44NtEKMM2bNQRH2HTkMkq1EaCTAWJa8oGdEsBdgaNg49Oj5qDJFC-_D_ydcz6uVSuZoDn8IgX38Sa5wvjteSBnemLcbfLObbgEiTsPuv33VlK4w1KO3Izbp8XDf1RhwxfJTMFtr09Q127rt5GufXdQEgXLxRYQFIGCX_hABU9c3Kpa3DGcKvsOOh0hebEscqKvZnrPNz_0yql4D7cAKPSfASN3MKqMDPdj9r8byfGXe9NVZrBm000F__0m00)

**Mô tả Hệ thống Con BankSystem và Interface của nó**

**Hệ thống con BankSystem là gì?**

- Hệ thống con BankSystem là một phần mềm chuyên dụng, chịu trách nhiệm quản lý các hoạt động liên quan đến ngân hàng, như:

- Quản lý tài khoản: Tạo, cập nhật, xóa tài khoản khách hàng.
- Quản lý giao dịch: Ghi nhận các giao dịch gửi tiền, rút tiền, chuyển khoản.
- Tính toán lãi: Tính toán lãi suất cho các loại hình tài khoản khác nhau.
- Bảo mật thông tin: Bảo vệ thông tin khách hàng và các giao dịch.

**Interface của hệ thống con BankSystem**

- Interface của BankSystem là một tập hợp các phương thức, hàm hoặc lệnh mà các hệ thống khác có thể gọi để tương tác với BankSystem. Nó giống như một "cổng vào" để truy cập vào các chức năng của hệ thống.

**Các phương thức điển hình trong interface của BankSystem:**

- Tạo tài khoản: createAccount(accountNumber, customerName, initialBalance)
- Rút tiền: withdraw(accountNumber, amount)
- Gửi tiền: deposit(accountNumber, amount)
- Chuyển khoản: transfer(fromAccount, toAccount, amount)
- Kiểm tra số dư: getBalance(accountNumber)
- Tính lãi: calculateInterest(accountNumber)

 **1.2 Biểu đồ ngữ cảnh của hệ thống con PrintService:**

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
  

**1.3 Biểu đồ ngữ cảnh của hệ thống con ProjectManagementDatabase:**

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

#### **2.Analysis class to design element map**

### Ánh xạ các lớp phân tích đến các phần tử thiết kế.

| **Analysis Class**             | **Design Element**              |
|--------------------------------|---------------------------------|
| **LoginForm**                  | **LoginForm**                   |
| **MaintainTimecardForm**       | **MainEmployeeForm**            |
|                                | **TimecardForm**                |
|                                |  **MainApplicationForm**        |
| **TimecardController**         | **TimecardController**          |
| **SystemClockInterface**       | **SystemClockInterface**        |
| **PayrollController**          | **PayrollController**           |
| **Paycheck**                   | **Paycheck**                    |
| **PaymentInstruction**         | **PaymentInstruction**          |
| **Employee**                   | **Employee**                    |
| **IEmployeeRepository**        | **IEmployeeRepository**         |
| **IPaymentRepository**         | **IPaymentRepository**          |
| **BankSystem**                 | **BankSystem**                  |
| **IBankSystem**                | **IBankSystem**                 |
| **ProjectManagementDatabase**  | **ProjectManagementDatabase**   |
| **IProjectDatabase**           | **IProjectDatabase**            |
| **ProjectData**                | **ProjectData**                 |

#### **3. Design element to owning package map**

###  Ánh xạ các phần tử thiết kế vào các gói


| **Design Element**        | **"Owning" Package**                        |
|---------------------------|--------------------------------------------|
| **UserInterface**          | Middleware::Presentation::GUI Framework    |
| **PayrollController**      | Applications::Payroll::BusinessLogic       |
| **TimecardController**     | Applications::Payroll::BusinessLogic       |
| **EmployeeRepository**     | DataAccess::Employee::Repository           |
| **PaymentRepository**      | DataAccess::Payment::Repository            |
| **Database**               | DataAccess::Database::Connection           |
| **Paycheck**               | BusinessServices::Payroll::Artifacts       |
| **PaymentInstruction**     | BusinessServices::Payroll::Artifacts       |
| **IEmployeeRepository**    | Interfaces::Employee::RepositoryInterface  |
| **IPaymentRepository**     | Interfaces::Payment::RepositoryInterface   |
| **IBankSystem**            | Interfaces::Bank::SystemInterface          |
| **IProjectDatabase**       | Interfaces::Project::DatabaseInterface     |
| **BankSystem**             | Subsystems::Bank::PaymentProcessing        |
| **ProjectManagementDatabase** | Subsystems::Project::DatabaseManagement |
| **ProjectData**            | BusinessServices::Project::DataArtifacts   |


#### **4. Architectural layers and their dependencies**
### Biểu đồ mô tả các layers trong hệ thống và quan hệ giữa chúng. 

![PlanText](https://www.planttext.com/api/plantuml/png/X59BJiCm4Dtx54Cth7g1Bb1_4Pk0AW8769nfCNNioEDKYe2JiU18N04xAKb_KRsnv9dtbN-_VwRiqVcgqE8cfxKo14_9uddsU9yc83Ko2t4BotQYiIR7eaIvnGt1QEM8oNZqoXf8ut047mB2wJbMM3khzS8Q7szoualq3FEA0p4pf7QZv227KyPdv7PAqibeZcQRrUofECFOTvB-0KqGAeBB9NfyHQOZ_VW8CoaR2vV5awBKjgPJuP2BjIeZMzUF8zrqmM-gP76M7CRZpxkZC3215wR1rJxSbSN1i1tkKBIt4V0JoCZa37bimbjneDdi_SSFYq4b5aKCPMj33EjUmEvK7g4jfD6xXjztl0_HGPLPss0L96fPXSP9J4E4-8N_0000__y30000")
           
   
