# Bước 1: Tổng quan hệ thống
## 1.1. Vấn đề của hệ thống hiện tại

Hệ thống CAB hiện tại đang tồn tại một số vấn đề:

- Việc phân công tài xế chủ yếu được thực hiện thủ công.
- Khách hàng khó theo dõi trạng thái chuyến đi.
- Thông tin thanh toán chưa được quản lý tập trung.
- Việc tìm kiếm và phân công tài xế chưa được tự động hóa.
- Khi tài xế từ chối hoặc không phản hồi, khách hàng có thể phải chờ lâu.
- Khó xử lý số lượng lớn yêu cầu đặt xe vào thời điểm cao điểm.
- Bộ phận vận hành gặp khó khăn trong việc theo dõi tài xế và các chuyến đang diễn ra.
- Khó tra cứu lịch sử chuyến đi và giao dịch.
- Hệ thống thông báo chưa có kiến trúc linh hoạt để mở rộng thêm nhiều kênh.
- Khó mở rộng hệ thống khi số lượng khách hàng và tài xế tăng.
- Chưa có đầy đủ cơ chế phân quyền và lưu vết các thao tác quan trọng.
- Một số nghiệp vụ chưa được xác định rõ như:
  - Cách tính cước.
  - Tiêu chí ưu tiên tài xế.
  - Thời gian tài xế phản hồi.
  - Chính sách hủy chuyến.
  - Xử lý khi mất kết nối.
  - Thời gian lưu trữ dữ liệu.
## 1.2. Mục tiêu đem lại

Hệ thống CAB mới được xây dựng nhằm:

### Đối với khách hàng

- Đặt xe nhanh chóng và thuận tiện.
- Theo dõi trạng thái chuyến đi.
- Biết thông tin tài xế và thời gian dự kiến đến.
- Xem lịch sử chuyến đi.
- Biết số tiền cần thanh toán.
- Hỗ trợ thanh toán tiền mặt và điện tử.
- Đánh giá tài xế sau khi hoàn thành chuyến.

### Đối với tài xế

- Nhận chuyến tự động dựa trên tiêu chí phù hợp.
- Chủ động chuyển trạng thái sẵn sàng nhận chuyến.
- Nhận thông báo khi có chuyến mới.
- Chấp nhận hoặc từ chối chuyến.
- Cập nhật trạng thái chuyến.
- Cập nhật vị trí để hỗ trợ tìm kiếm tài xế.

### Đối với nhân viên vận hành

- Quản lý khách hàng, tài xế và phương tiện.
- Theo dõi các chuyến đang diễn ra.
- Theo dõi trạng thái tài xế.
- Hỗ trợ xử lý các chuyến bị lỗi.
- Tra cứu lịch sử chuyến đi và giao dịch.
- Theo dõi và quản lý hoạt động của hệ thống.

### Đối với doanh nghiệp

- Tự động hóa quy trình đặt và phân công xe.
- Giảm sự phụ thuộc vào thao tác thủ công.
- Tăng khả năng phục vụ số lượng lớn khách hàng và tài xế.
- Quản lý tập trung dữ liệu chuyến đi và thanh toán.
- Nâng cao khả năng giám sát và báo cáo.
- Đảm bảo bảo mật và phân quyền.
- Có khả năng mở rộng thêm:
  - Loại dịch vụ.
  - Phương thức thanh toán.
  - Nhà cung cấp thanh toán.
  - Kênh thông báo.
  - Các chức năng mới trong tương lai.

---
## 1.3. Ai sử dụng hệ thống?

Hệ thống có 3 nhóm người dùng chính:

| Người dùng | Vai trò | Chức năng chính |
|---|---|---|
| **Customer** | Khách hàng | Đăng ký, đặt xe, theo dõi chuyến, thanh toán, đánh giá |
| **Driver** | Tài xế | Nhận chuyến, cập nhật vị trí, cập nhật trạng thái, hoàn thành chuyến |
| **Operation Staff** | Nhân viên vận hành | Quản lý khách hàng, tài xế, phương tiện, chuyến đi và xử lý sự cố |

### Các bên sử dụng / tương tác khác

| Người dùng / Hệ thống | Vai trò |
|---|---|
| **System Admin** | Quản trị tài khoản, phân quyền và cấu hình hệ thống |
| **Management** | Xem báo cáo, KPI, doanh thu và hiệu quả hoạt động |
| **Finance / Accounting** | Theo dõi giao dịch, thanh toán và doanh thu |
| **Customer Support** | Hỗ trợ khách hàng và tra cứu thông tin chuyến |
| **Payment Gateway** | Xử lý thanh toán điện tử |
| **Notification Provider** | Gửi Push Notification, SMS, Email hoặc các kênh khác |

---
# Bước 2: Stakeholder Analysis

## 2.1. Các bên liên quan – Stakeholder

| # | Stakeholder | Vai trò |
|---|---|---|
| 1 | **Management** | Chủ dự án, định hướng kinh doanh, theo dõi KPI, doanh thu và hiệu quả hoạt động |
| 2 | **Customer** | Người sử dụng dịch vụ, đặt xe, theo dõi chuyến, thanh toán và đánh giá tài xế |
| 3 | **Driver** | Người cung cấp dịch vụ vận chuyển, nhận và thực hiện chuyến |
| 4 | **Operation Staff** | Quản lý hoạt động đặt xe, theo dõi chuyến, tài xế và xử lý sự cố vận hành |
| 5 | **System Admin** | Quản trị tài khoản, phân quyền và cấu hình hệ thống |
| 6 | **Finance / Accounting** | Theo dõi giao dịch, thanh toán và doanh thu |
| 7 | **Customer Support** | Hỗ trợ khách hàng và tra cứu thông tin chuyến đi |
| 8 | **Payment Provider** | Cung cấp dịch vụ xử lý thanh toán điện tử |
| 9 | **Notification Provider** | Cung cấp dịch vụ gửi Push Notification, SMS, Email hoặc các kênh khác |
| 10 | **Map / Location Provider** | Cung cấp bản đồ, định vị, khoảng cách và dữ liệu hỗ trợ tính ETA |

---

## 2.2. Stakeholder Matrix

| Stakeholder | Power | Interest | Strategy |
|---|---|---|---|
| **Management** | Cao | Cao | **Manage Closely** – Cập nhật tiến độ, rủi ro, KPI, doanh thu và các quyết định quan trọng |
| **Customer** | Thấp | Cao | **Keep Informed** – Thu thập feedback và cung cấp thông tin về các thay đổi ảnh hưởng đến trải nghiệm |
| **Driver** | Thấp | Cao | **Keep Informed** – Thu thập nhu cầu, feedback và đảm bảo quy trình nhận/thực hiện chuyến phù hợp |
| **Operation Staff** | Cao | Cao | **Manage Closely** – Tham gia phân tích nghiệp vụ, kiểm thử và xác nhận quy trình vận hành |
| **System Admin** | Cao | Cao | **Manage Closely** – Xác định yêu cầu quản trị, phân quyền, cấu hình và bảo mật hệ thống |
| **Finance / Accounting** | Cao | Trung bình | **Keep Satisfied** – Đảm bảo yêu cầu về giao dịch, thanh toán và báo cáo doanh thu |
| **Customer Support** | Trung bình | Cao | **Keep Informed** – Cung cấp công cụ tra cứu và hỗ trợ xử lý các vấn đề của khách hàng |
| **Payment Provider** | Cao | Trung bình | **Keep Satisfied** – Đảm bảo tích hợp, giao dịch và xử lý lỗi thanh toán hoạt động ổn định |
| **Notification Provider** | Trung bình | Trung bình | **Monitor** – Theo dõi khả năng tích hợp và trạng thái dịch vụ |
| **Map / Location Provider** | Cao | Trung bình | **Keep Satisfied** – Đảm bảo dữ liệu vị trí, khoảng cách và ETA hoạt động ổn định |
## 2.2. Stakeholder Matrix 
 
```mermaid 
quadrantChart 
    title CAB System - Stakeholder Matrix 
    x-axis "Interest thấp" --> "Interest cao" 
    y-axis "Power thấp" --> "Power cao" 
 
    quadrant-1 "Manage Closely" 
    quadrant-2 "Keep Satisfied" 
    quadrant-3 "Monitor" 
    quadrant-4 "Keep Informed" 
 
    "Management": [0.85, 0.90] 
    "Customer": [0.85, 0.25] 
    "Driver": [0.80, 0.25] 
    "Operation Staff": [0.85, 0.85] 
    "System Admin": [0.85, 0.80] 
 
    "Finance / Accounting": [0.50, 0.75] 
    "Customer Support": [0.75, 0.45] 
 
    "Payment Provider": [0.50, 0.70] 
    "Notification Provider": [0.50, 0.50] 
    "Map / Location Provider": [0.50, 0.70]
```

---


# Bước 3: Business Objectives

## 3.1. Mục đích nghiệp vụ

| ID | Mục đích nghiệp vụ | Mô tả |
|---|---|---|
| **BO-01** | **Cải thiện trải nghiệm khách hàng** | Giúp khách hàng đặt xe nhanh chóng, theo dõi trạng thái chuyến, biết thông tin tài xế và thời gian dự kiến đến, xem lịch sử, thanh toán và đánh giá tài xế. |
| **BO-02** | **Tự động hóa quy trình đặt xe** | Giảm sự phụ thuộc vào tổng đài và thao tác thủ công trong việc tiếp nhận yêu cầu, tìm kiếm và phân công tài xế. |
| **BO-03** | **Nâng cao hiệu quả phân công tài xế** | Tự động tìm và ưu tiên tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành. |
| **BO-04** | **Nâng cao hiệu quả vận hành** | Cung cấp công cụ giúp nhân viên vận hành theo dõi chuyến đi, trạng thái tài xế, quản lý phương tiện và xử lý các trường hợp bất thường. |
| **BO-05** | **Quản lý tập trung dữ liệu** | Tập trung quản lý thông tin khách hàng, tài xế, phương tiện, chuyến đi, giao dịch và lịch sử hoạt động. |
| **BO-06** | **Nâng cao hiệu quả thanh toán** | Chuẩn hóa việc tính cước và hỗ trợ thanh toán tiền mặt hoặc thanh toán điện tử thông qua nhà cung cấp bên ngoài. |
| **BO-07** | **Nâng cao khả năng giám sát và ra quyết định** | Cung cấp dữ liệu và báo cáo về số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế. |
| **BO-08** | **Đảm bảo khả năng mở rộng và ổn định** | Xây dựng hệ thống có khả năng phục vụ số lượng lớn khách hàng và tài xế, đồng thời hạn chế ảnh hưởng khi một thành phần gặp sự cố. |
| **BO-09** | **Tăng khả năng mở rộng tính năng** | Cho phép bổ sung loại dịch vụ, phương thức thanh toán, nhà cung cấp thanh toán, kênh thông báo và các chức năng mới trong tương lai. |
| **BO-10** | **Đảm bảo bảo mật và kiểm soát hệ thống** | Bảo vệ dữ liệu cá nhân, dữ liệu vị trí và dữ liệu giao dịch; kiểm soát quyền truy cập và lưu vết các thao tác quan trọng. |

---

# Bước 4: Phạm vi dự án trong 7 tuần

Do thời gian triển khai chỉ có **7 tuần**, dự án được chia thành:

- **MVP – Must Have:** Bắt buộc hoàn thành trong 7 tuần.
- **Future Enhancement:** Các chức năng có thể phát triển ở giai đoạn sau.

## MVP trong 7 tuần

| Nhóm | Phạm vi |
|---|---|
| Authentication | Đăng ký, đăng nhập, xác thực người dùng |
| Customer | Quản lý hồ sơ, đặt xe, theo dõi chuyến |
| Driver | Hồ sơ, phương tiện, trạng thái nhận chuyến |
| Booking | Tạo và quản lý yêu cầu đặt xe |
| Driver Matching | Tìm kiếm và phân công tài xế |
| Trip | Quản lý trạng thái chuyến đi |
| Pricing | Tính cước chuyến đi |
| Payment | Tiền mặt + thanh toán điện tử |
| Notification | Thông báo cho Customer/Driver |
| Rating | Đánh giá tài xế |
| Operation | Quản lý và giám sát hệ thống |
| Reporting | Báo cáo cơ bản |
| Security | Authentication, Authorization, Audit Log |

---

# 3. Các module chính

## 3.1. Authentication & Authorization Module

Quản lý tài khoản và quyền truy cập hệ thống.

### Chức năng

- Đăng ký tài khoản Customer.
- Đăng nhập.
- Đăng xuất.
- Xác thực người dùng.
- Quản lý session/token.
- Phân quyền người dùng.
- Role-based access control (RBAC).

### Roles

```text
CUSTOMER
DRIVER
OPERATOR
ADMIN

