---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Xác định các công nghệ sử dụng để xây dựng dự án AI Recipe Finder.
* Lựa chọn các dịch vụ AWS phù hợp với từng thành phần của hệ thống.
* Hoàn thiện kiến trúc triển khai tổng thể của dự án.
* Hoàn thiện workflow giữa frontend, backend, cơ sở dữ liệu, xác thực và AI.
* Tìm kiếm các bộ dữ liệu phù hợp với chức năng gợi ý món ăn và phân tích dinh dưỡng.
* Phân tích cấu trúc, chất lượng và khả năng ứng dụng của từng dataset.
* Lựa chọn các dataset chính thức để chuẩn bị cho giai đoạn xử lý dữ liệu.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng hợp yêu cầu chức năng và phi chức năng của dự án AI Recipe Finder.<br>- Xác định các thành phần chính gồm frontend, backend, cơ sở dữ liệu, xác thực người dùng và AI.<br>- Đánh giá các công nghệ dựa trên năng lực của nhóm, thời gian thực hiện và ngân sách AWS.<br>- Lựa chọn React và Tailwind CSS để xây dựng frontend.<br>- Lựa chọn FastAPI và Python để phát triển backend API.<br>- Lựa chọn MySQL làm hệ quản trị cơ sở dữ liệu. | 18/05/2026 | 18/05/2026 |  |
| 3 | - Xác định các dịch vụ AWS chính thức sử dụng trong dự án.<br>- Lựa chọn AWS Amplify để triển khai frontend.<br>- Lựa chọn Amazon EC2 để triển khai backend FastAPI.<br>- Lựa chọn Amazon RDS for MySQL để lưu trữ dữ liệu hệ thống.<br>- Lựa chọn Amazon Cognito để quản lý đăng ký, đăng nhập và xác thực người dùng.<br>- Lựa chọn Amazon Bedrock để hỗ trợ chatbot và các chức năng AI.<br>- Xem xét AWS IAM và Amazon CloudWatch cho hoạt động phân quyền, ghi log và giám sát hệ thống. | 19/05/2026 | 19/05/2026 | <https://docs.aws.amazon.com/amplify/><br><https://docs.aws.amazon.com/ec2/><br><https://docs.aws.amazon.com/rds/><br><https://docs.aws.amazon.com/cognito/><br><https://docs.aws.amazon.com/bedrock/> |
| 4 | - Hoàn thiện kiến trúc tổng thể của hệ thống.<br>- Xác định frontend React được triển khai trên AWS Amplify.<br>- Xác định backend FastAPI được triển khai trên Amazon EC2 và cung cấp REST API cho frontend.<br>- Xác định Amazon RDS for MySQL lưu trữ dữ liệu món ăn, dinh dưỡng, người dùng và lịch sử hoạt động.<br>- Xác định Amazon Cognito chịu trách nhiệm xác thực người dùng và cung cấp token.<br>- Xác định Amazon Bedrock hỗ trợ chatbot và xử lý các yêu cầu AI.<br>- Xem xét phương thức kết nối, phân quyền và bảo vệ dữ liệu giữa các thành phần. | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html><br><https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html><br>https://youtu.be/l8isyDe-GwY?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i><br><https://skillbuilder.aws/learn/U89MJTNSM8/aws-wellarchitected-foundations/RCY5NFM8R9> |
| 5 | - Hoàn thiện workflow tổng thể của dự án AI Recipe Finder.<br>- Xác định luồng đăng ký và đăng nhập giữa frontend, Amazon Cognito và backend.<br>- Xác định luồng tìm kiếm món ăn và gợi ý công thức dựa trên nguyên liệu.<br>- Xác định luồng truy vấn dữ liệu giữa backend và Amazon RDS.<br>- Xác định luồng xử lý chatbot và tìm kiếm thông minh giữa backend và dịch vụ AI.<br>- Xác định cách lưu thông tin người dùng, món ăn yêu thích, lịch sử tìm kiếm và lịch sử trò chuyện.<br>- Thống nhất trách nhiệm của từng thành phần và hướng triển khai cho các tuần tiếp theo. | 21/05/2026 | 21/05/2026 | <https://youtu.be/l8isyDe-GwY?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i><br><https://skillbuilder.aws/learn/U89MJTNSM8/aws-wellarchitected-foundations/RCY5NFM8R9><br><https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |
| 6 | - Tìm kiếm các dataset liên quan đến công thức món ăn, nguyên liệu và dinh dưỡng.<br>- Khảo sát bộ dữ liệu Food.com Recipes and Interactions trên Kaggle.<br>- Khảo sát dữ liệu dinh dưỡng từ USDA FoodData Central.<br>- Phân tích các trường dữ liệu, số lượng bản ghi, định dạng và khả năng sử dụng của từng bộ dữ liệu.<br>- Đánh giá mức độ phù hợp của dữ liệu với chức năng gợi ý món ăn và phân tích calories.<br>- Lựa chọn dữ liệu công thức Food.com và dữ liệu dinh dưỡng USDA FoodData Central làm nguồn dữ liệu chính.<br>- Xác định dataset sẽ được tải xuống và xử lý trong môi trường cục bộ trước khi nhập dữ liệu đã làm sạch vào Amazon RDS.<br>- Xác định yêu cầu làm sạch, kiểm tra dữ liệu trùng lặp và chuẩn hóa dữ liệu. | 22/05/2026 | 22/05/2026 | <https://www.kaggle.com/datasets/realalexanderwei/food-com-recipes-with-ingredients-and-tags/data><br><https://fdc.nal.usda.gov/download-datasets><br><https://fdc.nal.usda.gov/data-documentation.html> |

### Kết quả đạt được tuần 5:

* Xác định được các công nghệ chính sử dụng trong dự án:

  * **Frontend:** React và Tailwind CSS.
  * **Backend:** FastAPI và Python.
  * **Cơ sở dữ liệu:** MySQL.
  * **Giao tiếp hệ thống:** REST API.
  * **Xác thực:** Token do Amazon Cognito cung cấp.
  * **Quản lý mã nguồn:** Git và GitHub.

* Chốt các dịch vụ AWS sử dụng trong kiến trúc:

  * **AWS Amplify:** Triển khai và cung cấp giao diện frontend.
  * **Amazon EC2:** Triển khai backend FastAPI.
  * **Amazon RDS for MySQL:** Lưu trữ dữ liệu quan hệ của hệ thống.
  * **Amazon Cognito:** Quản lý tài khoản và xác thực người dùng.
  * **Amazon Bedrock:** Hỗ trợ chatbot và các chức năng AI.
  * **AWS IAM:** Quản lý vai trò và quyền truy cập.
  * **Amazon CloudWatch:** Theo dõi log và trạng thái hệ thống.

* Hoàn thiện kiến trúc tổng thể của dự án:

  1. Người dùng truy cập giao diện React được triển khai trên AWS Amplify.
  2. Amazon Cognito xử lý đăng ký, đăng nhập và cung cấp token xác thực.
  3. Frontend gửi yêu cầu đến backend FastAPI trên Amazon EC2.
  4. Backend kiểm tra token đối với các API yêu cầu xác thực.
  5. Backend truy vấn dữ liệu trong Amazon RDS for MySQL.
  6. Các yêu cầu chatbot hoặc tìm kiếm thông minh được xử lý với sự hỗ trợ của Amazon Bedrock.
  7. Backend tổng hợp kết quả và trả phản hồi về frontend.

* Hoàn thiện các workflow chính:

  * Đăng ký, đăng nhập và xác thực người dùng.
  * Tìm kiếm và xem chi tiết công thức món ăn.
  * Gợi ý món ăn dựa trên nguyên liệu.
  * Tìm kiếm thông minh bằng AI Semantic Search.
  * Sử dụng chatbot hỗ trợ nấu ăn và tư vấn dinh dưỡng.
  * Phân tích lượng calories của món ăn.
  * Lưu món ăn yêu thích.
  * Lưu lịch sử tìm kiếm và lịch sử trò chuyện.

* Xác định chatbot AI và các chức năng liên quan đến dữ liệu cá nhân chỉ được sử dụng sau khi người dùng đăng nhập.

* Khảo sát và lựa chọn hai nguồn dữ liệu chính:

  * **Food.com Recipes and Interactions:** Cung cấp dữ liệu công thức, nguyên liệu, các bước chế biến và thẻ phân loại.
  * **USDA FoodData Central:** Cung cấp dữ liệu thực phẩm và thông tin dinh dưỡng để hỗ trợ phân tích calories.

* Xác định vai trò của từng dataset:

  * Dataset Food.com được sử dụng cho chức năng tìm kiếm và gợi ý món ăn.
  * Dataset USDA FoodData Central được sử dụng để tra cứu và hỗ trợ tính toán thông tin dinh dưỡng.

* Xác định quy trình chuẩn bị dữ liệu:

  1. Tải dataset từ nguồn cung cấp về môi trường cục bộ.
  2. Kiểm tra cấu trúc và kiểu dữ liệu.
  3. Phân tích dữ liệu thiếu và dữ liệu không hợp lệ.
  4. Phân tích và xử lý bản ghi trùng lặp.
  5. Chuẩn hóa tên món ăn và nguyên liệu.
  6. Chuyển đổi các trường dữ liệu có cấu trúc phức tạp.
  7. Kiểm tra chất lượng dữ liệu sau khi làm sạch.
  8. Nhập dữ liệu hoàn chỉnh vào Amazon RDS for MySQL.

* Hoàn thành mục tiêu lựa chọn công nghệ, chốt kiến trúc, hoàn thiện workflow và lựa chọn dataset, tạo cơ sở để bắt đầu triển khai dự án từ Tuần 6.