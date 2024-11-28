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
![PlantText](https://www.planttext.com/api/plantuml/png/L8yn3i8m34NtdC9YhzWPK1UOs2hOhSH0fDIfR4SLPsFWI5o1f5H2UBB_V_wotyzNhuPYPKmElMM1ivAugKhHnmdPO7FAjyZ7BEC6KA4r__xmKAElMLldMW9q-uM47HpOwbogo3WI80UOK7NE4jo2LBJkLVA2AGOq0YyKY2rYKjUixfUsCZ4pQF6ULBTNZAa8hM4LNGxOmN3FCmXfIUPwuj1-RFK1003__mC0)

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
![PlantText](https://www.planttext.com/api/plantuml/png/L90v3W8n34NxdCAYHzDJ81XcUYJ40Qp4e4ZPv9XYpaR1aRW2dWNGH2wYh_U_b_VpTQY2B8yO35h939ip3fn3WAEBFlagZ2fl0EkicAAujxvWaXzy6QfGdA3vkwRwM48UYBfsGhhMc2aBjlk5XnrSA90LRUAQQt4er7Ig2C7NRHPKJLshXZFnBNC4dTld15gqaC1aCpkZs7RLuc4jrThqpBefKoqvrN-kelDOEpZbTFCSSKnUyAXEl9CvK7BZkSRt0G00__y30000)

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
![PlantText](https://www.planttext.com/api/plantuml/png/L91BZi8m38RtEONLFUgUnOWfPJsL40Um4WEHyfATBdes5XnfhZ0cKoeHPP77z_sny_ju7gGYrpa6WxPcXkwOO_GYFYToS8ebv8Me0vHjOueQtlg2gK8tuS8vXFCYbMBZ_fUVr0yxud5ez-DWp3iBTbyh3tiuKo1RuTkv_b8SLkf7FQa4qypsZaBGOimgg3eEgat4rymHj06j6dIMDvyRhzJkuvtPMXBfJypQCPEKd8IsM4MtylPmpEdgEU8hUpMYodWZSw3aNZ_NnXy0003__mC0)

## 4. Maintain Timecard
### Mô tả :Nhân viên quản lý thông tin giờ làm việc của mình trên thẻ chấm công. Thẻ này ghi nhận số giờ làm việc, charge number tương ứng với các dự án, và trạng thái của thẻ.
### Luồng sự kiện
### Luồng chính (Basic Flow):
### Nhân viên mở giao diện thẻ chấm công
### Hiển thị thẻ
### Nhập giờ làm
### Lưu dữ liệu
### Hệ thống lưu lại các thay đổi trên thẻ
### Gửi thẻ chấm công
### Nhân viên yêu cầu gửi thẻ.
### Hệ thống xác nhận
### Kiểm tra tổng giờ làm không vượt quá giới hạn.
### Cập nhật trạng thái thẻ thành "Đã gửi" (Submitted).
### Lưu thẻ vào cơ sở dữ liệu ở trạng thái chỉ đọc.
### Luồng phụ (Alternative Flows) :
### Thẻ đã gửi:
### Nếu thẻ đã được gửi trước đó, hệ thống chỉ hiển thị ở chế độ chỉ đọc. Nhân viên không thể chỉnh sửa.
### Dữ liệu không hợp lệ:
### Nếu nhân viên nhập số giờ làm không hợp lệ (lớn hơn 24 giờ/ngày hoặc vượt quá giới hạn giờ làm), hệ thống hiển thị lỗi và yêu cầu sửa lại.
### Không kết nối được Project Management Database:
### Nếu không lấy được charge number từ cơ sở dữ liệu dự án, nhân viên chỉ có thể chỉnh sửa charge number đã tồn tại trên thẻ.
### Tiền điều kiện (Pre-conditions):
### Nhân viên đã đăng nhập vào hệ thống.
### Dữ liệu liên quan đến kỳ trả lương hiện tại phải tồn tại.
### Hậu điều kiện (Post-conditions):
### Dữ liệu thẻ chấm công được cập nhật hoặc lưu trữ trong hệ thống.
### Nếu thẻ được gửi, trạng thái thẻ là "Đã gửi" và không thể chỉnh sửa.
![PlantText](https://www.planttext.com/api/plantuml/png/V99BJWCn38RtEONLVTLz5wYKTWVYCS3UdN7Rm2GPEGvek1eBZiGLy3mwVMX4Lh7p-V_joB_VFuieo99SQJ2Nm31PkweCDT44CC8XC9L2DhSLUe790zOSoZAhev1hkUvwGN5uerpkqEEE77bPBLkspw-Mv_YpTPGZ5ptLX8gOGmSmlUfTO0xt5NcGli3qQGMw8WMUIDZI1q6UcDNw2FV8z5JkO0q52feJlQ5LXHuJSGtv7db7u9FR44Tp1Cu4RsqK2DjBUdoOwwAOlLHgJR0FYIDy1dwdqR4or966KSRbihHnLlxzdLSiRUk7le2jzHf-4SIcC4OR_EWdPSCpwCf8YeEoKaCdSxW9VclPeIWvMpFhJZcAKNV0BCWNpQPrvmy00F__0m00)

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
![PlantText](https://www.planttext.com/api/plantuml/png/N90xRiCm341tdeBmxWjqA89co6eWlO104ubWMH98ka3Erg57wXKYIqPWHnD5FZn-_d__JcfER9a3EB8as5qVQZpZEIIQEdJQ8iY5ykIpYuRTu1wIGcXeXLfufBvSd7R8-dtJY8zsPVdnn1Mf2O3Q4VlFpOeV-2t-TcF1t1gZB16sOi5MSu46ISIgE7fXCXmv9_M69YvgMSwdg53H_gX-bL5Obs0AEtSTgM0NZYpEU1s1xaoJGYiTP2rLJchBpbA8jb81jWKepJcmyGWdZkDw_kqz0G00__y30000)

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
![PlantText](https://www.planttext.com/api/plantuml/png/LCyv3iCW40NGdbECtFi2BYB78dsM4upC54Xi6OQ2iwN8aNA542-HJ0MVzmVnURt7BCXIl5CuIsJehbWvEWTdussmMHXRt07cDL6fSJlRX47--56pa5_GkZsgYqykLY8zBKHFIYspe3zj7WQuqxDG5c1AaKLjUHDwQhUtGbp1eA1gv_vObC81MfijcTNixURMbmRGDYU7TPy_KZ2_Ns_h2m00__y30000)

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
![PlantText](https://www.planttext.com/api/plantuml/png/N94z3i8m38NtdCBgtWim88JAYCHFBs2r5YfAck2uGyx6m96u0e4cfMsc-FdByxFoVhvsNf1bC5fX8vQXE1YdRI0g03taGha8TKtdi1SeJXZOQdqDNiZykF6wfEhEK8FSLliVyYsh_Sg8xPqQEMAFDpBKIsAJ7d6L4q2vJLDW0nTw3EG5c9nbKKcFn3Wa4kU1E82a2D2Ye4hDSkvKBuYPqnHXCdEZKZ9f54el_jZ2DiahrqXCwsoWwhpJ6F8IE-hRxpVaym400F__0m00)

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
![PlantText](https://www.planttext.com/api/plantuml/png/ND313i8W30RWEq_HxBxileDPvdOtCJv0mpebWK6WE_1i7dmaNy4wjqNb1FJxcyBp_cWIO-JPMOMQVOIYTy7wJ5G09jWEAWWosWIS68eJvkYjFUV4v1RtsVwgBTkr2-bQfROhA0zh16euaoND430xafmZllb1hMM1NIle4WPa-aTIAhzRhIhDMbDArOZ6pf7sNaBt2Meu-caqqI4RFrLzZF9u9ocyacfe6jvVigyN0000__y30000)

# Code Java cho ca sử dụng Maintain Timecard
```java
import java.util.*;

class Timecard {
    private final String employeeId;
    private final Date startDate;
    private final Date endDate;
    private final Map<Date, Map<String, Integer>> hoursWorked; // Ngày -> ChargeNumber -> Giờ
    private boolean isSubmitted;

    public Timecard(String employeeId, Date startDate, Date endDate) {
        this.employeeId = employeeId;
        this.startDate = startDate;
        this.endDate = endDate;
        this.hoursWorked = new HashMap<>();
        this.isSubmitted = false;
    }

    public boolean isSubmitted() {
        return isSubmitted;
    }

    public void addHours(Date date, String chargeNumber, int hours) throws IllegalStateException, IllegalArgumentException {
        if (isSubmitted) {
            throw new IllegalStateException("Cannot modify a submitted timecard.");
        }
        if (hours < 0 || hours > 24) {
            throw new IllegalArgumentException("Invalid hours. Must be between 0 and 24.");
        }

        hoursWorked.computeIfAbsent(date, k -> new HashMap<>()).put(chargeNumber, hours);
    }

    public void submit() throws IllegalStateException {
        if (isSubmitted) {
            throw new IllegalStateException("Timecard is already submitted.");
        }

        this.isSubmitted = true;
        System.out.println("Timecard submitted successfully!");
    }

    @Override
    public String toString() {
        StringBuilder builder = new StringBuilder();
        builder.append("Timecard for Employee: ").append(employeeId).append("\n");
        builder.append("Start Date: ").append(startDate).append(", End Date: ").append(endDate).append("\n");
        builder.append("Hours Worked: \n");

        for (Map.Entry<Date, Map<String, Integer>> entry : hoursWorked.entrySet()) {
            builder.append("  Date: ").append(entry.getKey()).append("\n");
            for (Map.Entry<String, Integer> charges : entry.getValue().entrySet()) {
                builder.append("    ChargeNumber: ").append(charges.getKey()).append(", Hours: ").append(charges.getValue()).append("\n");
            }
        }

        builder.append("Status: ").append(isSubmitted ? "Submitted" : "Not Submitted").append("\n");
        return builder.toString();
    }
}

public class MaintainTimecard {
    public static void main(String[] args) {
        try {
            String employeeId = "E12345";
            Date startDate = new Date(); // Giả định
            Date endDate = new Date(); // Giả định

            Timecard timecard = new Timecard(employeeId, startDate, endDate);

            // Thêm giờ làm
            timecard.addHours(new Date(), "CHARGE001", 8);
            timecard.addHours(new Date(), "CHARGE002", 4);

            // Hiển thị thẻ
            System.out.println(timecard);

            // Gửi thẻ
            timecard.submit();

            // Cố gắng chỉnh sửa sau khi đã gửi
            timecard.addHours(new Date(), "CHARGE003", 2); // Lỗi

        } catch (Exception e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}

