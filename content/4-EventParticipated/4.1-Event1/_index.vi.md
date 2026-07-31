---
title: "Event 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

# Bài thu hoạch “GenAI-powered App-DB Modernization workshop”

### Mục Đích Của Sự Kiện

- Chia sẻ best practices trong thiết kế ứng dụng hiện đại
- Giới thiệu phương pháp DDD và event-driven architecture
- Hướng dẫn lựa chọn compute services phù hợp
- Giới thiệu công cụ AI hỗ trợ development lifecycle

### Danh Sách Diễn Giả

- **Jignesh Shah** - Director, Open Source Databases
- **Erica Liu** - Sr. GTM Specialist, AppMod
- **Fabrianne Effendi** - Assc. Specialist SA, Serverless Amazon Web Services

### Nội Dung Nổi Bật

#### Những hạn chế của kiến trúc ứng dụng cũ

- Thời gian release sản phẩm lâu → mất doanh thu/bỏ lỡ cơ hội
- Hoạt động kém hiệu quả → mất năng suất, tốn kém chi phí
- Không tuân thủ các quy định về bảo mật → mất an ninh, uy tín

#### Chuyển đổi sang microservices

Chuyển đổi thành hệ thống modular – từng chức năng là một **dịch vụ độc lập** giao tiếp với nhau qua **sự kiện**, dựa trên 3 trụ cột cốt lõi:

- **Queue Management**: xử lý tác vụ bất đồng bộ
- **Caching Strategy**: tối ưu hiệu năng
- **Message Handling**: giao tiếp linh hoạt giữa các service

#### Domain-Driven Design (DDD)

- **Phương pháp 4 bước**: xác định domain events → sắp xếp timeline → xác định actor → xác định bounded context
- **Case study bookstore**: minh họa cách áp dụng DDD thực tế
- **Context mapping**: 7 pattern để tích hợp các bounded context

#### Event-Driven Architecture

- **3 pattern tích hợp**: Publish/Subscribe, Point-to-point, Streaming
- **Lợi ích**: loose coupling, khả năng mở rộng, khả năng phục hồi
- **So sánh sync vs async**: hiểu rõ sự đánh đổi (trade-off)

#### Compute Evolution

- **Dải trách nhiệm chia sẻ**: EC2 → ECS → Fargate → Lambda
- **Lợi ích của serverless**: không cần quản lý server, tự động scale, trả phí theo mức sử dụng
- **Functions vs Containers**: tiêu chí lựa chọn phù hợp

#### Amazon Q Developer

- **Tự động hóa SDLC**: từ lập kế hoạch đến bảo trì
- **Code transformation**: nâng cấp Java, hiện đại hóa .NET
- **AWS Transform agents**: di trú VMware, Mainframe, .NET

### Bài Học Rút Ra

- **Thiết kế từ business trước**: luôn bắt đầu từ domain nghiệp vụ và một ngôn ngữ chung (ubiquitous language) giữa business và tech, thay vì bắt đầu từ công nghệ.
- **Event storming**: kỹ thuật thực tế để mô hình hóa quy trình nghiệp vụ thành domain event, từ đó tách thành các microservice với bounded context rõ ràng.
- **Ưu tiên event-driven hơn đồng bộ**: giao tiếp bất đồng bộ theo hướng sự kiện giúp giảm coupling, tăng khả năng mở rộng và phục hồi; cần biết khi nào dùng pub/sub, point-to-point hay streaming.
- **Chọn compute phù hợp quy mô**: lựa chọn giữa VM → container → serverless dựa trên đặc điểm khối lượng công việc, không nên mặc định một lựa chọn.
- **Hiện đại hóa theo từng giai đoạn**: áp dụng khung 7Rs với lộ trình rõ ràng và đo lường được ROI — việc viết lại toàn bộ hệ thống trong một lần là rủi ro cao.

### Ứng Dụng Vào Công Việc

- **Áp dụng DDD** cho dự án hiện tại: tổ chức các buổi event storming cùng team business
- **Refactor microservices**: dùng bounded context để xác định ranh giới service
- **Áp dụng event-driven pattern**: thay thế một số lệnh gọi đồng bộ bằng messaging bất đồng bộ
- **Thử nghiệm serverless**: dùng AWS Lambda cho các use case phù hợp
- **Thử Amazon Q Developer**: tích hợp vào quy trình phát triển để tăng năng suất

### Trải Nghiệm Cá Nhân

Tham gia workshop **“GenAI-powered App-DB Modernization”** giúp tôi có cái nhìn rõ ràng hơn nhiều về cách các hệ thống cũ thực sự được hiện đại hóa trong thực tế, thay vì chỉ đọc lý thuyết trên mạng. Việc nghe các chuyên gia AWS trình bày qua case study thực tế — chứ không chỉ là slide — giúp các khái niệm như DDD và event-driven architecture trở nên dễ hình dung hơn hẳn.

Phần hữu ích nhất là bài tập event storming: nhìn thấy một quy trình nghiệp vụ được phân rã từng bước thành các domain event giúp tôi hiểu bounded context như một công cụ thiết kế cụ thể, chứ không còn là khái niệm trừu tượng. Tôi cũng hiểu rõ hơn khi nào *không nên* dùng microservices hay serverless — các diễn giả nhấn mạnh đây là những sự đánh đổi, không phải lựa chọn nâng cấp mặc định cho mọi trường hợp.

Tôi dự định mang tư duy business-first và thói quen tự hỏi "nên đồng bộ hay bất đồng bộ, và vì sao" vào công việc dự án của mình sau này.

#### Một số hình ảnh khi tham gia sự kiện
*Thêm các hình ảnh của bạn tại đây*
