---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 5:

* Xây dựng REST API cho catalog sản phẩm và cho việc đặt/tra cứu đơn hàng.
* Tìm hiểu Spring Security để bảo vệ seller portal (form login + CSRF).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                          | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ---------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Cài đặt `GET /api/products` và `GET /api/products/{id}` kèm DTO mapping                              | 08/09/2025   | 08/09/2025      |
| 3   | - Cài đặt `POST /api/orders` (chọn COD/VietQR) và `GET /api/orders/{code}` để tra cứu đơn hàng          | 09/09/2025   | 09/09/2025      |
| 4   | - Tìm hiểu Spring Security cơ bản: filter chain, authentication, authorization                          | 10/09/2025   | 10/09/2025      | <https://docs.spring.io/spring-security/reference/> |
| 5   | - Cấu hình form login + bảo vệ CSRF cho các route `/seller/**`                                          | 11/09/2025   | 11/09/2025      |
| 6   | - Viết integration test cho controller sản phẩm & đơn hàng bằng MockMvc                                 | 12/09/2025   | 12/09/2025      |


### Kết quả đạt được tuần 5:

* REST API hoạt động end-to-end: xem catalog, checkout (COD/VietQR), tra cứu đơn hàng theo mã.
* Các route seller portal được bảo vệ bằng form-login kèm CSRF.
* Integration test cho tầng controller chạy ổn định trong local build.
* ...
