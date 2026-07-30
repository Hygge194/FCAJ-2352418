---
title: "Worklog Tuần 5"
date: 2026-07-13
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Triển khai hệ thống bảo mật xác thực Spring Security tích hợp Stateless Token JWT.
* Phát triển API Danh mục sản phẩm (Category API) và API Sản phẩm (Product API) có phân quyền Role-based Access Control.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành |
| :---: | :--- | :---: | :---: |
| **2** | - Cấu hình Spring Security, xây dựng `JwtUtil` phục vụ cho việc sinh token khi đăng nhập và giải mã token khi gửi request | 13/07/2026 | 13/07/2026 |
| **3** | - Viết API Đăng ký và Đăng nhập (`/api/auth/register`, `/api/auth/login`), mã hóa mật khẩu người dùng bằng BCrypt | 14/07/2026 | 14/07/2026 |
| **4** | - Triển khai bộ lọc `JwtFilter` và cấu hình phân quyền các endpoints (chỉ `ADMIN` được tạo/sửa/xóa sản phẩm và danh mục) | 15/07/2026 | 15/07/2026 |
| **5** | - Viết API CRUD cho Category và Product, hiện thực chức năng lọc sản phẩm theo danh mục, khoảng giá và từ khóa | 16/07/2026 | 16/07/2026 |
| **6** | - Cấu hình `GlobalExceptionHandler` xử lý ngoại lệ tập trung và tích hợp `springdoc-openapi` hiển thị UI Swagger để test API | 17/07/2026 | 17/07/2026 |

### Kết quả đạt được tuần 5:

* Hệ thống authentication bằng JWT hoạt động chính xác và bảo mật.
* API CRUD cho Sản phẩm và Danh mục được xây dựng hoàn thiện và kiểm soát phân quyền an toàn.
* Swagger UI được tích hợp thành công tại địa chỉ `/swagger-ui.html` giúp quá trình phát triển và kiểm thử API dễ dàng hơn.