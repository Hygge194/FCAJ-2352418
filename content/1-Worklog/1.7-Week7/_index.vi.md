---
title: "Worklog Tuần 7"
date: 2026-07-27
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Tích hợp cổng thanh toán trực tuyến VNPay Sandbox cho luồng thanh toán đơn hàng Shopsflow.
* Triển khai endpoint xử lý Return URL và Webhook IPN (Instant Payment Notification) để tự động cập nhật trạng thái đơn hàng và xử lý hoàn kho khi thất bại.
* Tài liệu hóa luồng thanh toán VNPay, viết kịch bản Clean-up và hoàn tất kiểm thử tích hợp.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành |
| :---: | :--- | :---: | :---: |
| **2** | - Nghiên cứu tài liệu cổng thanh toán VNPay Sandbox, lấy thông tin tài khoản test và cấu hình các biến môi trường (`VNPAY_TMN_CODE`, `VNPAY_HASH_SECRET`, `VNPAY_API_URL`, `VNPAY_RETURN_URL`) vào file `.env` | 27/07/2026 | 27/07/2026 |
| **3** | - Viết lớp tiện ích `VnPayUtil` để sinh chữ ký bảo mật SHA512 và xây dựng API endpoint tạo liên kết thanh toán (`createPaymentUrl`) gửi từ Backend | 28/07/2026 | 28/07/2026 |
| **4** | - Triển khai các API xử lý phản hồi: Return URL (hiển thị kết quả giao diện người dùng) và Webhook IPN (cập nhật đơn hàng thành `PAID` hoặc `CANCELLED`, hoàn kho sản phẩm nếu thanh toán thất bại/hủy) | 29/07/2026 | 29/07/2026 |
| **5** | - Thực hiện chạy thử nghiệm giao dịch sử dụng các số thẻ test ngân hàng Sandbox của VNPay; viết tài liệu hướng dẫn tích hợp VNPay (`VNPAY_INTEGRATION.md`) | 30/07/2026 | 30/07/2026 |
| **6** | - Viết Unit Tests kiểm thử logic thanh toán của `VnPayService` (`VnPayServiceTest`), chạy Maven test tích hợp toàn diện backend và viết kịch bản Clean-up | 31/07/2026 | 31/07/2026 |

### Kết quả đạt được tuần 7:

* Tích hợp thành công cổng thanh toán trực tuyến VNPay Sandbox vào luồng đặt hàng của Shopsflow.
* Xây dựng thành công cơ chế đối soát, xác thực chữ ký SHA512 của VNPay khi nhận thông tin callback IPN giúp giao dịch diễn ra an toàn.
* Hoàn thành tài liệu hướng dẫn kết nối Frontend (`VNPAY_INTEGRATION.md`) giúp đội ngũ phát triển giao diện React dễ dàng hoàn thiện màn hình kết quả thanh toán.
* Toàn bộ hệ thống Backend đạt tiêu chí kiểm thử End-to-End và có kịch bản Clean-up tài nguyên hoàn chỉnh.