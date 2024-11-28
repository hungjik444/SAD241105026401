# Mô tả hệ thống con trong Payroll System
## BankSystem:

### Mô tả: Đây là hệ thống ngân hàng để xử lý các giao dịch chuyển khoản trực tiếp cho nhân viên. Payroll System gửi thông tin thanh toán qua BankSystem để thực hiện chuyển tiền vào tài khoản của nhân viên.
### Interface:
### Input: Dữ liệu giao dịch bao gồm số tài khoản, số tiền, ngày giao dịch.
### Output: Xác nhận giao dịch thành công hoặc thất bại.
## PrintService:

### Mô tả: Xử lý việc in phiếu lương cho nhân viên nhận lương qua phương thức "nhận trực tiếp" hoặc "qua bưu điện".
### Interface:
### Input: Dữ liệu phiếu lương bao gồm tên nhân viên, số tiền, ngày in.
### Output: Xác nhận in thành công hoặc thất bại.
## ProjectManagementDatabase:

### Mô tả: Đây là cơ sở dữ liệu dự án để quản lý charge numbers, liên kết thông tin dự án với giờ làm việc của nhân viên.
### Interface:
### Input: Yêu cầu truy vấn charge numbers.
### Output: Danh sách charge numbers, trạng thái dự án.

## Biểu đồ ngữ cảnh: BankSystem
![PlantText](https://www.planttext.com/api/plantuml/png/h5HBReCm4Drp2ejLkaWEWAegZTe5kqYSO68cgHKmQ3n6ZTgSh8iUgLUemIGnYIDrKIyGl7apy-PZVhw-buQ1sDPLqeBSmmv5MjYDEHZ6MgofUJ-auYCHxiWAZ14hqFl2MptiJqkDH6FMSAXHyqnfmsGbgqPdOWJp2_OmWF8DvJw8iKD-bhAncbTGWPOu0_-Pbvaec9JUESTUGAwt3TNGXmhy3UgoO73IUWdczEPTpWONecjKEVWTasDogJlNZBG5YQUArGaG-T_AXln_whvJvbJkgsR5LzEvJJcHomJQm81VUXhO2IMg3ccK4s50xGrbOpSLnaE_k4vded-EggS2X_AdNHp1gAQx6KkN83V6OdalsLKF9pblLYkmIKk4vsb4KaC7gWA7nIZ3b89zcS-VOdF9H3fk3veqmlTjSYn2jgHlETVLUIefxFg0uSO-VYuMuSLrJ5MtrN0T77Nfxat_0_W5003__mC0)

## Giải thích:
### Actor liên quan:
### Payroll System là hệ thống chính giao tiếp với BankSystem.
### BankSystem xử lý các yêu cầu thanh toán được gửi từ Payroll System.
### Dòng dữ liệu:
### Payroll System gửi thông tin thanh toán tới BankSystem.
### BankSystem phản hồi trạng thái giao dịch (thành công hoặc thất bại).

## Biểu đồ ngữ cảnh: PrintService
![PlantText](https://www.planttext.com/api/plantuml/png/Z9DDRi8m48NtEOML5KWD1uYgYWLTP8UK4mpEG2qSEx8d4QZbP5rm9AvGvyUDGr2fLoFFyyoNDvFRztLj2GpLfOmgu4Su88lpUcVFbh1aMwDFvvXzHimTBi5QToKKvMWQmN58zATg4nlDwn8LBOeXI9c_UkaLQDA-1ffboXejYg06_q1-x3iGK6qNmvEiI5bEBZuiVT2zkaINQEH-LoJe3jTtdw1wkB5ioA1TnnPybjbhKy8yaIH986f0YW88Vvrmn3kj9O8QaE_DH3FtCVpa86SxLnuafEP0GgidSCzc54vawctMCks1exTN-0kM_NCbOFDW9xJQ_h4L7SEaV9AyZJDDMLmPpT5QjF5SvzrrihfJJ4bVlrQhwJexeIWhYMrn9r-ZAjeVumS00F__0m00)
### Giải thích:
### Actor liên quan:
### Payroll System gửi yêu cầu in phiếu lương đến PrintService.
### PrintService xác nhận hoặc báo lỗi nếu in thất bại.
### Dòng dữ liệu:
### Yêu cầu in bao gồm dữ liệu nhân viên, ngày in, và thông tin lương.
### Phản hồi xác nhận hoặc báo lỗi in.

## Biểu đồ ngữ cảnh: ProjectManagementDatabase
![PlantText](https://www.planttext.com/api/plantuml/png/h5D1JiCm4Bpd5LPEhOJxW0YX7i8X1n1INx29jv71TY9xNQYWB-F0a_W2Jfg8H0u8fFfaxSxCUcVNd-yVMqTWoMkLj50zGOqitVdI7HsXPW-sUJccx3LXuLGAdEj2ZrZH7PY0rMWe1u8I70weywcH1c1Xzisg7UuYOpkoqjJhR1Jgw1EYRmKGJd8nzue52Cm4WjoXaQBNEIMdvBkNMqEIbbleYBD7HvNYt3reNCYMNeIECoOQNogS98Avv5t4u9mlcfKZWLHkjLweCNTc01fyplzkHc48xHug7FsGOu0L4u5BJBCl_FEkS7up6qF6Kej12m_eql_nphu4LjJ2zTjcyyk-1gxKhUg3WRv58xfly0K00F__0m00)
### Giải thích:
### Actor liên quan:
### Payroll System truy vấn dữ liệu từ ProjectManagementDatabase để lấy thông tin charge numbers.
### Nhân viên có thể nhập giờ làm việc dựa trên charge numbers này.
### Dòng dữ liệu:
### Payroll System gửi yêu cầu truy vấn.
### Database trả về danh sách charge numbers và thông tin liên quan.
## 2.Analysis class to design element map

 ánh xạ các lớp phân tích đến các phần tử thiết kế

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



---

## 3.Design element to owning package map

ánh xạ các phần tử thiết kế vào các gói

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
