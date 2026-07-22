---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Thảo luận với các thành viên trong nhóm để đề xuất và lựa chọn đề tài phù hợp.
* Xác định ý tưởng, mục tiêu và phạm vi của dự án.
* Phân tích các chức năng chính của hệ thống AI Recipe Finder.
* Tìm hiểu các dịch vụ AWS có thể sử dụng để triển khai dự án.
* Xây dựng workflow sơ bộ và xác định cách các thành phần trong hệ thống tương tác với nhau.
* Phân chia định hướng công việc ban đầu cho các thành viên trong nhóm.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Họp với các thành viên trong nhóm để đề xuất ý tưởng dự án.<br>- Thảo luận về tính khả thi, phạm vi thực hiện và khả năng ứng dụng AWS của từng ý tưởng.<br>- So sánh các đề tài dựa trên thời gian, nguồn dữ liệu, công nghệ và năng lực của nhóm.<br>- Thống nhất lựa chọn đề tài phù hợp để tiếp tục nghiên cứu. | 04/05/2026 | 04/05/2026 |  |
| 3 | - Chốt ý tưởng xây dựng dự án AI Recipe Finder.<br>- Xác định bài toán mà dự án cần giải quyết.<br>- Xác định đối tượng người dùng và nhu cầu chính của hệ thống.<br>- Phân tích mục tiêu, phạm vi và kết quả dự kiến của dự án. | 05/05/2026 | 05/05/2026 |  |
| 4 | - Phân tích các chức năng chính của hệ thống.<br>- Xác định chức năng gợi ý món ăn dựa trên nguyên liệu người dùng nhập.<br>- Đề xuất chức năng tìm kiếm thông minh bằng AI Semantic Search.<br>- Xác định chức năng chatbot hỗ trợ nấu ăn và tư vấn dinh dưỡng.<br>- Đề xuất chức năng phân tích lượng calories và quản lý thông tin người dùng.<br>- Xác định yêu cầu đăng nhập trước khi sử dụng chatbot AI. | 06/05/2026 | 06/05/2026 |  |
| 5 | - Tìm hiểu và đề xuất các dịch vụ AWS có thể sử dụng cho dự án.<br>- Đề xuất Amazon RDS để lưu trữ dữ liệu món ăn, dinh dưỡng và người dùng.<br>- Đề xuất Amazon EC2 hoặc AWS App Runner để triển khai backend.<br>- Đề xuất AWS Amplify để triển khai frontend.<br>- Đề xuất Amazon Cognito để quản lý đăng ký, đăng nhập và xác thực người dùng.<br>- Đề xuất Amazon Bedrock để hỗ trợ các chức năng AI.<br>- Đề xuất Amazon S3 để lưu trữ dữ liệu và các tệp cần thiết của dự án.<br>- Xem xét AWS IAM và Amazon CloudWatch phục vụ phân quyền, giám sát và quản lý hệ thống. | 07/05/2026 | 07/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/> |
| 6 | - Tìm hiểu cách tổ chức các thành phần frontend, backend, cơ sở dữ liệu và AI trong hệ thống.<br>- Xây dựng workflow sơ bộ cho dự án AI Recipe Finder.<br>- Xác định luồng người dùng từ đăng nhập, nhập nguyên liệu, tìm kiếm món ăn đến nhận kết quả gợi ý.<br>- Xác định luồng trao đổi dữ liệu giữa frontend, backend, Amazon RDS và dịch vụ AI.<br>- Thảo luận và thống nhất định hướng triển khai cho các tuần tiếp theo.<br>- Phân chia sơ bộ nhiệm vụ cho từng thành viên trong nhóm. | 08/05/2026 | 08/05/2026 | https://www.youtube.com/@AWSStudyGroup<br><https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |

### Kết quả đạt được tuần 3:

* Hoàn thành quá trình thảo luận, đánh giá và lựa chọn ý tưởng dự án cùng các thành viên trong nhóm.

* Thống nhất lựa chọn đề tài **AI Recipe Finder** để tiếp tục phân tích và triển khai.

* Xác định mục tiêu chính của dự án:

  * Gợi ý món ăn dựa trên nguyên liệu do người dùng cung cấp.
  * Hỗ trợ tìm kiếm món ăn thông minh bằng AI Semantic Search.
  * Cung cấp chatbot hỗ trợ nấu ăn và tư vấn dinh dưỡng.
  * Phân tích lượng calories và một số thông tin dinh dưỡng của món ăn.
  * Triển khai hệ thống theo mô hình điện toán đám mây trên AWS.

* Xác định các chức năng chính dự kiến của hệ thống:

  * Đăng ký, đăng nhập và quản lý thông tin người dùng.
  * Tìm kiếm và xem thông tin chi tiết món ăn.
  * Gợi ý món ăn dựa trên danh sách nguyên liệu.
  * Tìm kiếm món ăn bằng AI Semantic Search.
  * Chatbot hỗ trợ công thức nấu ăn và thông tin dinh dưỡng.
  * Phân tích calories của món ăn.
  * Lưu món ăn yêu thích và lịch sử tìm kiếm.
  * Yêu cầu người dùng đăng nhập trước khi sử dụng chatbot AI.

* Đề xuất được danh sách các dịch vụ AWS dự kiến sử dụng:

  * **Amazon RDS:** Lưu trữ dữ liệu món ăn, dinh dưỡng, người dùng và lịch sử hoạt động.
  * **Amazon EC2 hoặc AWS App Runner:** Triển khai backend FastAPI.
  * **AWS Amplify:** Xây dựng và triển khai frontend.
  * **Amazon Cognito:** Quản lý đăng ký, đăng nhập và xác thực người dùng.
  * **Amazon Bedrock:** Hỗ trợ chatbot và các chức năng AI.
  * **Amazon S3:** Lưu trữ tập dữ liệu và các tệp cần thiết.
  * **AWS IAM:** Quản lý vai trò và quyền truy cập giữa các dịch vụ.
  * **Amazon CloudWatch:** Theo dõi hoạt động, log và trạng thái của hệ thống.

* Xây dựng được workflow sơ bộ của hệ thống:

  1. Người dùng truy cập giao diện web.
  2. Người dùng đăng ký hoặc đăng nhập thông qua Amazon Cognito.
  3. Người dùng nhập nguyên liệu hoặc nội dung cần tìm kiếm.
  4. Frontend gửi yêu cầu đến backend thông qua API.
  5. Backend xử lý yêu cầu và truy vấn dữ liệu trong Amazon RDS.
  6. Các yêu cầu tìm kiếm thông minh hoặc chatbot được chuyển đến dịch vụ AI.
  7. Backend tổng hợp dữ liệu và trả kết quả về frontend.
  8. Frontend hiển thị danh sách món ăn, thông tin chi tiết và kết quả tư vấn cho người dùng.

* Xác định được các thành phần chính của hệ thống gồm frontend, backend, cơ sở dữ liệu, xác thực người dùng và dịch vụ AI.

* Có được định hướng ban đầu để phân chia nhiệm vụ và tiếp tục thiết kế kiến trúc, chuẩn bị dữ liệu trong tuần tiếp theo.