---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 2:

* Tiếp tục tìm hiểu các dịch vụ AWS nền tảng: VPC, Security Group, S3, IAM.
* Xem lại yêu cầu dự án DIY Shop và phác thảo sơ bộ kiến trúc AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                        | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | -------------------------------------------------------------------------------------------------------------------| ------------ | --------------- | ----------------------------------------- |
| 2   | - Xem lại bản nháp đề xuất DIY Shop (catalog sản phẩm, đơn hàng, thanh toán COD/VietQR) <br> - Phác thảo yêu cầu hệ thống ban đầu | 18/08/2025   | 18/08/2025      |
| 3   | - Tìm hiểu nền tảng VPC: CIDR, subnet, route table, Internet Gateway/NAT Gateway                                    | 19/08/2025   | 19/08/2025      | <https://docs.aws.amazon.com/vpc/> |
| 4   | - Tìm hiểu Security Group & NACL, thực hành viết rule inbound/outbound theo nguyên tắc least-privilege               | 20/08/2025   | 20/08/2025      | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html> |
| 5   | - Tìm hiểu Amazon S3 cơ bản: bucket, storage class, bucket policy, presigned URL                                     | 21/08/2025   | 21/08/2025      | <https://docs.aws.amazon.com/s3/> |
| 6   | - Tìm hiểu IAM: user/role/policy, nguyên tắc least-privilege <br> - **Thực hành:** tạo IAM role cho EC2 instance      | 22/08/2025   | 22/08/2025      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html> |


### Kết quả đạt được tuần 2:

* Hiểu nền tảng VPC, Security Group, S3, IAM và cách chúng phối hợp để bảo mật hệ thống.
* Phác thảo sơ bộ kiến trúc DIY Shop (EC2 + RDS + S3) dựa trên đề xuất dự án.
* Cài đặt môi trường phát triển local: JDK 17, Node.js, Git, AWS CLI.
* Tạo và kiểm thử thành công IAM role least-privilege đầu tiên gắn cho EC2 instance.
* ...
