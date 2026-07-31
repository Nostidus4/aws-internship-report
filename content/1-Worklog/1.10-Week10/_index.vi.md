---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 10:

* Cấu hình CloudWatch Agent, log group, metric filter, và alarm kèm cảnh báo email qua SNS.
* Xây dựng pipeline CI/CD với GitHub Actions để tự động build, test và deploy.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | -------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Cài đặt & cấu hình CloudWatch Agent trên EC2 <br> - Đẩy log ứng dụng/access log vào Log Group             | 13/10/2025   | 13/10/2025      | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html> |
| 3   | - Tạo Metric Filter để tính metric số lượng lỗi từ log ứng dụng                                             | 14/10/2025   | 14/10/2025      |
| 4   | - Tạo CloudWatch Alarm dựa trên metric lỗi <br> - Tạo SNS topic + đăng ký nhận email                        | 15/10/2025   | 15/10/2025      | <https://docs.aws.amazon.com/sns/latest/dg/welcome.html> |
| 5   | - Viết workflow GitHub Actions: build & test bằng PostgreSQL service container                              | 16/10/2025   | 16/10/2025      | <https://docs.github.com/actions> |
| 6   | - Mở rộng workflow để tự động deploy lên EC2 mỗi khi push lên `main`                                        | 17/10/2025   | 17/10/2025      |


### Kết quả đạt được tuần 10:

* CloudWatch tập trung log ứng dụng và access log, metric filter tính ra metric lỗi theo thời gian thực.
* Xác nhận alarm gửi email cảnh báo thật qua SNS khi tỷ lệ lỗi vượt ngưỡng.
* Mỗi lần push lên `main` đều được tự động build, test với PostgreSQL container, và deploy lên EC2.
* ...
