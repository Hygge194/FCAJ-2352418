---
title: "Worklog Tuần 4"
date: 2026-07-06
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Khởi tạo cấu trúc dự án Backend Shopsflow (Spring Boot 4, Java 21) và thiết lập môi trường phát triển cục bộ.
* Thiết lập hệ thống cơ sở dữ liệu PostgreSQL và tích hợp Flyway để quản lý lược đồ dữ liệu tự động.
* Soạn thảo tài liệu Proposal (Đề xuất dự án - Mục 2.3) hoàn chỉnh cho nhóm.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành |
| :---: | :--- | :---: | :---: |
| **2** | - Tạo khung dự án từ Spring Initializr, lựa chọn Java 21, Spring Boot 4 và cấu hình các dependencies ban đầu | 06/07/2026 | 06/07/2026 |
| **3** | - Cấu hình file `pom.xml`, cài đặt công cụ và thiết lập các biến cấu hình kết nối trong file `.env` (DB URL, Username, Password) | 07/07/2026 | 07/07/2026 |
| **4** | - Cấu hình database PostgreSQL trên máy cục bộ và kiểm tra kết nối thông qua Spring Data JPA | 08/07/2026 | 08/07/2026 |
| **5** | - Tích hợp Flyway Migration vào dự án, cấu hình đường dẫn và viết file SQL script khởi tạo bảng đầu tiên (`V1__init.sql`) | 09/07/2026 | 09/07/2026 |
| **6** | - Định nghĩa cấu trúc các JPA Entities nền tảng bao gồm `User`, `Product`, `Category` cùng với các Repository cơ bản <br> - Soạn thảo tài liệu 2.3 Proposal (Tổng quan, kiến trúc, timeline, ngân sách) | 10/07/2026 | 10/07/2026 |

### Kết quả đạt được tuần 4:

* Hạ tầng Backend cơ bản được thiết lập hoàn tất, chạy mượt mà ở môi trường local.
* Database PostgreSQL được liên kết thành công và tự động đồng bộ hóa cấu trúc bảng thông qua Flyway.
* Xây dựng xong các thực thể JPA lõi đại diện cho cơ sở dữ liệu của ứng dụng Shopsflow.
* Hoàn thành 100% tài liệu Proposal (Đề xuất dự án) cho hệ thống Shopsflow.