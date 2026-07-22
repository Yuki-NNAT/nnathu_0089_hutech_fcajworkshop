---
title: "Worklog Tuần 8"
date: 2026-06-06
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Tạo và cấu hình Amazon Cognito cho dự án AI Recipe Finder.
* Thiết lập User Pool và App Client phục vụ chức năng xác thực người dùng.
* Tích hợp cơ chế xác thực Amazon Cognito vào backend FastAPI.
* Xây dựng chức năng xác minh Access Token do Amazon Cognito phát hành.
* Xây dựng cơ chế lấy thông tin người dùng đã xác thực.
* Đồng bộ người dùng từ Amazon Cognito vào bảng `users` trên Amazon RDS.
* Cấu hình kết nối giữa Amazon Cognito, backend FastAPI và cơ sở dữ liệu.
* Kiểm tra API khi request không có Access Token.
* Kiểm tra chức năng xác thực và đồng bộ người dùng khi có Access Token hợp lệ.
* Rà soát việc xử lý token và thông tin người dùng nhằm hạn chế rủi ro bảo mật.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tạo Amazon Cognito User Pool cho dự án AI Recipe Finder.<br>- Cấu hình phương thức đăng nhập bằng email.<br>- Thiết lập các thuộc tính cần thiết của tài khoản người dùng.<br>- Cấu hình chính sách mật khẩu và cơ chế xác minh tài khoản.<br>- Tạo App Client để phục vụ quá trình xác thực.<br>- Kiểm tra các luồng đăng ký, xác nhận tài khoản và đăng nhập được hỗ trợ.<br>- Ghi nhận các thông tin cần thiết gồm AWS Region, User Pool ID và App Client ID. | 08/06/2026 | 08/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools.html><br><https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-client-apps.html> |
| 3 | - Nghiên cứu cấu trúc JSON Web Token do Amazon Cognito phát hành.<br>- Phân biệt ID Token, Access Token và Refresh Token.<br>- Xây dựng dependency xác thực dùng chung cho backend FastAPI.<br>- Nhận Access Token từ HTTP Authorization Header theo Bearer Token.<br>- Lấy public key từ JSON Web Key Set của Cognito User Pool.<br>- Xác minh chữ ký, thuật toán, thời hạn và các claim quan trọng của JWT.<br>- Kiểm tra token thuộc đúng User Pool và App Client đã cấu hình.<br>- Chuẩn hóa phản hồi `401 Unauthorized` khi token bị thiếu, hết hạn hoặc không hợp lệ. | 09/06/2026 | 09/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-user-pools-using-the-access-token.html><br><https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-user-pools-using-tokens-verifying-a-jwt.html> |
| 4 | - Xây dựng chức năng đồng bộ người dùng đã xác thực vào Amazon RDS.<br>- Sử dụng claim `sub` của Cognito làm định danh duy nhất của người dùng.<br>- Trích xuất email và tên người dùng từ thông tin xác thực.<br>- Hoàn thiện ORM Model, Pydantic Schema, CRUD và Auth Service cho người dùng.<br>- Tìm người dùng trong bảng `users` thông qua trường `cognito_sub`.<br>- Xây dựng cơ chế tự động tạo bản ghi khi người dùng đăng nhập lần đầu.<br>- Sử dụng lại bản ghi hiện có trong những lần truy cập sau để tránh trùng lặp.<br>- Xử lý trường hợp email đã tồn tại hoặc dữ liệu người dùng không hợp lệ. | 10/06/2026 | 10/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html> |
| 5 | - Cấu hình các biến môi trường của Amazon Cognito trên backend cục bộ và Amazon EC2.<br>- Không ghi trực tiếp User Pool ID, App Client ID và thông tin cấu hình vào mã nguồn.<br>- Tích hợp dependency xác thực vào Auth API Router.<br>- Xây dựng API `GET /auth/me` để trả về thông tin người dùng hiện tại.<br>- Cập nhật phiên bản backend có chức năng xác thực lên Amazon EC2.<br>- Khởi động lại `systemd service` và kiểm tra log vận hành.<br>- Gửi request đến `GET /auth/me` khi không có Access Token.<br>- Xác nhận API trả về `401 Unauthorized` đúng dự kiến.<br>- Kiểm tra phản hồi lỗi không làm lộ thông tin cấu hình hoặc chi tiết xử lý nội bộ. | 11/06/2026 | 11/06/2026 |  |
| 6 | - Chuẩn bị tài khoản người dùng trên Amazon Cognito và lấy Access Token hợp lệ.<br>- Gửi Access Token đến API `GET /auth/me` theo định dạng Bearer Token.<br>- Kiểm tra backend xác minh thành công chữ ký và các claim của JWT.<br>- Kiểm tra backend lấy được thông tin định danh của người dùng từ token.<br>- Kiểm tra người dùng đăng nhập lần đầu được thêm vào bảng `users` trên Amazon RDS.<br>- Kiểm tra API trả về đúng thông tin người dùng hiện tại.<br>- Gửi lại request bằng cùng một tài khoản và xác nhận không tạo bản ghi trùng lặp.<br>- Đối chiếu `cognito_sub` và email giữa Amazon Cognito với bảng `users`.<br>- Kiểm tra token sai định dạng, token không hợp lệ và token hết hạn.<br>- Tổng hợp kết quả và xác nhận luồng xác thực, đồng bộ người dùng hoạt động ở phía backend. | 12/06/2026 | 12/06/2026 |  |

### Kết quả đạt được tuần 8:

* Tạo và cấu hình thành công Amazon Cognito User Pool cho dự án AI Recipe Finder.

* Hoàn thành các cấu hình xác thực cơ bản:

  * Phương thức đăng nhập bằng email.
  * Thuộc tính tài khoản người dùng.
  * Chính sách mật khẩu.
  * Cơ chế xác minh tài khoản.
  * App Client phục vụ quá trình xác thực.
  * AWS Region, User Pool ID và App Client ID phục vụ cấu hình backend.

* Hoàn thành tích hợp cơ chế xác thực Amazon Cognito vào backend FastAPI.

* Xây dựng chức năng nhận Access Token từ HTTP Authorization Header theo định dạng:

  ```text
  Authorization: Bearer <access_token>