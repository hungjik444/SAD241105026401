
# Các hệ thống con trong payroll system
## 1. Authentication & Authorization System (Hệ thống Xác thực và Phân quyền)
### Chức năng chính:
#### Xác thực người dùng dựa trên tên đăng nhập và mật khẩu.
#### Phân quyền truy cập (nhân viên nhân sự, quản trị viên lương, hoặc quản lý).
#### Hỗ trợ chức năng "Quên mật khẩu" hoặc thay đổi mật khẩu.
### Tương tác với hệ thống khác:
#### Kết nối với User Management System để quản lý tài khoản và vai trò.
#### Bảo vệ các hệ thống con khác bằng cách kiểm tra quyền trước khi thực hiện chức năng.
## 2. User Management System (Hệ thống Quản lý Người dùng)
### Chức năng chính:
#### Quản lý thông tin người dùng (họ tên, email, vai trò, trạng thái tài khoản).
#### Tạo mới, chỉnh sửa, hoặc khóa tài khoản người dùng.
#### Cung cấp giao diện để quản trị viên quản lý người dùng.
### Tương tác với hệ thống khác:
#### Hỗ trợ Authentication & Authorization System trong việc xác định quyền truy cập.
#### Cung cấp thông tin cơ bản của người dùng cho các hệ thống báo cáo.
## 3. Timecard Management System (Hệ thống Quản lý Bảng Chấm Công)
### Chức năng chính:
#### Lưu trữ và quản lý thông tin giờ làm việc, ngày nghỉ, làm thêm giờ, và các thông tin liên quan của từng nhân viên.
#### Cho phép nhân viên nhân sự chỉnh sửa bảng chấm công.
#### Hỗ trợ nhập liệu tự động qua quét mã QR hoặc dữ liệu đồng bộ từ thiết bị chấm công.
### Tương tác với hệ thống khác:
#### Cung cấp dữ liệu đầu vào cho Payroll Calculation System.
#### Tích hợp với Employee Management System để đảm bảo thông tin nhân viên chính xác.
## 4. Payroll Calculation System (Hệ thống Tính Lương)
### Chức năng chính:
#### Tính toán lương dựa trên thông tin bảng chấm công, lương cơ bản, phụ cấp, và khấu trừ (thuế, bảo hiểm, v.v.).
#### Tự động xử lý các quy tắc tính toán theo quy định pháp luật và chính sách công ty.
#### Lưu trữ và hiển thị kết quả tính toán cho từng kỳ lương.
### Tương tác với hệ thống khác:
#### Sử dụng dữ liệu từ Timecard Management System và Employee Management System.
#### Kết nối với Banking System để chuyển khoản lương.
#### Tích hợp với Reporting System để xuất báo cáo.
## 5. Banking System Integration (Hệ thống Tích hợp Ngân hàng)
### Chức năng chính:
#### Gửi yêu cầu chuyển khoản lương tới hệ thống ngân hàng.
#### Xử lý và theo dõi trạng thái giao dịch (thành công, thất bại, hoặc chờ xử lý).
#### Ghi nhận chi tiết giao dịch ngân hàng để hỗ trợ kiểm tra và đối soát.
### Tương tác với hệ thống khác:
#### Nhận dữ liệu từ Payroll Calculation System.
#### Cung cấp kết quả giao dịch cho Reporting System để lập báo cáo tài chính.
## 6. Paycheck Generation System (Hệ thống Tạo và In Phiếu Lương)
### Chức năng chính:
#### Tạo phiếu lương cá nhân cho từng nhân viên từ kết quả bảng lương.
#### Tùy chỉnh định dạng phiếu lương (logo công ty, thông tin liên hệ, mã QR, v.v.).
#### Hỗ trợ in phiếu lương hoặc xuất file PDF để gửi qua email.
### Tương tác với hệ thống khác:
#### Lấy dữ liệu từ Payroll Calculation System.
#### Kết nối với Employee Management System để điền thông tin cá nhân vào phiếu lương.
## 7. Employee Management System (Hệ thống Quản lý Nhân viên)
### Chức năng chính:
#### Lưu trữ thông tin cá nhân của nhân viên (họ tên, số tài khoản ngân hàng, địa chỉ, phòng ban, v.v.).
#### Theo dõi trạng thái làm việc (đang làm việc, nghỉ phép, hoặc nghỉ việc).
#### Quản lý thông tin hợp đồng lao động và mức lương cơ bản.
### Tương tác với hệ thống khác:
#### Cung cấp dữ liệu cho Timecard Management System và Payroll Calculation System.
#### Kết nối với Paycheck Generation System để hiển thị thông tin trên phiếu lương.
## 8. Reporting System (Hệ thống Báo cáo)
### Chức năng chính:
#### Tạo báo cáo chi tiết hoặc tổng hợp về lương, giao dịch ngân hàng, và bảng chấm công.
#### Hỗ trợ xuất báo cáo ở các định dạng khác nhau (PDF, Excel, v.v.).
#### Tích hợp biểu đồ trực quan để quản lý theo dõi hiệu quả.
### Tương tác với hệ thống khác:
#### Thu thập dữ liệu từ Payroll Calculation System, Banking System, và Timecard Management System.
#### Cung cấp thông tin báo cáo cho các cấp quản lý.
## 9. Audit & Logging System (Hệ thống Kiểm tra và Ghi nhật ký)
### Chức năng chính:
#### Theo dõi và ghi lại tất cả các hoạt động trong hệ thống để đảm bảo tính minh bạch.
#### Hỗ trợ kiểm tra các thay đổi liên quan đến bảng chấm công, lương, và giao dịch ngân hàng.
#### Cảnh báo về các hành vi bất thường.
### Tương tác với hệ thống khác:
#### Kết nối với tất cả các hệ thống con để thu thập và lưu trữ nhật ký hoạt động.
## 10. Notification System (Hệ thống Thông báo)
### Chức năng chính:
#### Gửi thông báo tự động qua email hoặc tin nhắn khi có các sự kiện quan trọng (chạy bảng lương xong, giao dịch ngân hàng thất bại, v.v.).
#### Nhắc nhở các công việc cần thực hiện (chạy bảng lương, duyệt bảng chấm công, v.v.).
### Tương tác với hệ thống khác:
#### Nhận sự kiện từ Payroll Calculation System, Banking System, và các hệ thống con khác.
#### Cung cấp thông tin cập nhật kịp thời cho người dùng.
### Biểu đồ :
![PlantText](https://www.planttext.com/api/plantuml/png/T9EnRXGn48PxFyKe1LrUO0kKS487Ke8Y4YGaH65yPctjhhtPyo8jY09HK51HKXu88KKwaIBLhg8KY_8UVeAyGZnsxBiSt1KhtVpVxvdvlNipNEtD3MrCMvMafgoWEOUT8zerkYpXk9iRNkt01mBkzsg_DO8h8narKYju05ZGZNmV_WVwDT2v5uBdnPmtS4YLExTotdK8fSEyCW4yaHLdj9bjWQCSu3ZWX9QiBVzfVoS7zX5LXLJvdGvFbU5vuosUHJaToWHd1Kovuit_3lLoW1zNTQaxphUC6-K0F-UrRing28-aOWnt9etBz43d-GRffK0zqqQ-ZHUmXgpNoKT2y09WT_TX2XaoE1BZ3mMdRMU7Jugal96AUMOmQLrlPljVDSpiy0TAQOSlBJ3XIXMmySBD6sbqOdpEDhN3Ka8tdhLe_eq6xFDPGI6qxN-gUwQKT0Odjbzeg8Mq_LKBvVNvzMAZmogy35wsRWm3RqRdOVY81Z_69Zsn_R86vKPV6Z2Dw-JAHemB2Rca6XVyoWH9qw0_tMi6JwHVm0Y7eUq2tLAv0p77Tt8yKoJXw4sHPd20AXHkARFDkfeKlVSkDkR9C3dXroNX_K1qtr_KLCYuMZ5U0gQyCF3tcns-kppsk9hX9qt8BG000F__0m00)
