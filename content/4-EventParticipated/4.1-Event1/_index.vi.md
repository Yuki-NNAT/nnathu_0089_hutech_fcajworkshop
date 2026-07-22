---
title: "Event 1"
date: 2026-07-07
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch “AWS FIRST CLOUD AI JOURNEY COMMUNITY DAY”

### Mục Đích Của Sự Kiện

-	Cập nhật các xu hướng thực tiễn về Cloud Computing và cách ứng dụng Generative AI (GenAI) vào môi trường doanh nghiệp.
-	Chia sẻ các best practices trong việc thiết kế kiến trúc phần mềm nền tảng, xây dựng hệ thống đa tác vụ (multi-agent) và bảo mật hạ tầng mạng.
-	Tạo không gian kết nối cộng đồng IT, truyền cảm hứng và định hướng bộ kỹ năng cần thiết cho kỹ sư trong kỷ nguyên AI.


### Danh Sách Diễn Giả

-	**Nguyễn Gia Hưng** - Solutions Architect, AWS Vietnam (Founder FCAJ)
-	**Tinh Truong** - Platform Engineer, GoTymeX
-	**Anh Pham** - Cloud Consultant, G-AsiaPacific Vietnam
-	**Thinh Nguyen** - DevOps Engineer, FCAJ
-	**Uyển Lê, Thảo Nguyễn, Mai Nguyễn** - GenAI Engineers, VIB
-	**Duc Dao** - Solutions Architect, Cloud Kinetics
-	**Vy Lâm** - Senior Business Systems Analyst, VPBank


### Nội Dung Nổi Bật

####	Xu hướng việc làm & Mindset của Kỹ sư IT:
Sự tiến bộ của AI làm giảm rào cản chi phí phát triển phần mềm, kéo theo nhu cầu sản xuất sản phẩm tăng vọt. Kỹ sư cần hiểu bài toán nghiệp vụ (business use case) và phải có sản phẩm thực tế minh chứng năng lực thay vì chỉ dựa vào lý thuyết.
#### Tối ưu hóa ngữ cảnh (Context) trong AI:
Để AI không cung cấp các phản hồi rác (hallucination), kỹ sư cần nạp ngữ cảnh cụ thể và giới hạn thông tin thay vì nhồi nhét tài liệu đại trà trên internet (hội chứng "Internet Builder").
####	Tự động hóa với Amazon Q (AI Agent):

Ứng dụng trợ lý ảo để phân tích file Excel, tạo dashboard BI và tóm tắt cuộc họp tự động thông qua việc kết nối hệ sinh thái công sở bằng MCP (Model Context Protocol).
####	Kiến trúc mạng và Bảo mật với Amazon CloudFront:
Giới thiệu giải pháp Flat-rate pricing giúp doanh nghiệp ngăn chặn rủi ro "bill shock" (chi phí tăng vọt do lượng truy cập bất thường hoặc bị tấn công DDoS). Sử dụng mạng lưới Point of Presence (PoP) của AWS để phân tán lưu lượng và bảo vệ hạ tầng gốc với VPC Origin, cho phép kết nối thẳng từ CloudFront vào private subnet, giấu kín hệ thống khỏi mạng internet public.
####	Kinh nghiệm thực chiến Hackathon & Phát triển sản phẩm GenAI (UTM Morpo):
Chia sẻ quá trình xây dựng dự án sinh giao diện người dùng (UI) trong 36 giờ bằng kiến trúc Serverless phối hợp 3 AI Agent. Nhóm đã giải quyết bài toán tốn thời gian và token khi nhờ AI generate lại toàn bộ UI bằng cách phát triển tính năng cho phép chỉnh sửa trực tiếp component và CSS ngay trên giao diện. Từ đó, nhóm đúc kết các bài học quản lý rủi ro khi dùng AI (hết token, sinh code thừa) và chiến lược tập trung vào tính năng cốt lõi thay vì "nhồi nhét" ý tưởng.
####	Kiểm soát tính định hướng (Deterministic) của mô hình LLM:
Giải thích cơ chế hoạt động của LLM và phân tích thực tế rằng ngay cả khi cài đặt Temperature = 0, kết quả đầu ra đôi khi vẫn biến thiên do giới hạn phần cứng (GPU) và cơ chế tối ưu hóa suy luận của nhà cung cấp. Do đó, cần có chiến lược giảm thiểu rủi ro như chạy nhiều lần để bầu chọn kết quả, tự host model, sử dụng JSON mode, và đặc biệt là thiết kế các luồng (downstream services) linh hoạt để xử lý lỗi ngẫu nhiên của AI.
####	Thiết kế Enterprise-Grade Multi-Agent System:
Xây dựng hệ thống nhiều AI Agent chuyên biệt phối hợp để đánh giá tín dụng doanh nghiệp startup. Quá trình này đặc biệt đề cao các yếu tố bảo mật doanh nghiệp (Security & Compliance) thông qua việc kiểm soát vector tấn công MCP, ngăn chặn Prompt Injection, xây dựng tính năng lưu vết hệ thống (Audit Trail) và thiết lập quy trình luân chuyển khóa (API Key Rotation).


### Những Gì Học Được

- **Tư Duy Kỹ Thuật Hướng Nghiệp Vụ:** 
Luôn tiếp cận vấn đề từ bài toán kinh doanh và trải nghiệm người dùng thực tế. Việc chia nhỏ hệ thống thành các AI Agent hoặc tập trung giải quyết triệt để một nỗi đau cốt lõi (như tính năng edit UI thay vì generate liên tục) mang lại giá trị cao hơn.

- **Kiến Trúc Kỹ Thuật & An Toàn Thông Tin:** 
Nắm bắt được phương pháp thiết lập chốt chặn an toàn với CloudFront. Tính năng VPC Origin là một bước tiến đột phá để cô lập kiến trúc backend khỏi các rủi ro từ internet.

- **Kiểm soát rủi ro từ hệ thống AI (AI Risk Management):** 
Hiểu được bản chất xác suất của LLM để không tin tưởng mù quáng vào kết quả trả về. Luôn phải lường trước các kịch bản AI bị "ảo giác" (hallucinate), hết token giới hạn, hoặc phản hồi sai định dạng để có cơ chế dự phòng.


### Ứng Dụng Vào Công Việc

-	Hệ thống Multi-Agent: Chia nhỏ thành các Agent độc lập (phân tích sở thích, tìm công thức, tính dinh dưỡng) để gợi ý cá nhân hóa chính xác hơn. 
-	Tối ưu luồng sinh nội dung: Chỉ update cục bộ (edit) một nguyên liệu khi người dùng yêu cầu thay đổi thay vì generate lại toàn bộ công thức để tiết kiệm token. 
-	Kiểm soát định dạng (Deterministic): Thiết lập Temperature thấp và ép JSON mode để dữ liệu trả về (tên món, nguyên liệu, cách làm) luôn đúng chuẩn. 
-	Bảo mật & Context: Dùng CloudFront và VPC Origin bảo vệ database. Truyền ngữ cảnh giới hạn (chỉ gửi nguyên liệu người dùng đang có) vào prompt để tránh Prompt Injection. 


### Trải nghiệm trong event

Tham gia sự kiện **“AWS FIRST CLOUD AI JOURNEY COMMUNITY DAY”** là một trải nghiệm rất bổ ích, giúp em có cái nhìn toàn diện về cách kết hợp giữa các dịch vụ Cloud AWS và sức mạnh của Generative AI để xây dựng các ứng dụng an toàn, ổn định. Một số trải nghiệm nổi bật:

#### Học hỏi từ các diễn giả có chuyên môn cao

-	Các chuyên gia, kỹ sư đến từ AWS, VIB, GoTymeX, và Cloud Kinetics đã chia sẻ những kinh nghiệm thực chiến đắt giá trong việc thiết kế và phát triển phần mềm hiện đại.
-	Qua các case study thực tế (như bài toán Hackathon 36 giờ hay hệ thống đánh giá tín dụng startup), tôi hiểu sâu hơn về cách ứng dụng kiến trúc Multi-Agent để giải quyết các luồng nghiệp vụ phức tạp thay vì chỉ phụ thuộc vào một mô hình đơn lẻ.


#### Trải nghiệm kỹ thuật thực tế

-	Được phân tích sâu về cơ chế hoạt động của LLM, giúp tôi lý giải được lý do AI "ảo giác" (hallucination) và hiểu cách tham số Temperature, JSON mode tác động đến tính nhất quán của dữ liệu đầu ra.
-	Hình dung rõ ràng quy trình bảo mật hạ tầng mạng bằng Amazon CloudFront và VPC Origin để cô lập các backend quan trọng, bảo vệ hệ thống khỏi các đợt tấn công DDoS hay rủi ro cạn kiệt chi phí ("bill shock").
-	Nắm bắt được khái niệm MCP (Model Context Protocol) và các rủi ro bảo mật đi kèm như Prompt Injection hay MCP Attack Vectors khi cấp quyền cho AI tương tác với hệ thống.

#### Bài học rút ra
-	Việc chia nhỏ luồng xử lý AI thành các Agent chuyên biệt giúp giảm thiểu sai sót, tăng cường khả năng mở rộng (scalability) và dễ dàng gỡ lỗi cho hệ thống.
-	Không bao giờ tin tưởng tuyệt đối vào kết quả của AI. Cần áp dụng các chiến lược kiểm soát (như chạy nhiều lần để bầu chọn kết quả) và thiết kế hệ thống luôn có kịch bản dự phòng khi AI trả về dữ liệu lỗi.
-	Bảo mật là yếu tố sống còn khi đưa ứng dụng GenAI vào môi trường thực tế (production). Việc giới hạn quyền truy cập hạ tầng bằng CloudFront/VPC Origin và thiết lập quy trình luân chuyển khóa API (API Key Rotation) là những tiêu chuẩn bắt buộc phải tuân thủ.

#### Một số hình ảnh khi tham gia sự kiện
* Thêm các hình ảnh của các bạn tại đây

![Event 1](/images/4-Event/Event1.jpg)