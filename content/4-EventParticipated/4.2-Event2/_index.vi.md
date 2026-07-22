---
title: "Event 2"
date: 2026-07-07
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch sự kiện “FIRST CLOUD JOURNEY COMMUNITY DAY”

### Mục đích của sự kiện

- Giới thiệu các ứng dụng thực tế của AWS trong Cloud, AI, an toàn thông tin và hệ thống thời gian thực.
- Chia sẻ kiến thức về Docker, DevOps, WebSocket, GraphRAG và Machine Learning.
- Giúp sinh viên phát triển kỹ năng chuyên môn, khả năng làm việc nhóm và định hướng nghề nghiệp thông qua kinh nghiệm thực tế.

### Danh sách diễn giả

- **Nguyễn Quốc Bảo** – Ứng dụng nhiều người chơi với Godot và AWS WebSocket
- **Trần Trung Vinh** – System Administrator, Central Retail Group
- **Bảo Huỳnh** – Junior Cloud Native Developer, Endava Vietnam; Founder and Head of ITea Lab
- **Lê Hoàng Gia Đại** – AWS WAF và phát hiện xâm nhập bằng Machine Learning
- **Việt Phát** – Sinh viên ngành AI, Swinburne University of Technology
- **Trương Huy Phước** – Kỹ năng làm việc nhóm hiệu quả

### Nội dung nổi bật

#### Xây dựng ứng dụng thời gian thực với AWS WebSocket

Bài trình bày giới thiệu kiến trúc ứng dụng nhiều người chơi sử dụng Godot, Amazon API Gateway WebSocket, AWS Lambda và Amazon DynamoDB. WebSocket duy trì kết nối thời gian thực, Lambda xử lý logic và DynamoDB lưu trạng thái kết nối cũng như trạng thái trò chơi.

Kiến trúc Serverless này phù hợp với các ứng dụng theo lượt. Những hệ thống cần đồng bộ liên tục với tần suất cao có thể cần dịch vụ chuyên dụng như Amazon GameLift.

#### Định hướng nghề nghiệp Cloud và DevOps

Diễn giả chia sẻ hành trình từ IT Helpdesk đến System Administrator và Cloud–DevOps. Những kiến thức quan trọng bao gồm Linux, mạng máy tính, xử lý sự cố, giám sát, tài liệu hóa, tự động hóa, Docker, CI/CD và Infrastructure as Code.

Bài chia sẻ nhấn mạnh rằng kinh nghiệm từ dự án thực tế và kiến thức chuyên sâu về một số công nghệ cốt lõi có giá trị hơn việc học quá nhiều công cụ nhưng không có đủ thời gian thực hành.

#### Đóng gói ứng dụng bằng Docker

Docker đóng gói ứng dụng cùng với các thư viện cần thiết, giúp hệ thống hoạt động nhất quán trong môi trường phát triển, kiểm thử và triển khai thực tế.

Container nhẹ hơn máy ảo vì sử dụng chung hệ điều hành của máy chủ. Docker đặc biệt phù hợp với triển khai backend, microservices, môi trường kiểm thử và quy trình CI/CD.

#### Kết hợp AWS WAF và Machine Learning

AWS WAF giúp bảo vệ ứng dụng web trước SQL Injection, XSS, bot độc hại, brute force và lưu lượng truy cập bất thường.

Giải pháp được giới thiệu kết hợp AWS WAF với hệ thống phát hiện xâm nhập sử dụng Machine Learning. AWS WAF lọc các mẫu tấn công đã biết, trong khi Machine Learning phân tích hành vi lưu lượng để phát hiện những dấu hiệu bất thường.

Bài trình bày cũng nhấn mạnh tầm quan trọng của việc làm sạch dữ liệu, cân bằng lớp, đánh giá mô hình, ghi log và giám sát bảo mật.

#### GraphRAG với Amazon Bedrock và Neptune

GraphRAG biểu diễn thông tin thông qua các thực thể và mối quan hệ, giúp hệ thống AI trả lời những câu hỏi cần suy luận qua nhiều bước.

Amazon Bedrock có thể hỗ trợ xử lý tài liệu và tạo embedding, trong khi Amazon Neptune lưu trữ và truy vấn đồ thị tri thức. GraphRAG phù hợp với dữ liệu có quan hệ phức tạp nhưng chỉ nên được áp dụng khi RAG thông thường không đáp ứng được yêu cầu.

#### Kỹ năng làm việc nhóm

Một dự án hiệu quả cần có sự phân chia trách nhiệm rõ ràng, trao đổi thường xuyên, theo dõi tiến độ minh bạch và thông báo khó khăn kịp thời.

Các công cụ cộng tác có thể hỗ trợ quản lý công việc và chia sẻ tài liệu, nhưng mỗi thành viên vẫn phải có trách nhiệm hoàn thành phần việc được giao và phối hợp với những thành viên khác.

### Kiến thức và bài học tiếp thu được

#### Lựa chọn kiến trúc phù hợp

Công nghệ cần được lựa chọn dựa trên yêu cầu thực tế của hệ thống. Kiến trúc Serverless WebSocket phù hợp với một số ứng dụng thời gian thực, trong khi những hệ thống có yêu cầu cao hơn có thể cần máy chủ chuyên dụng.

Tương tự, GraphRAG chỉ nên được sử dụng khi mối quan hệ giữa các thực thể dữ liệu mang lại giá trị rõ ràng hơn phương pháp truy xuất thông tin thông thường.

#### Tư duy Cloud và DevOps

Cloud và DevOps không chỉ là việc học cách sử dụng từng công cụ. Quá trình này còn yêu cầu tự động hóa, giám sát, tài liệu hóa, quản lý phiên bản, triển khai có khả năng lặp lại và phối hợp giữa các nhóm.

#### Bảo mật nhiều lớp và chất lượng dữ liệu

Một cơ chế bảo mật duy nhất không thể ngăn chặn mọi mối đe dọa. Việc kết hợp AWS WAF, phân tích hành vi, logging, giám sát và cảnh báo giúp hệ thống được bảo vệ tốt hơn.

Hiệu quả của Machine Learning cũng phụ thuộc nhiều vào chất lượng dữ liệu. Các giá trị không hợp lệ, nhãn sai và tình trạng mất cân bằng lớp cần được xử lý trước khi huấn luyện mô hình.

### Khả năng ứng dụng vào dự án AI Recipe Finder

Những kiến thức tiếp thu từ sự kiện có thể được áp dụng vào dự án **AI Recipe Finder** như sau:

- Đóng gói FastAPI backend bằng Docker để đồng nhất môi trường local và EC2.
- Nghiên cứu CI/CD để tự động hóa kiểm thử và triển khai backend.
- Tài liệu hóa kết nối cơ sở dữ liệu, biến môi trường, Nginx và cấu hình dịch vụ hệ thống.
- Sử dụng AWS WAF để bảo vệ các endpoint công khai trước những cuộc tấn công web phổ biến.
- Theo dõi log của backend và hạ tầng thông qua Amazon CloudWatch.
- Nghiên cứu GraphRAG nếu hệ thống cần phân tích mối quan hệ phức tạp giữa món ăn, nguyên liệu, dinh dưỡng và dị ứng.
- Phân chia rõ trách nhiệm giữa các thành viên phụ trách frontend, backend, database và AI.

### Trải nghiệm tại sự kiện

Tham gia sự kiện **First Cloud Journey Community Day** giúp em tiếp thu thêm nhiều kiến thức hữu ích về kiến trúc Cloud, DevOps, Docker, trí tuệ nhân tạo, an toàn thông tin và kỹ năng làm việc nhóm.

#### Tiếp cận các phần trình diễn thực tế

Phần trình diễn WebSocket giúp em hiểu cách các dịch vụ AWS hỗ trợ ứng dụng thời gian thực. Nội dung về AWS WAF và Machine Learning cho thấy cách kết hợp biện pháp bảo mật truyền thống với phân tích hành vi.

Các bài trình bày về Docker và GraphRAG cũng giới thiệu những giải pháp thực tế cho việc triển khai ứng dụng và xây dựng hệ thống AI có dữ liệu chứa nhiều mối quan hệ phức tạp.

#### Bài học rút ra

- Công nghệ cần được lựa chọn theo yêu cầu thực tế của hệ thống.
- Docker giúp đồng nhất môi trường phát triển và triển khai.
- Cloud và DevOps yêu cầu tự động hóa, giám sát và tài liệu hóa.
- Bảo mật nhiều lớp hiệu quả hơn việc phụ thuộc vào một cơ chế duy nhất.
- Hiệu quả của Machine Learning phụ thuộc nhiều vào chất lượng dữ liệu.
- Kinh nghiệm thực tế và khả năng làm việc nhóm có vai trò quan trọng đối với thành công của dự án.

#### Một số hình ảnh tại sự kiện

![Event 2](/images/4-Event/Event2_1.jpg)
![Event 2](/images/4-Event/Event2_2.jpg)