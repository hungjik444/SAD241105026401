# Phân tích các ca sử dụng trong Payroll System
## Danh sách các ca sử dụng
### Login: Đăng nhập hệ thống.
### Maintain Employee Information: Quản lý thông tin nhân viên (thêm, sửa, xóa).
### Maintain Purchase Order: Quản lý đơn hàng mua của nhân viên nhận hoa hồng.
### Maintain Timecard: Quản lý thẻ chấm công của nhân viên.
### Run Payroll: Chạy quy trình tính lương.
### Create Administrative Report: Tạo báo cáo hành chính.
### Create Employee Report: Nhân viên tạo báo cáo của riêng họ.
### Select Payment Method: Nhân viên chọn phương thức thanh toán.
![PlantText](https://www.planttext.com/api/plantuml/png/R9AzRi8m4CTtFuMLdO7lJeWATQW40a7PifoIQx7a3tI-LCgpTU2H-WerYOCXPV1mF_zqvx_jtv_BqZCGLqOBADYHV3DdxMh4M6OxgCbfBLzBewpoJ11m9i6t96g7sZCQ8IgF1NYKsTfzATjenzKmuGqeos7TnkJstNuwCi3ATVxeYR-hg3W5bDijbKZH73ynFvG9YCgeJ9AohqAVDaxSdARD5I4mtiTKts7Q7i-EEEgpVtgAyI3EatX0ZGLVvngqdDiDyibrXtiHekiW1uD5SrSzCEw3IH_C-o1qRMBSMjvNeuTg9aJxTB6UYYNQyleR_W000F__0m00)
## Mô tả chi tiết từng ca sử dụng
## 1. Login
### Mô tả: Người dùng đăng nhập vào hệ thống.
### Tác nhân: Nhân viên, Payroll Administrator.
### Luồng chính:
### Người dùng nhập tên và mật khẩu.
### Hệ thống xác thực và đăng nhập người dùng.
### Luồng phụ:
### Tên/mật khẩu không hợp lệ: Hiển thị thông báo lỗi.
### Tiền điều kiện: Hệ thống đang ở màn hình đăng nhập.
### Hậu điều kiện: Người dùng đăng nhập thành công hoặc hệ thống giữ nguyên trạng thái.
## 2. Maintain Employee Information
### Mô tả: Payroll Administrator quản lý thông tin nhân viên (thêm, sửa, xóa).
### Tác nhân: Payroll Administrator.
### Luồng chính:
### Payroll Administrator chọn hành động: thêm, sửa, hoặc xóa nhân viên.
### Hệ thống thực hiện hành động tương ứng.
### Luồng phụ:
### Không tìm thấy thông tin nhân viên: Hiển thị thông báo lỗi.
### Tiền điều kiện: Payroll Administrator đã đăng nhập.
### Hậu điều kiện: Thông tin nhân viên được cập nhật.
## 3. Maintain Purchase Order
### Mô tả: Nhân viên nhận hoa hồng quản lý đơn hàng mua.
### Tác nhân: Nhân viên nhận hoa hồng.
### Luồng chính:
### Nhân viên chọn hành động: thêm, sửa, hoặc xóa đơn hàng.
### Hệ thống thực hiện hành động tương ứng.
### Luồng phụ:
### Đơn hàng đã đóng: Không thể chỉnh sửa hoặc xóa.
### Đơn hàng không thuộc về nhân viên: Hiển thị thông báo lỗi.
### Tiền điều kiện: Nhân viên đã đăng nhập.
### Hậu điều kiện: Đơn hàng được cập nhật.
### 4. Maintain Timecard
### (Đã phân tích ở trên)

## 5. Run Payroll
### Mô tả: Chạy quy trình tính lương định kỳ.
### Tác nhân: Hệ thống.
### Luồng chính:
### Hệ thống tự động chạy vào các ngày thứ Sáu và ngày làm việc cuối tháng.
### Tính toán lương dựa trên thẻ chấm công, đơn hàng, và thông tin nhân viên.
### Tạo và gửi thanh toán (in hoặc chuyển khoản).
### Luồng phụ:
### Hệ thống ngân hàng không hoạt động: Tự động thử lại sau một khoảng thời gian.
### Nhân viên bị xóa: Tạo phiếu lương cuối cùng, sau đó xóa khỏi hệ thống.
### Tiền điều kiện: Thẻ chấm công và đơn hàng hợp lệ.
### Hậu điều kiện: Lương được thanh toán cho nhân viên đủ điều kiện.
## 6. Create Administrative Report
### Mô tả: Payroll Administrator tạo báo cáo quản trị.
### Tác nhân: Payroll Administrator.
### Luồng chính:
### Chọn loại báo cáo (giờ làm việc, tổng lương...).
### Nhập khoảng thời gian và danh sách nhân viên.
### Hệ thống tạo và hiển thị báo cáo.
### Luồng phụ:
### Dữ liệu không đủ hoặc không hợp lệ: Hiển thị thông báo lỗi.
### Tiền điều kiện: Payroll Administrator đã đăng nhập.
### Hậu điều kiện: Báo cáo được tạo.
## 7. Create Employee Report
### Mô tả: Nhân viên tự tạo báo cáo cá nhân.
### Tác nhân: Nhân viên.
### Luồng chính:
### Chọn loại báo cáo (giờ làm việc, lương YTD...).
### Nhập khoảng thời gian.
### Hệ thống tạo và hiển thị báo cáo.
### Luồng phụ:
### Dữ liệu không đủ: Hiển thị thông báo lỗi.
### Tiền điều kiện: Nhân viên đã đăng nhập.
### Hậu điều kiện: Báo cáo được tạo.
## 8. Select Payment Method
### Mô tả: Nhân viên chọn phương thức nhận lương.
### Tác nhân: Nhân viên.
### Luồng chính:
### Chọn phương thức thanh toán (nhận trực tiếp, chuyển khoản, qua bưu điện).
### Nhập thông tin bổ sung (địa chỉ, tài khoản ngân hàng).
### Hệ thống cập nhật thông tin.
### Luồng phụ:
### Không tìm thấy thông tin nhân viên: Hiển thị thông báo lỗi.
### Tiền điều kiện: Nhân viên đã đăng nhập.
### Hậu điều kiện: Phương thức thanh toán được cập nhật.

