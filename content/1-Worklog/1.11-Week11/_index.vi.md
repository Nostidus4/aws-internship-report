---
title: "Worklog Tuần 11"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 11:

* Chuyển toàn bộ credential sang Secrets Manager và bật Multi-AZ cho RDS.
* Thêm Application Load Balancer + Auto Scaling Group, và gắn AWS WAF.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | -------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Chuyển credential DB & seller từ file plaintext sang Secrets Manager <br> - Bật automatic rotation        | 20/10/2025   | 20/10/2025      | <https://docs.aws.amazon.com/secretsmanager/> |
| 3   | - Bật Multi-AZ cho RDS instance hiện có <br> - Kiểm tra hành vi failover                                    | 21/10/2025   | 21/10/2025      |
| 4   | - Tạo Application Load Balancer + Target Group <br> - Tạo Auto Scaling Group trải trên 2 AZ                 | 22/10/2025   | 22/10/2025      | <https://docs.aws.amazon.com/elasticloadbalancing/> |
| 5   | - Tạo WAF Web ACL với managed rule group, gắn vào ALB <br> - Thêm rule rate-limit cho endpoint đăng nhập     | 23/10/2025   | 23/10/2025      | <https://docs.aws.amazon.com/waf/> |
| 6   | - Load test hành vi scale-out của Auto Scaling Group <br> - Kiểm tra TLS termination tại ALB                | 24/10/2025   | 24/10/2025      |


### Kết quả đạt được tuần 11:

* Không còn credential dạng plaintext trên EC2; credential DB và seller tự động rotate qua Secrets Manager.
* Loại bỏ single point of failure của RDS nhờ bật Multi-AZ.
* Tầng ứng dụng chạy phía sau ALB có TLS termination, cùng Auto Scaling Group trải trên 2 AZ.
* AWS WAF đang lọc tấn công tầng ứng dụng và rate-limit endpoint đăng nhập.
* ...
