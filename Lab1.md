# 1. Phân tích kiến trúc
## a. Đề xuất kiến trúc
### Kiến trúc ba lớp (3-Tier Architecture): Bao gồm Presentation Layer, Application Layer, Database Layer, và bổ sung thêm một lớp Security Layer để xử lý các yêu cầu bảo mật.
### Giải thích lý do lựa chọn:
#### Phù hợp với tính chất hệ thống Payroll System, đáp ứng yêu cầu phân quyền bảo mật cao.
#### Kiến trúc ba lớp đảm bảo khả năng mở rộng, dễ bảo trì và nâng cấp khi cần thiết.
### Ý nghĩa từng thành phần trong kiến trúc:
#### Presentation Layer: Xử lý giao diện và tương tác người dùng.
#### Application Layer: Thực hiện xử lý nghiệp vụ chính của hệ thống như tính toán lương, ghi nhận giờ làm và đơn hàng.
#### Database Layer: Quản lý dữ liệu nhân viên, thẻ thời gian, đơn đặt hàng và phiếu lương.
#### Security Layer: Đảm bảo chỉ những người được phép mới có thể truy cập các dữ liệu nhạy cảm.
## b. Biểu đồ Package
![PlantText](https://www.planttext.com/api/plantuml/png/T9112i8m44NtESNGlHV8Gbhq08M2-p6E4anZo4o58fxCXKVo2YOY14FTpdky3_DwF5iMZ3ADJWKqPpmHD7qa9Yyezk8Rk2a0TLS5To4uQ_xHBGhkaMa13MIcQ6Kkg9fQhQkwXWqw1mF5gpN4wfTclSnfw4no6F9fmIph6dOKxN66dk9ecPEIqeNNtG-XRrwrv0_vNMy0003__mC0)

# 2. Cơ chế phân tích
## Các cơ chế cần giải quyết
### Cơ chế phân quyền: Đảm bảo rằng chỉ những người dùng có quyền hạn thích hợp mới có thể thực hiện các thao tác nhất định.
### Cơ chế bảo mật dữ liệu: Đảm bảo tính riêng tư và toàn vẹn của dữ liệu về lương và giờ làm.
### Cơ chế tính lương tự động: Hệ thống cần tự động tính toán lương vào các ngày nhất định dựa trên thông tin thẻ thời gian và đơn hàng của nhân viên.
### Cơ chế ghi nhận thời gian làm việc: Cung cấp phương thức để nhân viên ghi lại giờ làm việc hàng tuần.

# 3. Phân tích ca sử dụng "Payment"
## a. Xác định các lớp phân tích
### Lớp "Employee": Lưu thông tin nhân viên, bao gồm tên, ID, loại lương (theo giờ, cố định, hoa hồng).
### Lớp "Payroll Administrator": Chịu trách nhiệm duyệt và quản lý thanh toán cho nhân viên.
### Lớp "Payment": Thực hiện tính toán lương cho từng nhân viên dựa trên thông tin thẻ thời gian và đơn hàng.
## b. Biểu đồ Sequence cho ca sử dụng "Payment"
### Mô tả quá trình tính toán và tạo phiếu lương cho nhân viên:
#### "Payroll Administrator" khởi tạo quá trình thanh toán.
#### Hệ thống truy xuất dữ liệu giờ làm việc và đơn đặt hàng.
#### Hệ thống tính toán lương và tạo phiếu thanh toán cho từng nhân viên.
## c. Nhiệm vụ và thuộc tính của từng lớp phân tích
### Employee: Thuộc tính name, id, salaryType. Nhiệm vụ là lưu trữ và cung cấp thông tin cơ bản của nhân viên.
### Payroll Administrator: Thuộc tính adminId, role. Nhiệm vụ là quản lý và duyệt quá trình thanh toán.
### Payment: Thuộc tính totalPayment, paymentDate. Nhiệm vụ là thực hiện tính toán lương dựa trên giờ làm và đơn đặt hàng.
## d. Biểu đồ lớp
![PlantText](https://www.planttext.com/api/plantuml/png/Z5B1IiGm4BttAq9FAkoYrnvaHGNt80ekU1wJOJUOPCeaAHJnoppuIVw2oLhRJLd47Xeoxysyzv9yVNokV00EqPfA6l1UtDhMK8yetYgHleNGgX5FWRNR3WK75cSb3mQut_Jj76YXj-Z2FOOTbNE4a61aD13myOTqSje8HV75OFLU3MuIn6JCbRBQQHyO0l7e379rFH_RCadqVkZCGplIgXYPrSOfWyNrF2POYYwCbWhoJNBTYFmVHBVeaCiefUf6MvJ0QfJTKMJ_JFoAILYxC9IfGmw9UvVX2JWuhTopHxD8ngTaaUKEF3wmmkcKAE_-aowd2DTahVPUaoklOtmMzKKj5elBj2wNP_MKgn5rzEZh8yppFRDqzmSzhRztb5YC4dMNcKVVmipEGQC51zlSjqAdqll-1W00__y30000)

# 4. Phân tích ca sử dụng "Maintain Timecard"
## a. Xác định các lớp phân tích
### Lớp "Employee": Lưu trữ thông tin nhân viên như trong ca sử dụng Payment.
### Lớp "Timecard": Ghi lại thông tin thẻ thời gian làm việc của từng nhân viên.
### Lớp "Project": Lưu trữ các mã dự án để nhân viên ghi nhận giờ làm việc theo từng dự án.
## b. Biểu đồ Sequence cho ca sử dụng "Maintain Timecard"
### Biểu đồ mô tả quá trình nhân viên ghi nhận giờ làm
#### "Employee" đăng nhập vào hệ thống.
#### Hệ thống hiển thị danh sách mã dự án để chọn và nhập số giờ làm việc.
#### "Employee" nhập giờ làm việc vào thẻ thời gian cho từng dự án cụ thể.
## c. Nhiệm vụ và thuộc tính của từng lớp phân tích
### Employee: Như mô tả trong ca sử dụng "Payment".
### Timecard: Thuộc tính date, hoursWorked, projectId. Nhiệm vụ là ghi lại số giờ làm việc của nhân viên.
### Project: Thuộc tính projectId, projectName. Nhiệm vụ là cung cấp mã dự án để nhân viên ghi nhận giờ làm.
## d. Biểu đồ lớp 
![PlantText](https://www.planttext.com/api/plantuml/png/R971IWCn48RlUOeXfrRSWjSzI0yLz2A21SznCsodJJObcRM8zCbww2Fv2iww8MAtEIJmvS_7pEJxT5ucDf5xxrJZJ4hmuFSkV2B2bm9P5P2juPKZTMq6dV7u3m6uqAx9usnUmqSWguugsmRQc6YBZJDukhHQms9ToPx19lGnlOMuGubInndlOzXYmnVl0OorZyEBsIHmEwf-9PC2NyPqgU-wll3dQUyjyWhPa4j3-_bA_6MG-av3LTtBkLZSwB-HrA1J_-w9arO5vj2OrwKyoKgreI6PZuK3yKQh9NPs-BSV0000__y30000)
# 5. Hợp nhất kết quả phân tích
## Hệ thống "Payroll System" hỗ trợ quản lý giờ làm việc và thanh toán lương cho nhân viên, bao gồm hai chức năng chính
### Select Payment: Nhân viên chọn phương thức nhận lương (chuyển khoản, nhận trực tiếp, gửi bưu điện).
### Maintain Timecard: Nhân viên ghi nhận giờ làm việc và gửi thông tin cho hệ thống tính lương.
## Quan hệ giữa các lớp
### Employee liên kết với Timecard để ghi nhận giờ làm việc và với Payment để nhận thanh toán lương.
### Employee có thể liên kết với Project để ghi nhận giờ làm theo từng dự án.
### PayrollAdministrator quản lý các bản ghi thanh toán trong Payment.
## Biểu đồ lớp
![PlantText](https://www.planttext.com/api/plantuml/png/b9FFJiCm3CRlVGehfmwn2Quze24DYHr0I21n3etL1PAuIjAX2V5a77WaNe5qoxB-kwo7LdK_sx_FJlz-VfVES-iRhR9ISUVWJjUATeZmbK6uvY150S_UIbF5WE4Q1w6QxpGQ_u1-GtqvW4E5fN_gAdBT4yuAs98KKQ-eUf4QyzhIUqXS9zabRAYnhW1f_37bEulORKh9hKZOFWRMGtp1VS1VXNiCxAk-alr0iQzzz3Ji7_cu4FTjnfc0SG29BuviXCSrDSON8AXvKzWNh_he01KQjE4r5iynBg_Br2yuvZguE75Dsaxnn-7oMmY_Gi-bSlaiVUhwjgJKhT3IIES3BTdKZBVHyOJhq6oRJ8qcrV6GJYkxPZ2VtuJdOd71JiUX06Qn92iScnApj9U34EKM9vLN-xB7OGNnPpWm3iYmRDBXWAVJHNF3gxR94ere_xli7m00__y30000)
