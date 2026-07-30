---
title: "Worklog Tuần 3"
date: 2026-06-29
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Nghiên cứu dịch vụ lưu trữ đối tượng Amazon S3 và ứng dụng Hosting Website tĩnh.
* Tìm hiểu giải pháp CSDL quan hệ Amazon RDS (PostgreSQL/MySQL) và CSDL NoSQL Amazon DynamoDB.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :---: | :--- | :---: | :---: | :--- |
| **2** | - Tìm hiểu Amazon S3: Buckets, Objects, Storage Classes và Bucket Policy <br> - So sánh giữa Block Storage (EBS), File Storage (EFS) và Object Storage (S3) | 29/06/2026 | 29/06/2026 | Amazon S3 Developer Guide |
| **3** | - **Thực hành:** Tạo S3 Bucket, bật tính năng Static Website Hosting và cấu hình Bucket Policy cho phép phân phối tài nguyên tĩnh công khai | 30/06/2026 | 30/06/2026 | S3 Hosting Lab |
| **4** | - Nghiên cứu Amazon RDS: Lựa chọn Database Engine (PostgreSQL/MySQL), Instance Classes <br> - Học khái niệm Multi-AZ Deployment và Read Replicas | 01/07/2026 | 01/07/2026 | Amazon RDS Guide |
| **5** | - **Thực hành:** Khởi tạo PostgreSQL Database Instance trên RDS nằm trong Private Subnet, thiết lập Security Group cho phép Backend kết nối | 02/07/2026 | 02/07/2026 | RDS Hands-on Lab |
| **6** | - Tìm hiểu Amazon DynamoDB: Tables, Items, Primary Keys (Partition Key & Sort Key) <br> - **Thực hành:** Khởi tạo bảng DynamoDB và thao tác CRUD dữ liệu | 03/07/2026 | 03/07/2026 | DynamoDB Documentation |

### Kết quả đạt được tuần 3:

* Thành công triển khai trang web tĩnh lên Amazon S3 với chi phí tối ưu.
* Nắm vững nguyên lý hoạt động của Amazon RDS và khởi tạo thành công Instance PostgreSQL phục vụ lưu trữ dự án.
* Hiểu bản chất của cơ sở dữ liệu NoSQL DynamoDB và thực thi các câu lệnh CRUD cơ bản.  