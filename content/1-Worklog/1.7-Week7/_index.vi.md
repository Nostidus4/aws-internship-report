---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 7:

* Xây dựng trang catalog sản phẩm, giỏ hàng, và checkout.
* Tích hợp frontend với REST API backend, và bundle frontend vào thư mục `static/` của Spring Boot.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                        | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------| ------------ | --------------- | ----------------------------------------- |
| 2   | - Xây dựng trang danh sách & chi tiết sản phẩm <br> - Viết API client có kiểu (fetch + TS interface)     | 22/09/2025   | 22/09/2025      |
| 3   | - Xây dựng trang Giỏ hàng (state local) và form Checkout (COD/VietQR)                                    | 23/09/2025   | 23/09/2025      |
| 4   | - Xây dựng trang Tra cứu đơn hàng (tìm theo mã đơn)                                                       | 24/09/2025   | 24/09/2025      |
| 5   | - Cấu hình Vite build xuất vào `src/main/resources/static` (same-origin, không cần CORS)                 | 25/09/2025   | 25/09/2025      | <https://vitejs.dev/config/build-options.html> |
| 6   | - Xây dựng khung Seller Dashboard (giao diện quản lý sản phẩm & đơn hàng)                                 | 26/09/2025   | 26/09/2025      |


### Kết quả đạt được tuần 7:

* Luồng khách hàng hoạt động end-to-end trên local: xem sản phẩm → giỏ hàng → checkout → tra cứu đơn hàng.
* Frontend được bundle trực tiếp vào file jar của Spring Boot, chạy same-origin, không cần cấu hình CORS.
* Khung Seller Dashboard đã sẵn sàng để kết nối với API quản lý sản phẩm/đơn hàng.
* ...
