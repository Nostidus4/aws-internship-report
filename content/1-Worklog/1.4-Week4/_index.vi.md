---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 4:

* Thiết kế domain model cốt lõi (Product, Category, Order, Customer) với Spring Data JPA.
* Tiếp tục xây dựng schema thông qua các migration Flyway.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | -----------------------------------------------------------------------------------------------------------| ------------ | --------------- | ----------------------------------------- |
| 2   | - Thiết kế entity `Product`/`Category` với JPA annotation và các mối quan hệ                                  | 01/09/2025   | 01/09/2025      | <https://docs.spring.io/spring-data/jpa/reference/> |
| 3   | - Thiết kế entity `Order`/`OrderItem`/`Customer` <br> - Định nghĩa enum trạng thái đơn hàng (pending/paid/shipped/...) | 02/09/2025   | 02/09/2025      |
| 4   | - Viết migration Flyway cho bảng `orders` và `customers` <br> - Seed dữ liệu mẫu để test local                | 03/09/2025   | 03/09/2025      | <https://flywaydb.org/documentation/> |
| 5   | - Cài đặt các repository Spring Data JPA (`ProductRepository`, `OrderRepository`, ...)                        | 04/09/2025   | 04/09/2025      |
| 6   | - Viết unit test cho repository chạy trên PostgreSQL container test                                            | 05/09/2025   | 05/09/2025      |


### Kết quả đạt được tuần 4:

* Schema cốt lõi (product, category, order, order item, customer) đã được migrate đầy đủ qua Flyway.
* Toàn bộ repository được bao phủ bởi unit test chạy trên PostgreSQL container thật.
* Nắm vững cách mapping quan hệ JPA (`@OneToMany`/`@ManyToOne`) và cơ chế cascade.
* ...
