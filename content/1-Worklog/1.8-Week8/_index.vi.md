---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 8:

* Khởi tạo VPC, subnet, và Security Group cho DIY Shop.
* Khởi chạy RDS PostgreSQL và EC2, thiết lập kết nối an toàn giữa hai dịch vụ.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | -------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tạo VPC với 2 public + 2 private subnet trên 2 AZ <br> - Cấu hình route table & IGW                       | 29/09/2025   | 29/09/2025      | <https://docs.aws.amazon.com/vpc/> |
| 3   | - Tạo Security Group: EC2 (public, inbound HTTP/SSH) và RDS (private, chỉ nhận inbound từ EC2 SG)           | 30/09/2025   | 30/09/2025      |
| 4   | - Khởi tạo RDS PostgreSQL (`db.t4g.micro`) trong private subnet                                             | 01/10/2025   | 01/10/2025      | <https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.html> |
| 5   | - Khởi chạy EC2 instance (`t3.micro`) trong public subnet <br> - Gắn Elastic IP                              | 02/10/2025   | 02/10/2025      |
| 6   | - Kiểm tra kết nối an toàn EC2→RDS qua mạng nội bộ <br> - Chạy `flyway migrate` lên RDS thật                 | 03/10/2025   | 03/10/2025      |


### Kết quả đạt được tuần 8:

* Hoàn thành mô hình VPC/subnet/Security Group trải rộng trên 2 Availability Zone.
* RDS PostgreSQL chỉ có thể truy cập từ tầng ứng dụng, không thể truy cập từ internet công cộng.
* Schema ứng dụng được migrate thành công lên RDS thật thông qua Flyway.
* ...
