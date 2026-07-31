---
title: "Dọn dẹp"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 5.4. </b> "
---

### Dọn dẹp

_Xóa tài nguyên theo thứ tự ngược lại với thứ tự tạo — xóa các tài nguyên phụ thuộc trước, tài nguyên nền tảng sau cùng — để tránh lỗi phụ thuộc._

### 1. CloudWatch — xóa Alarms, Metric Filters, Log Groups, SNS

1. Vào CloudWatch Console → **Alarms** → chọn cả 3 alarm (`common-metric`, `http-4xx-count`, `http-5xx-count`) → **Actions → Delete**

![Alarms deletion](alarms.png)

2. Vào CloudWatch Console → **Log groups** → `/diyshop/app` → tab **Metric filters** → xóa filter `common-metric`; lặp lại với `/diyshop/access` (xóa `http-4xx-count`, `http-5xx-count`)

![alt text](image.png)

3. Xóa cả hai Log Group: `/diyshop/app`, `/diyshop/access` → **Actions → Delete log group(s)**

![alt text](image-1.png)

4. Vào SNS Console → **Topics** → chọn `diyshop-alerts` → **Delete** (subscription email đã đính kèm sẽ tự động bị xóa cùng với topic)

![alt text](image-2.png)

### 2. EC2 — terminate instance + release Elastic IP

1. Vào EC2 Console → **Instances** → chọn `diyshop-app-server` → **Instance state → Terminate instance**
2. **Lưu ý quan trọng — dễ bị bỏ sót, gây phát sinh chi phí liên tục:** terminate instance **không** tự động giải phóng Elastic IP. Vào EC2 Console → **Elastic IPs** → chọn IP vừa không còn được gắn (unassociated) → **Actions → Release Elastic IP address** (tùy theo cấu hình của bạn)

![alt text](image-3.png)

### 3. S3 — empty bucket trước khi xóa

1. Vào S3 Console → chọn bucket `diyshop-s3-bucket-...` → **Empty** (nhập tên bucket để xác nhận) — bucket còn chứa object thì không thể xóa trực tiếp
2. Sau khi bucket rỗng → **Delete** bucket (nhập tên bucket để xác nhận lần nữa)

![alt text](image-4.png)

### 4. IAM — xóa Role và Policy

1. Vào IAM Console → **Roles** → `diyshop-ec2-role` → tab **Permissions** → **Detach** policy `diyshop-s3-product-images-policy` trước
2. Xóa role: **Roles** → chọn `diyshop-ec2-role` → **Delete**

![alt text](image-5.png)

3. Xóa policy: **Policies** → chọn `diyshop-s3-product-images-policy` → **Delete**

![alt text](image-6.png)

### 5. RDS — xóa DB instance

1. Vào RDS Console → **Databases** → chọn `diyshop-db-instance` → **Modify** → nếu **Deletion protection** đang bật thì tắt trước, sau đó **Apply**
2. **Actions → Delete**
3. Tùy chọn: chọn **"Create final snapshot"** nếu bạn muốn backup trước khi xóa (khuyến nghị cho môi trường production thực tế, không bắt buộc cho lab này), hoặc bỏ chọn nếu chỉ dùng cho môi trường test
4. Nhập `delete me` để xác nhận → **Delete**

![alt text](image-8.png)

5. Sau khi instance đã bị xóa, xóa luôn **DB Subnet Group** (`rds-subnet-group`) trong mục Subnet groups

![alt text](image-9.png)

### 6. Security Groups — xóa các SG tự tạo

1. Vào VPC Console → **Security Groups** → xóa `EC2-WebApp-SG` và `SG-RDSPostgreSQL`
2. **Không xóa** security group `default` của VPC — vì đây không phải là group được tạo thủ công nên không cần xóa

![alt text](image-10.png)

### 7. VPC Endpoint

1. Vào VPC Console → **Endpoints** → chọn `diy-vpce-s3` (hoặc tên được tự động sinh nếu bạn tạo bằng wizard "VPC and more") → **Delete VPC endpoints**

![alt text](image-11.png)

### 8. VPC — xóa toàn bộ (bước cuối cùng)

1. Vào VPC Console → **Your VPCs** → chọn `diy-vpc` → **Actions → Delete VPC**
2. Console sẽ liệt kê toàn bộ tài nguyên con còn lại (subnet, route table, Internet Gateway) và xóa tất cả cùng lúc sau khi xác nhận — đây là bước dọn dẹp cuối cùng

![alt text](image-12.png)

---

**Kiểm tra sau khi dọn dẹp:** Vào Billing Console → xác nhận không còn tài nguyên nào liên quan đến `diy-vpc`/`diyshop-*` đang phát sinh chi phí; vào VPC Console → **Your VPCs** → xác nhận `diy-vpc` không còn xuất hiện trong danh sách.
