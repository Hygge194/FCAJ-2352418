---
title: "Worklog Tuần 6"
date: 2026-07-20
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Phát triển API Giỏ hàng (Cart) và Đơn hàng (Order), hoàn tất luồng Checkout.
* Xử lý vấn đề tranh chấp số lượng sản phẩm tồn kho khi có nhiều người mua hàng đồng thời (Concurrency Control).
* Phát triển API Đánh giá sản phẩm (Product Reviews) và viết Unit Tests nghiệp vụ.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành |
| :---: | :--- | :---: | :---: |
| **2** | - Phát triển API Giỏ hàng (Cart Controller & Service), xử lý logic thêm sản phẩm, cập nhật số lượng và xóa sản phẩm | 20/07/2026 | 20/07/2026 |
| **3** | - Phát triển API Đơn hàng (Order Controller & Service), tự động chuyển đổi giỏ hàng hiện tại thành Đơn hàng với trạng thái `PENDING` | 21/07/2026 | 21/07/2026 |
| **4** | - Triển khai cơ chế khóa lạc quan (Optimistic Locking) bằng cách thêm cột `@Version` trong entity Product để kiểm soát số lượng tồn kho | 22/07/2026 | 22/07/2026 |
| **5** | - Viết API Review sản phẩm (chỉ người mua mới được review, người viết mới được sửa/xóa review của mình) | 23/07/2026 | 23/07/2026 |
| **6** | - Viết Unit Tests bằng Mockito cho các Services cốt lõi (`CartService`, `OrderService`, `ProductService`) đảm bảo logic hoạt động chính xác | 24/07/2026 | 24/07/2026 |

### Kết quả đạt được tuần 6:

* Hoàn thiện luồng Cart và Checkout tạo đơn hàng thông suốt.
* Khắc phục triệt để hiện tượng Over-selling (bán quá số lượng tồn kho thực tế) bằng Optimistic Locking.
* API Review sản phẩm và bộ Unit Tests nghiệp vụ backend chính được viết đầy đủ với độ bao phủ cao.