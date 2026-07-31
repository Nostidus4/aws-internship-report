---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 9:

* Cấu hình Amazon S3 với IAM role least-privilege để lưu trữ ảnh sản phẩm.
* Triển khai ứng dụng Spring Boot trên EC2 dưới dạng `systemd` service.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                            | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | --------------------------------------------------------------------------------------------------------| ------------ | --------------- | ----------------------------------------- |
| 2   | - Tạo S3 bucket để lưu ảnh sản phẩm <br> - Cấu hình bucket policy ở chế độ private                          | 06/10/2025   | 06/10/2025      |
| 3   | - Tạo IAM Role least-privilege (chỉ `PutObject`/`GetObject`) <br> - Gắn vào instance profile của EC2         | 07/10/2025   | 07/10/2025      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html> |
| 4   | - Cài đặt upload ảnh & sinh presigned URL trong backend (AWS SDK for Java)                                  | 08/10/2025   | 08/10/2025      | <https://docs.aws.amazon.com/sdk-for-java/> |
| 5   | - Build file jar triển khai và deploy lên EC2 <br> - Kiểm thử thực tế việc upload ảnh end-to-end             | 09/10/2025   | 09/10/2025      |
| 6   | - Viết file `systemd` unit <br> - Cấu hình ứng dụng chạy dưới dạng managed service, tự khởi động lại         | 10/10/2025   | 10/10/2025      |


### Kết quả đạt được tuần 9:

* Ảnh sản phẩm được lưu trữ trên S3 hoàn toàn thông qua IAM role least-privilege, đã kiểm thử thực tế.
* Backend sinh presigned URL nên frontend không bao giờ truy cập S3 trực tiếp.
* Ứng dụng chạy ổn định dưới dạng `systemd` service trên EC2, tự khởi động lại khi gặp lỗi.
* ...
