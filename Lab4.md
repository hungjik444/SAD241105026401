# Thiết kế các ca sử dụng của hệ thống Payroll system và giải thích 
## Thiết kế các ca sử dụng của hệ thống Payroll system

## 1.Login
### Mục đích:
#### Xác thực người dùng trước khi họ có thể sử dụng hệ thống.
#### Tác nhân chính (Primary Actor):
#### Người dùng (Quản trị viên lương, nhân viên nhân sự).
#### Luồng công việc chính:
#### Người dùng nhập tên đăng nhập và mật khẩu.
#### Hệ thống kiểm tra thông tin trong cơ sở dữ liệu.
#### Nếu thông tin đúng, hệ thống cho phép truy cập vào giao diện chính.
#### Nếu thông tin sai, hệ thống hiển thị thông báo lỗi và yêu cầu thử lại.
#### Điểm mở rộng (Extension Points):
#### Trường hợp tài khoản bị khóa hoặc không tồn tại: Hiển thị thông báo phù hợp.
#### Chức năng quên mật khẩu để hỗ trợ người dùng.
### Biểu đồ tuần tự :
![diagram](https://www.planttext.com/api/plantuml/png/R90nImCn68Rt_8gNxlw13jAnKnSLNDDSk0JlSiVbg-3SeODBEtKIUeE3Ga71nSlWaCF_aL_WNp2vLYXgXkJZvNaVFlBbFYQMU4EBic1SKDNWoie6t68qopzVWdlGoFoxoKUiZfWMkkQ6S75dIPO3DWrk1LB1RHB4XlhP-P4OOwP2jwz1_jcWt_HBayCSebk_GnadmaqCdXRiA3qfN_jM3ExNzFYtM2RzoyDuGUZNf-Q8xeo2I0M6U7xCKPts6sEgWrkQGNsFNFCAMKnM1aBvlL5C5bR-aORkaJ0FNQl_bruUDfpxja8Ht5OpQJ8sYLVwtMy0003__mC0)

## 2.Maintain Timecard
### Mục đích:
#### Quản lý giờ làm việc, ngày nghỉ, và thông tin công việc của từng nhân viên.
#### Tác nhân chính (Primary Actor):
#### Nhân viên nhân sự.
#### Luồng công việc chính:
#### Nhân viên nhân sự đăng nhập và truy cập giao diện chấm công.
#### Hệ thống hiển thị danh sách các bảng chấm công.
#### Nhân viên chọn bảng chấm công cần chỉnh sửa.
#### Hệ thống hiển thị chi tiết bảng chấm công.
#### Nhân viên chỉnh sửa thông tin, bao gồm giờ làm, ngày nghỉ, hoặc các ghi chú.
#### Sau khi chỉnh sửa, nhân viên lưu thông tin.
#### Hệ thống xác nhận và cập nhật vào cơ sở dữ liệu.
#### Điểm mở rộng (Extension Points):
#### Trường hợp dữ liệu không hợp lệ: Hiển thị thông báo lỗi.
#### Trường hợp ghi đè dữ liệu cũ: Yêu cầu xác nhận trước khi lưu.
### Biểu đồ tuần tự :
![diagram](https://www.planttext.com/api/plantuml/png/V99FIiD06CNtESL7LWfj3z255Bh9GbnK5sxZj2G3oMTC9e4ifGiH4Um1X6WHGIWekCeikfZGUym9l8BV94L2YDqCmynxl_Vcpu_SJXBXnY8D0yjbuZe6PmPk0lQPhruHCgu-4B2U9rf-sLP4OivuvAA0ypmHYx2MErhUWV2rNA5dMnP1XYVx_J5KJzKIFSBeSXDPUzUG1Cvi39VgXJLR23TfhkKjWeZJ75Yjxg0kTBdcC7VHXuICFZ1oleN0r3TwNRJ3jLnYNUlXNqydO4hYHuGhog7ARQKfz8vcITuRb9ORzs0Yypa8hikjwCFr1VznYL172evmv17q6G9LX0D0JnKvZKOyW6oKZOwx7QRctfeR5P2f0lnsgHQuMgbrvpYTJgUxpxIt-u4t38o7KWg2DkB90kVcVrc_0000__y30000)

## 3 .Run Payroll
### Mục đích:
#### Tính toán bảng lương cho nhân viên dựa trên dữ liệu chấm công, mức lương cơ bản, và các khoản phụ cấp, khấu trừ.
#### Tác nhân chính (Primary Actor):
#### Quản trị viên lương.
#### Luồng công việc chính:
#### Quản trị viên đăng nhập và truy cập giao diện chạy bảng lương.
#### Hệ thống lấy dữ liệu từ bảng chấm công, thông tin mức lương, và các quy định thuế/phụ cấp.
#### Hệ thống tự động tính toán lương cho từng nhân viên.
#### Kết quả bảng lương được hiển thị cho quản trị viên kiểm tra.
#### Quản trị viên xác nhận và lưu bảng lương.
#### Hệ thống lưu kết quả vào cơ sở dữ liệu.
#### Điểm mở rộng (Extension Points):
#### Trường hợp dữ liệu chấm công chưa đầy đủ: Hiển thị cảnh báo và yêu cầu bổ sung dữ liệu.
#### Tính năng xem lịch sử bảng lương cũ.
### Biểu đồ tuần tự :
![diagram](https://www.planttext.com/api/plantuml/png/Z94_JiCm5CPtd-9JzrwW0sgt3WmW65XJfqeY9IyXiIjbH1qOkj0RDAgw85KmCCK3WwFUmoVW2ZWcq41LYVtxVN_U-r3luq9ukP19p3mkqXnNNfcdSJpnauZW5HXSIrDl2I8tQeL5f9y9yU7rK54mO9b58nvb7WdSb8MO9mwP6lK84HgrRaNib-NmebEEq3mrImf0eQdt6UlueHNqWH7kTCM_H8HxMHhrqBQH9RZZpjfVcdfNmZVg1N5a6qbmQx9BmFMRZLtepVUGd-mZVAlt54AakYBCsWC49-AJebERiYGtVFK7GhFMMuYZwVdQ_RbTH_dl2dtOWIBK6vlf9hFndFpsqunz0W00__y30000)

## 4.Process Bank Transactions
### Mục đích:
#### Tự động chuyển khoản lương cho nhân viên qua hệ thống ngân hàng.
#### Tác nhân chính (Primary Actor):
#### Quản trị viên lương.
#### Luồng công việc chính:
#### Quản trị viên đăng nhập và truy cập giao diện xử lý giao dịch.
#### Hệ thống lấy dữ liệu bảng lương đã được xác nhận.
#### Hệ thống gửi thông tin tài khoản ngân hàng và số tiền đến hệ thống ngân hàng.
#### Ngân hàng xử lý giao dịch và trả kết quả (thành công hoặc thất bại).
#### Hệ thống hiển thị kết quả cho quản trị viên.
#### Ghi nhận trạng thái giao dịch vào cơ sở dữ liệu.
#### Điểm mở rộng (Extension Points):
#### Trường hợp giao dịch thất bại: Hiển thị thông báo lỗi và chi tiết lỗi.
#### Trường hợp thông tin ngân hàng không hợp lệ: Cảnh báo và yêu cầu chỉnh sửa.
### Biểu đồ tuần tự :
![diagram](
https://www.planttext.com/api/plantuml/png/T98nJiCm68Ltd-Af4qZq0XsgmW8J0i70Qfmgjfeu8R4H6H430mlSe841gL850rCZnE2gz_09UWNijY0NaTNwtllVU_Ao-HgKYXPAfmcXJ6K5JcXLP4co7wL2WfRed6exUv5GXMqUS2tCH29Pl2zg6NT8xgI2YPnAXREgLCDq9JcopJqKjytJN-Y0ob4BYEFOF4jmC_OYifMZsz_Ozp1_dDyvM78xc-PauzLrG2ZeuSBKR0r9NEdADhU-Wgx0LhfM-qFRJ0KgCz6UVDMuSGz8p2TYGJD4RWJ6Vy_sWq8_MeUy8H6kcGurs57SVBZaoXrKPYmmufbVTW-bw--UVSPT4YpK3NA5VK9NvVVYODwQjCznlhvzQUhitqRRFeEXZFoF8EGR003__mC0
)

## 5.Print Paychecks
### Mục đích:
#### Tạo và in phiếu lương cho nhân viên để lưu trữ hoặc phát cho nhân viên.
#### Tác nhân chính (Primary Actor):
#### Quản trị viên lương.
#### Luồng công việc chính:
#### Quản trị viên đăng nhập và truy cập giao diện in phiếu lương.
#### Hệ thống hiển thị danh sách các kỳ lương đã tính toán.
#### Quản trị viên chọn kỳ lương cần in phiếu.
#### Hệ thống lấy dữ liệu bảng lương và tạo phiếu lương cho từng nhân viên.
#### Phiếu lương được hiển thị để kiểm tra hoặc chỉnh sửa (nếu cần).
#### Quản trị viên gửi lệnh in.
#### Hệ thống xác nhận in thành công.
#### Điểm mở rộng (Extension Points):
#### Tùy chỉnh định dạng phiếu lương (logo, thông tin bổ sung).
#### Chọn in toàn bộ phiếu hoặc chỉ in cho một số nhân viên cụ thể.
### Biểu đồ tuần tự :
![diagram](https://www.planttext.com/api/plantuml/png/Z96nJiCm48PtFyMfUr-W0ofYwS00Oe7HE5LiuLn3OYDvH1qOAYHu0og4a2eXa62AXmwk-Xv-0bwXTcX262An_zz_tzrzs_MuLBHGEfE4CZKhu8IQOYRbOP8915h2u5JxwXb15Tuku4Qu5OBSVcoNc0v87b31H4vHmPafrJIhaOctTw2ujuynHFvK3W_soH5i7ZPpJ06vhzvoikU78T05Hd3kbkmdX72jZRUtqKORO3NNMtyK1EuHhhpzR8mZyeeGSZaNlbhhTkelTkoh5mE9j-yWHLX4msKyGDfqa7xJISZFiTvy0Gb53cLmvysmjg7F-CAjTAseEuejzQy3TJZ5tLDGOEuhmECf9l79XEm0003__mC0)
#  Lý do đưa ra thiết kế đó:
## 1. Login
### Lý do thiết kế:
### Bảo mật: Đây là bước đầu tiên và quan trọng nhất để đảm bảo rằng chỉ những người dùng được phép (nhân viên nhân sự, quản trị viên lương) mới có thể truy cập vào hệ thống.
### Xác định quyền truy cập: Sau khi đăng nhập, hệ thống có thể phân quyền để chỉ cho phép người dùng thực hiện các chức năng phù hợp với vai trò của họ.
### Trải nghiệm người dùng: Quy trình đơn giản và trực quan để không làm phức tạp trải nghiệm người dùng.
## 2. Maintain Timecard
### Lý do thiết kế:
### Tính minh bạch: Bảng chấm công là dữ liệu nền tảng để tính lương. Việc cho phép chỉnh sửa và cập nhật thông tin giờ làm, ngày nghỉ giúp quản lý chặt chẽ và minh bạch.
### Tương tác linh hoạt: Thiết kế quy trình chỉnh sửa theo từng bước, từ tải danh sách, chọn bảng chấm công đến lưu dữ liệu, giúp người dùng dễ kiểm soát và tránh lỗi.
### Tích hợp dữ liệu: Việc cập nhật dữ liệu được thiết kế để đồng bộ với các module khác như bảng lương, giảm thiểu lỗi do dữ liệu không nhất quán.
## 3. Run Payroll
### Lý do thiết kế:
### Tự động hóa: Hệ thống tự động tính toán lương giúp giảm thiểu sai sót và tiết kiệm thời gian so với tính toán thủ công.
### Kiểm tra và xác nhận: Việc hiển thị kết quả trước khi lưu đảm bảo rằng quản trị viên có thể kiểm tra tính chính xác của bảng lương trước khi xử lý tiếp.
### Tính mô-đun: Quy trình này dễ mở rộng để tích hợp các yếu tố như thưởng, phạt, thuế, và phụ cấp, phù hợp với quy định từng doanh nghiệp.
## 4. Process Bank Transactions
### Lý do thiết kế:
### Tích hợp với ngân hàng: Chức năng này đảm bảo tính hiện đại và tiện lợi của hệ thống, tự động hóa quy trình chuyển khoản lương.
### Giảm thiểu rủi ro: Xử lý trực tiếp qua hệ thống ngân hàng giúp tránh các lỗi thủ công trong chuyển khoản.
### Theo dõi giao dịch: Hệ thống ghi nhận trạng thái giao dịch (thành công hoặc thất bại) để quản trị viên dễ dàng kiểm soát và xử lý các vấn đề phát sinh.
## 5. Print Paychecks
### Lý do thiết kế:
### Lưu trữ và minh bạch: Phiếu lương là tài liệu cần thiết để nhân viên biết rõ về lương của mình, đồng thời giúp doanh nghiệp lưu trữ hồ sơ tài chính.
### Tùy chỉnh linh hoạt: Việc cho phép tùy chỉnh định dạng phiếu lương (logo, thông tin công ty) giúp hệ thống phù hợp với đặc thù của từng doanh nghiệp.
### Tiện ích: Chức năng chọn in theo nhóm hoặc cá nhân giúp tiết kiệm thời gian và công sức cho quản trị viên lương.
## Các nguyên tắc chung trong thiết kế:
### Đơn giản và trực quan: Giảm thiểu các bước thừa, đảm bảo quy trình mạch lạc, dễ sử dụng cho mọi người dùng.
### Tính nhất quán: Các bước trong quy trình được chuẩn hóa để dễ dàng duy trì và phát triển.
### Tính bảo mật: Tất cả dữ liệu liên quan đến lương và giao dịch ngân hàng được bảo mật và xử lý an toàn.
### Tính mở rộng: Mỗi chức năng được thiết kế với tư duy mô-đun, có thể dễ dàng tích hợp các tính năng mới trong tương lai.
### Tích hợp dữ liệu: Dữ liệu được liên kết chặt chẽ giữa các module (bảng chấm công, bảng lương, phiếu lương) để đảm bảo tính chính xác và đồng nhất.
