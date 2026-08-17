# CAB System – Business Analysis

## 1. Mục tiêu hệ thống

### 1.1. Tổng quan

CAB System là nền tảng đặt xe trực tuyến, hỗ trợ toàn bộ quy trình từ khi khách hàng tạo yêu cầu đặt xe, tìm kiếm và phân công tài xế, thực hiện chuyến đi, tính cước, thanh toán cho đến đánh giá sau chuyến.

Hệ thống được xây dựng với mục tiêu thay thế các quy trình thủ công hiện tại, nâng cao trải nghiệm khách hàng, hỗ trợ nhân viên vận hành và tạo nền tảng có khả năng mở rộng trong tương lai.

### 1.2. Mục tiêu chính

| STT | Mục tiêu | Mô tả |
|-----|----------|-------|
| 1 | Đặt xe trực tuyến | Cho phép khách hàng nhập điểm đón, điểm đến, lựa chọn loại xe và tạo yêu cầu đặt xe |
| 2 | Tự động tìm tài xế | Tìm kiếm và ưu tiên tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và tiêu chí vận hành |
| 3 | Quản lý chuyến đi | Theo dõi toàn bộ trạng thái chuyến từ lúc tạo yêu cầu đến khi hoàn thành |
| 4 | Tính cước | Xác định số tiền khách hàng cần thanh toán dựa trên loại dịch vụ và thông tin chuyến đi |
| 5 | Thanh toán | Hỗ trợ thanh toán tiền mặt và thanh toán điện tử thông qua nhà cung cấp bên thứ ba |
| 6 | Thông báo | Gửi thông báo cho khách hàng và tài xế về các sự kiện quan trọng của chuyến đi |
| 7 | Quản trị | Cho phép nhân viên quản lý khách hàng, tài xế, phương tiện, chuyến đi và giao dịch |
| 8 | Báo cáo | Cung cấp dữ liệu về số chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế |
| 9 | Bảo mật | Đảm bảo xác thực, phân quyền, bảo vệ dữ liệu và lưu vết các thao tác quan trọng |
| 10 | Khả năng mở rộng | Cho phép bổ sung dịch vụ, phương thức thanh toán và kênh thông báo trong tương lai |

---

## 2. Người sử dụng hệ thống

Hệ thống có 3 nhóm người dùng chính:

### 2.1. Customer – Khách hàng

Khách hàng sử dụng CAB System để:

- Đăng ký tài khoản
- Đăng nhập
- Cập nhật thông tin cá nhân
- Nhập điểm đón và điểm đến
- Lựa chọn loại xe
- Tạo yêu cầu đặt xe
- Theo dõi trạng thái chuyến đi
- Theo dõi thông tin tài xế
- Xem thời gian dự kiến tài xế đến
- Xem lịch sử chuyến đi
- Xem số tiền phải trả
- Thanh toán
- Đánh giá tài xế

### 2.2. Driver – Tài xế

Tài xế sử dụng CAB System để:

- Đăng ký hoặc được nhân viên vận hành tạo tài khoản
- Cập nhật thông tin cá nhân
- Cập nhật thông tin phương tiện
- Chuyển trạng thái sẵn sàng nhận chuyến
- Nhận thông báo chuyến mới
- Chấp nhận hoặc từ chối chuyến
- Cập nhật vị trí
- Cập nhật trạng thái chuyến
- Xác nhận đã đến điểm đón
- Xác nhận đã đón khách
- Cập nhật trạng thái đang di chuyển
- Hoàn thành chuyến

### 2.3. Operation Staff – Nhân viên vận hành

Nhân viên vận hành sử dụng hệ thống để:

- Quản lý khách hàng
- Quản lý tài xế
- Quản lý phương tiện
- Theo dõi các chuyến đang diễn ra
- Kiểm tra trạng thái tài xế
- Hỗ trợ xử lý các chuyến bị lỗi
- Tra cứu lịch sử chuyến đi
- Tra cứu lịch sử giao dịch
- Theo dõi hoạt động của hệ thống

---

# 3. Các bên liên quan – Stakeholders

| Stakeholder | Vai trò | Mức độ quan tâm | Mức độ ảnh hưởng |
|-------------|---------|------------------|-------------------|
| Customer | Đặt xe và sử dụng dịch vụ | Cao | Trung bình |
| Driver | Nhận và thực hiện chuyến | Cao | Trung bình |
| Operation Staff | Điều phối và xử lý sự cố | Cao | Cao |
| System Admin | Quản trị hệ thống và phân quyền | Trung bình/Cao | Cao |
| Management | Theo dõi KPI, doanh thu và báo cáo | Cao | Cao |
| Finance/Accounting | Quản lý thanh toán và doanh thu | Cao | Cao |
| Payment Provider | Xử lý thanh toán điện tử | Trung bình | Cao |
| Notification Provider | Cung cấp dịch vụ gửi thông báo | Trung bình | Trung bình |
| Development/IT Team | Xây dựng và bảo trì hệ thống | Cao | Cao |
| Security/Compliance | Kiểm soát bảo mật và tuân thủ | Trung bình | Cao |

---

# 4. Stakeholder Matrix

Stakeholder được phân loại dựa trên hai tiêu chí:

- **Power:** Mức độ quyền lực/ảnh hưởng đến dự án
- **Interest:** Mức độ quan tâm đến dự án

## 4.1. Power / Interest Matrix

| | Interest thấp | Interest cao |
|---|---|---|
| **Power cao** | **Keep Satisfied** | **Manage Closely** |
| **Power thấp** | **Monitor** | **Keep Informed** |

### Manage Closely

Các stakeholder cần được quản lý và trao đổi thường xuyên:

- Management / Ban giám đốc
- Operation Staff
- Product Owner / Business Owner
- Business Analyst
- Finance/Accounting
- Security/Compliance

### Keep Satisfied

Các stakeholder có quyền ảnh hưởng cao nhưng không cần tham gia vào mọi hoạt động hằng ngày:

- Senior Management
- Security/Compliance
- Một số bộ phận quản lý cấp cao

### Keep Informed

Các stakeholder cần được cập nhật thường xuyên:

- Customer
- Driver
- Customer Support
- Các bộ phận nghiệp vụ liên quan

### Monitor

Các stakeholder có mức độ ảnh hưởng và quan tâm thấp:

- Các bộ phận nội bộ chỉ sử dụng dữ liệu/báo cáo gián tiếp
- Các bên liên quan không trực tiếp tham gia vận hành hệ thống

---

# 5. Mindmap – CAB System

Mindmap tổng quan của hệ thống:

```text
CAB SYSTEM
│
├── 1. Stakeholders
│   ├── Customer
│   ├── Driver
│   ├── Operation Staff
│   ├── Admin
│   ├── Management
│   ├── Finance
│   └── External Providers
│
├── 2. Account & Authentication
│   ├── Register
│   ├── Login
│   ├── Profile
│   └── Authorization
│
├── 3. Booking
│   ├── Pickup Location
│   ├── Destination
│   ├── Vehicle Type
│   └── Create Booking
│
├── 4. Driver Matching
│   ├── Driver Location
│   ├── Driver Availability
│   ├── Matching Criteria
│   ├── Accept Trip
│   ├── Reject Trip
│   └── Retry Matching
│
├── 5. Trip
│   ├── Searching Driver
│   ├── Driver Assigned
│   ├── Driver Arrived
│   ├── Passenger Picked Up
│   ├── In Progress
│   └── Completed
│
├── 6. Fare & Payment
│   ├── Fare Calculation
│   ├── Cash Payment
│   ├── Online Payment
│   ├── Payment Failed
│   └── Payment Retry
│
├── 7. Notification
│   ├── Customer Notification
│   ├── Driver Notification
│   ├── Push Notification
│   ├── SMS
│   └── Email
│
└── 8. Administration & Reporting
    ├── Customer Management
    ├── Driver Management
    ├── Vehicle Management
    ├── Trip Management
    ├── Transaction Management
    ├── Reports
    └── Audit Log
