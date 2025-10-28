<div align="center">

# 🚀 Web Final Project · E‑Commerce

**Xây dựng Đồ án Quản lý Trà sữa AloTra**

<p>
  <img src="https://img.shields.io/badge/Java-17-007396?style=for-the-badge&logo=java&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring%20Boot-2.7.14-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
  <img src="https://img.shields.io/badge/Maven-3.9%2B-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white" />
</p>
<p>
  <img src="https://img.shields.io/badge/SQL%20Server-2019%2B-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white" />
  <img src="https://img.shields.io/badge/Thymeleaf-3.0%2B-005F0F?style=for-the-badge&logo=thymeleaf&logoColor=white" />
</p>

</div>

---


Dự án được phát triển bởi nhóm sinh viên:

| Thành viên | GitHub |
|------------|--------|
| **Nguyễn Duy Cường** | [@ndc87](https://github.com/ndc87) |
| **Võ Hữu Tín** | [@TimmyVonAtaraxia](https://github.com/TimmyVonAtaraxia) |
| **Phan Đình Duẩn** | [@Dinh-Duan](https://github.com/Dinh-Duan) |
| **Hà Như Quỳnh** | [@12hqwwo](https://github.com/12hqwwo) |
---

## Mục lục

1. [Giới thiệu về đề tài](#1-giới-thiệu-về-đề-tài)
   - [Các chức năng chính](#các-chức-năng-chính)
     - [Cho Khách hàng](#cho-khách-hàng)
     - [Cho Admin](#cho-admin)
     - [Cho Vendor](#cho-vendor)
2. [Các công nghệ sử dụng](#2-các-công-nghệ-sử-dụng)
   - [Backend Framework](#backend-framework)
   - [Security & Authentication](#security--authentication)
   - [Frontend](#frontend)
   - [Utilities & Libraries](#utilities--libraries)
   - [Build Tool & Application Server](#build-tool--application-server)
3. [Cấu trúc thư mục](#3-cấu-trúc-thư-mục)
4. [Cách chạy dự án](#4-cách-chạy-dự-án)
   - [Yêu cầu hệ thống](#yêu-cầu-hệ-thống)
   - [Các bước cài đặt](#các-bước-cài-đặt)
     - [4.1. Clone dự án](#41-clone-dự-án)
     - [4.2. Cấu hình cơ sở dữ liệu](#42-cấu-hình-cơ-sở-dữ-liệu)
     - [4.3. Cấu hình ứng dụng](#43-cấu-hình-ứng-dụng)
     - [4.4. Build và chạy ứng dụng](#44-build-và-chạy-ứng-dụng)
     - [4.5. Truy cập ứng dụng](#45-truy-cập-ứng-dụng)

---

## 1. Giới thiệu về đề tài

**Hệ thống Quản lý Bán hàng Trà Sữa AloTra** là một ứng dụng web thương mại điện tử đầy đủ tính năng, được xây dựng bằng Spring Boot Framework. Dự án cung cấp một nền tảng quản lý toàn diện cho chuỗi cửa hàng trà sữa với các tính năng từ quản lý sản phẩm, xử lý đơn hàng, thanh toán trực tuyến, quản lý chi nhánh đến thống kê doanh thu.

### Các chức năng chính:

#### Cho Khách hàng:

| Chức năng | Mô tả |
|-----------|-------|
| **Xác thực & Bảo mật** | Đăng ký/Đăng nhập với mã hóa BCrypt |
| **Quản lý hồ sơ** | Cập nhật thông tin cá nhân, địa chỉ giao hàng |
| **Duyệt sản phẩm** | Xem danh sách sản phẩm theo danh mục, tìm kiếm, lọc |
| **Giỏ hàng** | Thêm/Xóa/Cập nhật sản phẩm trong giỏ hàng |
| **Đặt hàng** | Tạo đơn hàng với nhiều hình thức thanh toán |
| **Thanh toán trực tuyến** | Tích hợp VNPay Payment Gateway |
| **Quản lý đơn hàng** | Theo dõi trạng thái, hủy/trả đơn hàng |
| **Đánh giá sản phẩm** | Đánh giá và bình luận về sản phẩm |
| **Mã giảm giá** | Áp dụng mã giảm giá cho đơn hàng |
| **Chat trực tiếp** | Trò chuyện với admin qua WebSocket |

#### Cho Admin:

| Chức năng | Mô tả |
|-----------|-------|
| **Dashboard** | Thống kê tổng quan hệ thống |
| **Quản lý danh mục** | CRUD danh mục sản phẩm |
| **Quản lý sản phẩm** | CRUD sản phẩm, hình ảnh (tích hợp Cloudinary) |
| **Quản lý đơn hàng** | Xem, cập nhật trạng thái đơn hàng |
| **Quản lý khách hàng** | Xem thông tin khách hàng |
| **Quản lý tài khoản** | CRUD tài khoản người dùng, phân quyền |
| **Quản lý mã giảm giá** | CRUD voucher giảm giá |
| **Quản lý chi nhánh** | CRUD thông tin chi nhánh |
| **Quản lý nhân viên** | Gán nhân viên cho chi nhánh |
| **Báo cáo thống kê** | Thống kê doanh thu theo thời gian |
| **Chat support** | Trả lời tin nhắn khách hàng real-time |

#### Cho Vendor:

| Chức năng | Mô tả |
|-----------|-------|
| **Dashboard chi nhánh** | Thống kê doanh thu của chi nhánh |
| **Quản lý đơn hàng** | Xử lý đơn hàng thuộc chi nhánh |
| **Quản lý kho** | Quản lý tồn kho sản phẩm |
| **Báo cáo doanh thu** | Thống kê doanh thu theo chi nhánh |
| **Quản lý hóa đơn** | Xem và xuất hóa đơn |

---

## 2. Các công nghệ sử dụng

### Backend Framework

| Công nghệ | Phiên bản | Mô tả |
|-----------|-----------|-------|
| **Spring Boot** | 2.7.14 | Core framework |
| **Spring Data JPA** | 2.7.14 | Data persistence layer |
| **Spring Security** | 2.7.14 | Authentication & Authorization |
| **Spring WebSocket** | 2.7.14 | Real-time communication |
| **Hibernate** | 5.6.x | ORM implementation |
| **Microsoft SQL Server** | 2019+ | Relational database |

### Security & Authentication

| Công nghệ | Mô tả |
|-----------|-------|
| **Spring Security** | Authentication và phân quyền |
| **BCrypt** | Password hashing |
| **CORS Configuration** | Cross-Origin Resource Sharing |

### Frontend

| Công nghệ | Mô tả |
|-----------|-------|
| **Thymeleaf** | Server-side template engine |
| **HTML/CSS/JavaScript** | Client-side rendering |
| **Bootstrap** | UI framework |
| **jQuery** | JavaScript library |
| **SockJS & STOMP** | WebSocket client libraries |
| **Animate.css** | CSS animation library |

### Utilities & Libraries

| Thư viện | Mục đích sử dụng |
|----------|------------------|
| **Lombok** | Giảm boilerplate code |
| **Apache Commons IO** | File handling utilities |
| **Cloudinary** | Cloud-based image storage |
| **Jackson** | JSON processing |
| **Jakarta Mail** | Email sending (notifications) |
| **Spring Boot DevTools** | Development tools |
| **Hibernate Validator** | Bean validation |

### Build Tool & Application Server

| Công cụ | Mô tả |
|---------|-------|
| **Apache Maven** | Dependency management và build automation |
| **Spring Boot Embedded Tomcat** | Application server |

---

## 3. Cấu trúc thư mục

> **Dự án được xây dựng theo kiến trúc MVC (Model-View-Controller) với Spring Boot**

```
Web_FinalProject/
├── src/
│   └── main/
│       ├── java/
│       │   └── com/
│       │       └── project/
│       │           └── DuAnTotNghiep/
│       │               ├── config/                   # Configuration classes
│       │               ├── controller/               # Controllers
│       │               │   ├── admin/                # Admin controllers
│       │               │   ├── customer/             # Customer controllers
│       │               │   └── vendor/
│       │               │   └── api/
│       │               ├── dto/                      # Data Transfer Objects
│       │               ├── entity/                   # JPA Entity classes
│       │               │   └── enumClass/            # Enumerations
│       │               ├── exception/                # Custom exceptions
│       │               ├── repository/               # Data Access Layer
│       │               ├── security/                 # Security configurations
│       │               ├── service/                  # Business logic layer
│       │               │   └── serviceImpl/          # Service implementations
│       │               └── utils/                    # Utility classes
│       ├── resources/
│       │   ├── application.properties                # Application configuration
│       │   ├── static/                               # Static resources
│       │   │   ├── admin/                            # Admin assets
│       │   │   │   ├── vendors/                      # Admin vendor libraries
│       │   │   │   └── assets/
│       │   │   ├── css/
│       │   │   ├── js/
│       │   │   ├── images/
│       │   │   └── vendor/                           # Client vendor libraries
│       │   └── templates/                            # Thymeleaf templates
│       │       ├── admin/                            # Admin views
│       │       ├── customer/                         # Customer views
│       │       └── layout/                           # Layout templates
│       └── webapp/
├── uploads/                                          # Uploaded files directory
├── upload-barcode/                                   # Barcode images
├── bin/                                              # Compiled classes
├── pom.xml                                           # Maven configuration
├── mvnw                                              # Maven wrapper (Unix)
├── mvnw.cmd                                          # Maven wrapper (Windows)
└── README.md                                         # Project documentation
```

---

## 4. Cách chạy dự án

### Yêu cầu hệ thống

Trước khi cài đặt, cần chuẩn bị các công cụ sau:

| Thành phần | Phiên bản khuyến nghị | Ghi chú |
|------------|----------------------|---------|
| **JDK** | 17+ | Thiết lập biến môi trường JAVA_HOME |
| **Apache Maven** | 3.9+ | Hoặc sử dụng Maven wrapper đi kèm |
| **SQL Server** | 2019 hoặc mới hơn | Dùng để lưu trữ dữ liệu |
| **IDE** | Spring Tool Suite / Eclipse  |
| **Git** | Latest | Version control |

### Các bước cài đặt

#### 4.1. Clone dự án

```bash
git clone https://github.com/ndc87/Web_FinalProject.git
cd Web_FinalProject
```

#### 4.2. Cấu hình cơ sở dữ liệu

##### 4.2.1. Tạo database trong SQL Server

1. Mở SQL Server Management Studio (SSMS)
2. Tạo database mới với tên `trasua`
3. Chạy script khởi tạo database

#### 4.3. Cấu hình ứng dụng

##### 4.3.1. Cập nhật file `application.properties`

Mở file `src/main/resources/application.properties` và cập nhật thông tin kết nối database:

```properties
# ====================== DATABASE CONFIG ======================
spring.datasource.url=jdbc:sqlserver://localhost:1433;database=trasua;encrypt=true;trustServerCertificate=true;useUnicode=true;characterEncoding=UTF-8
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.SQLServer2012Dialect
spring.jpa.hibernate.ddl-auto=none

# ====================== MAIL CONFIG ======================
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=your_email@gmail.com
spring.mail.password=your_app_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

# ====================== CLOUDINARY CONFIG ======================
cloudinary.cloud_name=your_cloud_name
cloudinary.api_key=your_api_key
cloudinary.api_secret=your_api_secret
```

**Lưu ý quan trọng:**

- **Database:** Thay đổi `username` và `password` theo thông tin SQL Server của bạn
- **Email Config:** Sử dụng App Password của Gmail (không phải mật khẩu thông thường)
  - Hướng dẫn tạo App Password: [Google App Passwords](https://support.google.com/accounts/answer/185833)
- **VNPay Config:** Các giá trị VNPay trong `ConfigVNPay.java` là môi trường sandbox
  - Tham khảo: [VNPay Developer](https://sandbox.vnpayment.vn/apis/)
- **Cloudinary:** Đăng ký tài khoản miễn phí tại [Cloudinary](https://cloudinary.com/) để lưu trữ hình ảnh

#### 4.4. Build và chạy ứng dụng

##### Cách 1: Sử dụng Maven Wrapper

```bash
# Windows
mvnw.cmd spring-boot:run

# Linux/macOS
./mvnw spring-boot:run
```

##### Cách 2: Sử dụng Maven CLI

```bash
mvn clean install
mvn spring-boot:run
```

##### Cách 3: Sử dụng IDE

1. Mở project trong IntelliJ IDEA
2. Chờ Maven tải dependencies
3. Tìm class `WebAloTraApplication.java` (có annotation `@SpringBootApplication`)
4. Click chuột phải → Run 'WebAloTra'

##### Cách 4: Sử dụng Spring Tool Suite

1. Mở project trong Spring Tool Suite
2. Chờ Maven tải dependencies
3. Tìm class `WebAloTraApplication.java` (có annotation `@SpringBootApplication`)
4. Click chuột phải → Run 'WebAloTra'

#### 4.5. Truy cập ứng dụng

Sau khi ứng dụng khởi động thành công, mở trình duyệt và truy cập:

| Trang | URL |
|-------|-----|
| **Trang chủ** | http://localhost:8080/ |

**Tài khoản mặc định:** 

| Vai trò | Email | Mật khẩu |
|---------|-------|----------|
| Admin | admin@gmail.com | 123456 |
| Vendor | vendor@gmail.com | 123456 |
| Customer | customer@gmail.com | 123456 |


---

<div align="center">

**Hệ thống Quản lý Bán hàng Trà Sữa**

Đồ án Lập trình Web - Đại học Sư phạm Kỹ thuật TP.HCM

</div>
