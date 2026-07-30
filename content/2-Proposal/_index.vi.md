---
title: "Bản đề xuất"
date: 2026-06-15
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

Tại phần này, em xin trình bày tóm tắt các nội dung đề xuất cho dự án thực tập của mình: **Shopsflow Backend**.

# Shopsflow Backend
## Nền tảng Thương mại điện tử toàn diện và bảo mật triển khai trên AWS

### 1. Tóm tắt điều hành
**Shopsflow** là một dự án nền tảng thương mại điện tử (e-commerce) được thiết kế nhằm cung cấp trải nghiệm mua sắm trực tuyến mượt mà và an toàn. Trong phạm vi kỳ thực tập này, dự án tập trung vào việc xây dựng hệ thống **Backend** mạnh mẽ bằng Java Spring Boot, tích hợp quản lý giỏ hàng, xử lý tranh chấp hàng tồn kho khi có nhiều lượng mua cùng lúc, và thanh toán trực tuyến qua VNPay. Toàn bộ hệ thống được thiết kế để triển khai trên hạ tầng đám mây của AWS nhằm đảm bảo tính sẵn sàng cao, bảo mật và dễ dàng mở rộng.

### 2. Tuyên bố vấn đề
**Vấn đề hiện tại**
Các hệ thống bán hàng quy mô nhỏ thường gặp khó khăn trong việc quản lý đồng bộ dữ liệu kho khi có lượng truy cập lớn (over-selling). Ngoài ra, việc tích hợp thanh toán trực tuyến nội địa một cách an toàn (tránh giả mạo webhook, thất thoát dữ liệu) và bảo mật API cho người dùng vẫn là thách thức lớn.

**Giải pháp**
Shopsflow Backend sử dụng:
*   **Java 21 & Spring Boot 4**: Xây dựng các API cốt lõi nhanh chóng và chuẩn mực.
*   **Spring Security & JWT**: Quản lý xác thực và phân quyền truy cập Stateless, an toàn.
*   **Optimistic Locking**: Giải quyết triệt để bài toán tranh chấp dữ liệu tồn kho.
*   **Tích hợp VNPay**: Xử lý thanh toán với cơ chế đối soát chữ ký điện tử SHA512 bảo mật.
*   **AWS Services**: Triển khai trên Amazon EC2, dùng Amazon RDS (PostgreSQL) cho Database để tăng tính ổn định, và Amazon S3 để lưu trữ tài nguyên tĩnh (ảnh sản phẩm).

**Lợi ích và hoàn vốn đầu tư (ROI)**
Giải pháp cung cấp một bộ khung backend hoàn chỉnh, có thể sẵn sàng tích hợp với bất kỳ nền tảng Frontend nào (Web/App). Bằng cách sử dụng AWS Managed Services như RDS, hệ thống giảm thiểu chi phí bảo trì Database thủ công, tập trung vào phát triển tính năng.

### 3. Kiến trúc giải pháp

![Sơ đồ kiến trúc](/images/5-Workshop/5.1-Workshop-overview/diagram1.jpg)

**Dịch vụ AWS sử dụng chính**
- **Amazon VPC**: Thiết lập mạng riêng ảo (Public/Private Subnets) cô lập cơ sở dữ liệu.
- **Amazon EC2**: Triển khai ứng dụng Spring Boot.
- **Amazon RDS (PostgreSQL)**: Cơ sở dữ liệu quan hệ quản lý thông tin User, Product, Order.
- **Amazon S3**: Lưu trữ hình ảnh sản phẩm tĩnh.
- **AWS IAM**: Quản lý quyền truy cập tài nguyên bảo mật.

**Thiết kế thành phần**
- **Security Module**: Xác thực JWT, Role-based Access Control.
- **Catalog Module**: Quản lý danh mục và sản phẩm.
- **Checkout Module**: Quản lý Giỏ hàng, Đơn hàng, tồn kho.
- **Payment Module**: Xử lý tích hợp VNPay và Webhook IPN.

### 4. Triển khai kỹ thuật
**Các giai đoạn triển khai**
Dự án trải qua 4 giai đoạn chính trong 9 tuần:
1. **Thiết kế kiến trúc & Setup**: Lên mô hình CSDL, thiết lập môi trường (Java, DB) và hạ tầng mạng AWS VPC.
2. **Phát triển Core API**: Triển khai JWT, Product/Category CRUD.
3. **Phát triển luồng Checkout**: Giỏ hàng, Order, Optimistic Locking chống Over-selling.
4. **Thanh toán & Đưa lên Cloud**: Tích hợp VNPay Sandbox, viết Unit Test, triển khai lên EC2 và RDS.

**Yêu cầu kỹ thuật**
- Backend: Java 21, Spring Boot, Maven, Flyway (Migration).
- Database: PostgreSQL.
- Cloud: AWS CLI, SSH (EC2), cấu hình Security Groups.

### 5. Lộ trình & Mốc triển khai
- **Tháng 1 (Tuần 1-4)**: Học AWS, thiết kế CSDL, khởi tạo dự án Spring Boot, hoàn thiện Proposal.
- **Tháng 2 (Tuần 5-9)**: Viết API (Cart, Order, Payment), xử lý Concurrency, viết Unit Tests, hoàn thiện tài liệu Blog và đóng gói báo cáo dự án.

### 6. Ước tính ngân sách
*Ước tính chi phí AWS cho môi trường Dev/Test (áp dụng Free Tier ở mức tối đa):*
- **Amazon EC2 (t3.micro)**: Đang trong Free-tier (nếu còn) hoặc ~8-10 USD/tháng.
- **Amazon RDS (db.t3.micro)**: Đang trong Free-tier hoặc ~15 USD/tháng.
- **Amazon S3**: Lưu trữ siêu nhỏ, chi phí < 0.1 USD/tháng.
- **Data Transfer**: Miễn phí dưới 100GB.
*=> Tổng chi phí tham khảo: ~20-25 USD/tháng nếu hết Free-tier.*

### 7. Đánh giá rủi ro
**Ma trận rủi ro**
- Rò rỉ cấu hình Database/Secret Key: Ảnh hưởng cao, xác suất thấp.
- Lỗi logic thanh toán VNPay: Ảnh hưởng cao, xác suất trung bình.
- Hết hạn Free-tier AWS: Ảnh hưởng trung bình.

**Chiến lược giảm thiểu**
- Không đưa thông tin nhạy cảm lên GitHub, sử dụng Parameter Store hoặc Environment Variables.
- Viết Unit Test kỹ lưỡng (`VnPayServiceTest`) và log request cẩn thận.
- Cài đặt **AWS Budgets** để cảnh báo khi chi phí vượt quá $1.

### 8. Kết quả kỳ vọng
- Một Backend hoàn chỉnh có khả năng xử lý mua hàng và thanh toán thực tế.
- Khả năng tích hợp an toàn với Frontend.
- Nâng cao kỹ năng lập trình Java, thao tác với Cloud AWS và quản lý hệ thống.