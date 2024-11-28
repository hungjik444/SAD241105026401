Mô tả hệ thống con trong Payroll System
BankSystem:

Mô tả: Đây là hệ thống ngân hàng để xử lý các giao dịch chuyển khoản trực tiếp cho nhân viên. Payroll System gửi thông tin thanh toán qua BankSystem để thực hiện chuyển tiền vào tài khoản của nhân viên.
Interface:
Input: Dữ liệu giao dịch bao gồm số tài khoản, số tiền, ngày giao dịch.
Output: Xác nhận giao dịch thành công hoặc thất bại.
PrintService:

Mô tả: Xử lý việc in phiếu lương cho nhân viên nhận lương qua phương thức "nhận trực tiếp" hoặc "qua bưu điện".
Interface:
Input: Dữ liệu phiếu lương bao gồm tên nhân viên, số tiền, ngày in.
Output: Xác nhận in thành công hoặc thất bại.
ProjectManagementDatabase:

Mô tả: Đây là cơ sở dữ liệu dự án để quản lý charge numbers, liên kết thông tin dự án với giờ làm việc của nhân viên.
Interface:
Input: Yêu cầu truy vấn charge numbers.
Output: Danh sách charge numbers, trạng thái dự án.

Biểu đồ ngữ cảnh: BankSystem
![PlantText](https://www.planttext.com/api/plantuml/png/L5113e903Bpt5GrtFi31g8bt8twWWSOGTxkuBGTYV9a7d-GNt4M9qDjqfZEJlf-lhHf56xo3o8sHN1pZaSOOdAj7DVPu1qpJ1Dy7OJ4izYJNBrSWAVuXF02eiH2n-5dWhlMTT6gHqdgIJvjPTl2z2oFpnCm0O5sWB3UB4AomPcbpIP_hdFWsi9h2Gf8lrXvLqjaG1S-HH5Dw5mHh8niKjiakF-03003__mC0)

Giải thích:
Actor liên quan:
Payroll System là hệ thống chính giao tiếp với BankSystem.
BankSystem xử lý các yêu cầu thanh toán được gửi từ Payroll System.
Dòng dữ liệu:
Payroll System gửi thông tin thanh toán tới BankSystem.
BankSystem phản hồi trạng thái giao dịch (thành công hoặc thất bại).

Biểu đồ ngữ cảnh: PrintService
![PlantText](https://www.planttext.com/api/plantuml/png/L91D2i8m44RtSugX-rwW2wc8-s9E4D9H0lcfawbGn9Evy4XUmPXQCBFBu_lU37a_NtqIpJ9x1qn6TBWuma4l79rJInBoU0VCOwAVOg0Ws0niWoZYcpNKe4xu3-01e8r4phbLW_lHss2JiCwu50hPOaS_kRZGgjeU0FKHRRkhrc27YiAuCZpHTQOa2Qf8wLIM3Wynd2txNq-9bZb1dqtV7u0F0000__y30000)
Giải thích:
Actor liên quan:
Payroll System gửi yêu cầu in phiếu lương đến PrintService.
PrintService xác nhận hoặc báo lỗi nếu in thất bại.
Dòng dữ liệu:
Yêu cầu in bao gồm dữ liệu nhân viên, ngày in, và thông tin lương.
Phản hồi xác nhận hoặc báo lỗi in.

Biểu đồ ngữ cảnh: ProjectManagementDatabase
![PlantText](https://www.planttext.com/api/plantuml/png/N8zD2i9034RtEKNelXVeGWhgibBj2T8QAZ8_9PDP3EB9N7Wah-2e55g_tHVUIyZhyQo3acYq1eG79JSQnfQIU6Ew59GjtW1p1cydxzWf5gtuQsORSZIopQCTAVKKk40As3PpXJi03Ue5YxsTZ4_y8-O2i3vKbfk5ZHKU8ql2xOLaP3n4sxC4M11VORMYmXDh5FSlrUpEdnzptW000F__0m00)
Giải thích:
Actor liên quan:
Payroll System truy vấn dữ liệu từ ProjectManagementDatabase để lấy thông tin charge numbers.
Nhân viên có thể nhập giờ làm việc dựa trên charge numbers này.
Dòng dữ liệu:
Payroll System gửi yêu cầu truy vấn.
Database trả về danh sách charge numbers và thông tin liên quan.
