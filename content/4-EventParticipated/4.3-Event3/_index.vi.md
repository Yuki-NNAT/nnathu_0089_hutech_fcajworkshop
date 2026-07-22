---
title: "Event 3"
date: 2026-07-07
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch sự kiện “FCAJ COMMUNITY DAY – DATA DRIVEN, AI RISEN”

### Mục đích của sự kiện

- Cung cấp góc nhìn thực tế về sự phát triển của AI và những ảnh hưởng của công nghệ này đối với hoạt động của doanh nghiệp.
- Giới thiệu cách ứng dụng các giải pháp hiện đại như Voice AI, tự động hóa DevOps và AI trong lĩnh vực tuyển dụng.
- Chia sẻ phương pháp xây dựng kết nối an toàn giữa AI Agent và hệ thống nội bộ thông qua Model Context Protocol (MCP) trên nền tảng AWS.
- Tạo cơ hội để sinh viên và những người làm trong lĩnh vực công nghệ giao lưu, học hỏi kinh nghiệm từ các chuyên gia.

### Danh sách diễn giả

- **Steve Tran** – CTO/Founder, CloudThinker
- **Trung Vu** – CEO, Revve AI
- **Nghi Danh** – AI Engineer, Renova Cloud
- **Kiet Tran** – AI Engineer, AWS Student Builder Group
- **Bao Phan & Nguyen Nguyen** – Cloud Engineers, Cloud Kinetics
- **Truong Tran & Anh Dang** – AI Solution Sales, Noventiq
- **Toan Nguyen** – AWS Security Builder

### Nội dung nổi bật

#### Sự thay đổi trong định hướng nghề nghiệp

Sự phát triển nhanh chóng của AI đang làm thay đổi yêu cầu tuyển dụng trong ngành công nghệ thông tin. Nhiều công việc cơ bản có thể được tự động hóa, trong khi doanh nghiệp ngày càng ưu tiên những nhân sự có kinh nghiệm thực tế và khả năng sử dụng AI để nâng cao hiệu quả công việc.

Qua nội dung chia sẻ, em nhận thấy sinh viên công nghệ thông tin cần chủ động tham gia các dự án thực tế, xây dựng sản phẩm và tích lũy kinh nghiệm càng sớm càng tốt. Bên cạnh kiến thức chuyên môn, khả năng sử dụng AI như một công cụ hỗ trợ cũng đang trở thành một kỹ năng quan trọng.

#### Tự động hóa DevOps và hạ tầng Cloud

Sự kiện giới thiệu DevOps AI Agent có khả năng hỗ trợ kỹ sư phân tích nhật ký hệ thống, tìm hiểu cấu trúc hạ tầng và xác định nguyên nhân gốc rễ của sự cố. Giải pháp này có thể rút ngắn quá trình điều tra từ nhiều giờ xuống còn vài phút trong một số trường hợp.

Tuy nhiên, AI Agent chỉ đóng vai trò phân tích và đề xuất phương án xử lý. Kỹ sư vẫn cần kiểm tra kết quả và là người đưa ra quyết định cuối cùng trước khi thực hiện những thay đổi có ảnh hưởng đến hệ thống.

#### Giải pháp Voice AI dành cho tiếng Việt

Một nội dung đáng chú ý khác là bài toán xây dựng Voice AI cho tiếng Việt – ngôn ngữ còn hạn chế về số lượng và mức độ đa dạng của dữ liệu huấn luyện so với nhiều ngôn ngữ phổ biến khác.

Thay vì xử lý trực tiếp theo mô hình Speech-to-Speech, giải pháp được trình bày chia quy trình thành ba giai đoạn:

1. **Speech-to-Text:** Chuyển giọng nói của người dùng thành văn bản.
2. **LLM Processing:** Sử dụng mô hình ngôn ngữ lớn để phân tích yêu cầu và xây dựng nội dung phản hồi.
3. **Text-to-Speech:** Chuyển phản hồi dạng văn bản thành giọng nói.

Cách tiếp cận này giúp hệ thống dễ kiểm soát nội dung đầu ra, hỗ trợ nhận diện đặc điểm giọng nói theo vùng miền và thuận tiện hơn khi tích hợp Tool Calling để thực hiện các tác vụ bên ngoài.

#### Ứng dụng AI trong lĩnh vực nhân sự

Sự kiện cũng trình bày khả năng sử dụng AI để hỗ trợ quy trình tuyển dụng, đặc biệt trong việc xử lý số lượng lớn hồ sơ ứng viên.

Thông qua việc kết nối Amazon Q với các nền tảng và nguồn dữ liệu trong doanh nghiệp, hệ thống có thể hỗ trợ phân tích CV, xây dựng mô tả công việc, so sánh năng lực của ứng viên và tổng hợp thông tin về mức lương dự kiến.

Giải pháp này góp phần giảm khối lượng công việc thủ công và hỗ trợ bộ phận nhân sự đánh giá ứng viên dựa trên các tiêu chí nhất quán hơn. Tuy nhiên, kết quả do AI cung cấp vẫn cần được con người kiểm tra để hạn chế sai sót và thiên kiến trong quá trình tuyển dụng.

#### Bảo mật kết nối MCP trong hệ thống nội bộ

Khi Amazon Q hoặc AI Agent cần truy cập cơ sở dữ liệu nội bộ, việc bảo vệ dữ liệu và hạn chế kết nối từ Internet công cộng là yêu cầu quan trọng.

Mô hình được trình bày đề xuất triển khai MCP Server trong private subnet của Amazon VPC. Hệ thống có thể kết hợp VPC Endpoint, chính sách kiểm soát truy cập và chứng chỉ do AWS Certificate Manager quản lý để bảo vệ quá trình truyền dữ liệu.

Kiến trúc này giúp giảm mức độ công khai của các dịch vụ nội bộ, giới hạn phạm vi truy cập và tăng cường khả năng bảo vệ dữ liệu khi AI Agent tương tác với hệ thống doanh nghiệp.

### Kiến thức và bài học tiếp thu được

#### Vai trò của AI trong công việc

Qua sự kiện, em nhận thấy AI không chỉ được sử dụng để thay thế các thao tác thủ công mà còn đóng vai trò hỗ trợ con người phân tích dữ liệu, phát hiện vấn đề và đưa ra đề xuất nhanh hơn.

Khả năng sử dụng AI hiệu quả sẽ trở thành một lợi thế quan trọng. Tuy nhiên, con người vẫn cần kiểm tra kết quả, đánh giá rủi ro và chịu trách nhiệm đối với những quyết định cuối cùng.

#### Bảo mật khi xây dựng AI Agent

Khi AI Agent được cấp quyền truy cập vào cơ sở dữ liệu, API hoặc các công cụ nội bộ, bảo mật phải được xem xét ngay từ giai đoạn thiết kế.

Luồng dữ liệu cần được mã hóa, quyền truy cập phải tuân theo nguyên tắc đặc quyền tối thiểu và những dịch vụ quan trọng nên được đặt trong mạng riêng. Hệ thống cũng cần lưu lại lịch sử hoạt động để có thể kiểm tra khi xảy ra sự cố.

#### Lựa chọn kiến trúc AI phù hợp

Đối với những hệ thống có nhiều nhiệm vụ phức tạp, việc phân chia luồng xử lý thành các Agent chuyên biệt có thể giúp mỗi thành phần có trách nhiệm rõ ràng hơn. Cách tiếp cận này hỗ trợ quá trình kiểm thử, phân quyền và xác định lỗi.

Tuy nhiên, kiến trúc Multi-Agent không phải lúc nào cũng cần thiết. Việc lựa chọn giữa Single Agent và Multi-Agent cần dựa trên độ phức tạp của bài toán, chi phí vận hành và yêu cầu thực tế của hệ thống.

### Khả năng ứng dụng vào dự án AI Recipe Finder

Từ những kiến thức tiếp thu được tại sự kiện, em nhận thấy một số giải pháp có thể được nghiên cứu để mở rộng dự án **AI Recipe Finder**:

- **Tăng cường bảo vệ kết nối backend:** Có thể nghiên cứu đặt cơ sở dữ liệu trong private subnet và chỉ cho phép backend truy cập thông qua các quy tắc mạng phù hợp. Nếu hệ thống tích hợp MCP trong tương lai, MCP Server cũng cần được cô lập và giới hạn quyền truy cập.
- **Bảo vệ dữ liệu người dùng:** Các thông tin như sở thích ăn uống, món ăn yêu thích hoặc tiền sử dị ứng cần được mã hóa khi truyền và chỉ được truy cập bởi những thành phần đã được cấp quyền.
- **Hỗ trợ phân tích sự cố:** Có thể thử nghiệm DevOps AI Agent để hỗ trợ phân tích log khi backend hoặc các chức năng của ứng dụng gặp lỗi, chẳng hạn API không phản hồi hoặc hình ảnh món ăn không tải được.
- **Phân chia nhiệm vụ AI:** Những chức năng như tìm kiếm công thức, phân tích nguyên liệu và tư vấn dinh dưỡng có thể được tách thành các thành phần chuyên biệt nếu luồng xử lý trở nên phức tạp hơn.
- **Mở rộng Voice AI:** Trong tương lai, hệ thống có thể bổ sung tính năng tương tác bằng tiếng Việt theo quy trình Speech-to-Text → LLM → Text-to-Speech. Người dùng có thể hỏi công thức hoặc nhận hướng dẫn nấu ăn bằng giọng nói mà không cần thao tác trực tiếp trên màn hình.

### Trải nghiệm tại sự kiện

Tham gia sự kiện **“FCAJ COMMUNITY DAY – DATA DRIVEN, AI RISEN”** là một trải nghiệm bổ ích, giúp em tiếp cận nhiều ứng dụng thực tế của AI trong vận hành hệ thống, giao tiếp bằng giọng nói, tuyển dụng và bảo mật hạ tầng Cloud.

#### Tiếp cận các phần trình diễn thực tế

Các phần demo giúp em hình dung rõ hơn cách những giải pháp AI được áp dụng trong môi trường thực tế. Một số nội dung nổi bật gồm Voice Agent hỗ trợ tư vấn thông tin sản phẩm qua tổng đài, DevOps AI hỗ trợ xác định nguyên nhân sự cố hệ thống và Amazon Q hỗ trợ phân tích, đánh giá hồ sơ ứng viên.

Thông qua những phần trình diễn này, em nhận thấy AI có thể hỗ trợ xử lý nhiều công việc trong thời gian ngắn. Tuy nhiên, hiệu quả của hệ thống vẫn phụ thuộc vào chất lượng dữ liệu, phạm vi quyền truy cập và cơ chế kiểm tra kết quả.

#### Bài học rút ra

- Khả năng sử dụng AI hiệu quả đang trở thành một kỹ năng quan trọng đối với kỹ sư công nghệ thông tin.
- AI nên được sử dụng như công cụ hỗ trợ phân tích và đề xuất; con người vẫn cần kiểm tra và chịu trách nhiệm đối với quyết định cuối cùng.
- Bảo mật cần được xem xét ngay từ giai đoạn thiết kế, đặc biệt khi AI Agent được kết nối với dữ liệu và dịch vụ nội bộ.
- Quyền truy cập của AI cần được giới hạn theo nguyên tắc đặc quyền tối thiểu và mọi hoạt động quan trọng nên được ghi nhận để phục vụ kiểm tra.
- Kiến trúc Multi-Agent phù hợp với những hệ thống có nhiều nhiệm vụ chuyên biệt, nhưng cần cân nhắc giữa lợi ích, độ phức tạp và chi phí vận hành.
- Các giải pháp AI cần có cơ chế kiểm tra dữ liệu đầu ra, xử lý ngoại lệ và phương án dự phòng khi kết quả không đáp ứng yêu cầu.

#### Một số hình ảnh tại sự kiện

![Event 3](/images/4-Event/Event3_1.jpg)
![Event 3](/images/4-Event/Event3_2.jpg)