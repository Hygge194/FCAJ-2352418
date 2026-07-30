---
title: "Worklog Tuần 2"
date: 2026-06-22
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Hiểu các khái niệm mạng nền tảng trên AWS với Amazon Virtual Private Cloud (VPC).
* Thực hành thiết lập hạ tầng mạng riêng biệt, cấu hình Route Tables, Internet Gateway và các lớp tường lửa bảo mật.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **2** | - Tìm hiểu tổng quan về Amazon VPC, quy hoạch dải địa chỉ IP với CIDR Notation <br> - Phân biệt khái niệm Public Subnet và Private Subnet | 22/06/2026 | 22/06/2026 | Amazon VPC Guide |
| **3** | - Tìm hiểu cơ chế hoạt động của Internet Gateway (IGW), Route Table <br> - Nghiên cứu giải pháp kết nối Internet an toàn cho Private Subnet bằng NAT Gateway | 23/06/2026 | 23/06/2026 | VPC Networking Guide |
| **4** | - Phân biệt cơ chế tường lửa Security Group (Stateful) và Network ACL (Stateless) <br> - **Thực hành:** Khởi tạo Custom VPC, chia Public Subnet và Private Subnet | 24/06/2026 | 24/06/2026 | Security Best Practices |
| **5** | - **Thực hành:** Tạo và gắn Internet Gateway vào VPC, cấu hình Route Table cho Public Subnet, khởi tạo NAT Gateway cho Private Subnet | 25/06/2026 | 25/06/2026 | VPC Hands-on Lab |
| **6** | - **Thực hành:** Khởi tạo EC2 tại Public Subnet và Private Subnet, kiểm thử kết nối Internet từ Private Subnet qua NAT Gateway, thiết lập SG & NACL | 26/06/2026 | 26/06/2026 | VPC Lab Testing |

### Kết quả đạt được tuần 2:

* Hiểu sâu sắc cách thức xây dựng mạng đám mây VPC an toàn cho ứng dụng web.
* Dựng thành công VPC mô hình chuẩn bao gồm Public Subnet (chứa Web/Load Balancer) và Private Subnet (chứa Backend/Database).
* Cấu hình NAT Gateway cho phép tài nguyên ở Private Subnet tải gói tin cập nhật mà ngăn chặn truy cập trực tiếp từ bên ngoài.
* Thiết lập chính xác Security Group và Network ACL đảm bảo an toàn truy cập mạng.