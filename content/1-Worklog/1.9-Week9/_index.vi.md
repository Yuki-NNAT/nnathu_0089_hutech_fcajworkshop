---
title: "Worklog Tuần 9"
date: 2026-06-13
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Bổ sung các API cần thiết cho backend của dự án AI Recipe Finder.
* Phát triển các chức năng liên quan đến dữ liệu và tài khoản người dùng.
* Hoàn thiện các thành phần ORM Model, Pydantic Schema, CRUD, Service và API Router cho từng chức năng.
* Bổ sung hoặc điều chỉnh cấu trúc cơ sở dữ liệu khi cần thiết.
* Áp dụng xác thực Amazon Cognito cho các API cá nhân hóa.
* Kiểm tra dữ liệu đầu vào, quyền truy cập và phản hồi lỗi của API.
* Triển khai phiên bản backend mới lên Amazon EC2.
* Hỗ trợ frontend và thành phần AI kết nối với backend.
* Xác định nguyên nhân và xử lý các lỗi phát sinh trong quá trình tích hợp.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng hợp yêu cầu API từ các thành phần frontend và AI.<br>- Kiểm tra lại cấu trúc backend và các API đã hoàn thành.<br>- Xác định các chức năng backend cần bổ sung cho người dùng đã đăng nhập.<br>- Kiểm tra cấu trúc các bảng `users`, `favorites`, `search_history` và `chat_history` trên Amazon RDS.<br>- Rà soát khóa chính, khóa ngoại, ràng buộc duy nhất và các chỉ mục liên quan.<br>- Xác định request, response, mã trạng thái HTTP và yêu cầu xác thực của từng API.<br>- Lập kế hoạch triển khai theo cấu trúc Router, Schema, CRUD và Service. | 15/06/2026 | 15/06/2026 |  |
| 3 | - Bổ sung API phục vụ quản lý thông tin tài khoản người dùng.<br>- Xây dựng request schema để kiểm tra dữ liệu đầu vào.<br>- Bổ sung chức năng cập nhật tên người dùng hiện tại.<br>- Xây dựng API `PATCH /auth/me/username`.<br>- Sử dụng người dùng lấy từ dependency xác thực thay vì nhận `user_id` trực tiếp từ client.<br>- Kiểm tra username rỗng, không đúng định dạng hoặc vượt quá độ dài cho phép.<br>- Kiểm tra trường hợp username đã được sử dụng nếu hệ thống áp dụng ràng buộc duy nhất.<br>- Chuẩn hóa response theo schema thông tin người dùng.<br>- Kiểm tra API khi không có token, token không hợp lệ và token hợp lệ. | 16/06/2026 | 16/06/2026 |  |
| 4 | - Tiếp tục bổ sung các API cá nhân hóa theo tài khoản người dùng.<br>- Hoàn thiện các thành phần ORM Model, Pydantic Schema, CRUD, Service và Router cần thiết.<br>- Áp dụng dependency xác thực Amazon Cognito cho các API yêu cầu đăng nhập.<br>- Liên kết dữ liệu với người dùng thông qua `user_id` được xác định từ `cognito_sub`.<br>- Kiểm tra quyền truy cập để người dùng chỉ có thể thao tác với dữ liệu thuộc tài khoản của mình.<br>- Xử lý trường hợp tài nguyên không tồn tại hoặc dữ liệu bị trùng lặp.<br>- Sử dụng transaction, commit và rollback phù hợp khi thay đổi dữ liệu.<br>- Kiểm tra dữ liệu được lưu chính xác trên Amazon RDS. | 17/06/2026 | 17/06/2026 |  |
| 5 | - Hoàn thiện và kiểm tra các API được bổ sung trong tuần.<br>- Kiểm tra request hợp lệ và không hợp lệ bằng Swagger UI.<br>- Kiểm tra các trường hợp `401 Unauthorized`, `404 Not Found`, `409 Conflict` và `422 Unprocessable Entity`.<br>- Rà soát response schema và nội dung phản hồi lỗi.<br>- Kiểm tra API không trả về token, stack trace hoặc thông tin cơ sở dữ liệu.<br>- Kiểm tra lại việc giới hạn dữ liệu đầu vào và phân trang nếu có.<br>- Cập nhật mã nguồn lên GitHub.<br>- Pull phiên bản mới trên Amazon EC2.<br>- Khởi động lại `systemd service` và kiểm tra log vận hành.<br>- Kiểm tra các API hoạt động sau khi triển khai. | 18/06/2026 | 18/06/2026 |  |
| 6 | - Cung cấp thông tin endpoint, phương thức HTTP, request và response cho các thành viên phụ trách frontend và AI.<br>- Hỗ trợ frontend gửi Access Token đến backend bằng Authorization Header.<br>- Hỗ trợ kết nối frontend với các API đã triển khai trên Amazon EC2.<br>- Hỗ trợ thành phần AI truy xuất hoặc gửi dữ liệu thông qua backend.<br>- Kiểm tra cấu hình URL, CORS, token và dữ liệu request trong quá trình tích hợp.<br>- Theo dõi log backend để xác định nguyên nhân lỗi.<br>- Xử lý các lỗi liên quan đến xác thực, dữ liệu đầu vào, kết nối cơ sở dữ liệu và cấu trúc response.<br>- Kiểm tra lại toàn bộ luồng sau khi sửa lỗi.<br>- Ghi nhận các nội dung chưa hoàn thành để tiếp tục xử lý trong tuần sau. | 19/06/2026 | 19/06/2026 |  |

### Kết quả dự kiến tuần 9:

* Xác định được danh sách API cần bổ sung dựa trên yêu cầu của frontend và thành phần AI.

* Hoàn thiện API quản lý thông tin người dùng:

  * `GET /auth/me`: Lấy thông tin người dùng hiện tại.
  * `PATCH /auth/me/username`: Cập nhật username của người dùng hiện tại.

* Các API cá nhân hóa sử dụng dependency xác thực Amazon Cognito để xác định người dùng đang đăng nhập.

* Người dùng không cần và không được tự truyền `user_id` để truy cập dữ liệu cá nhân.

* Hoàn thiện các thành phần backend cần thiết cho những chức năng được triển khai:

  * ORM Model.
  * Pydantic Schema.
  * CRUD.
  * Service.
  * API Router.
  * Authentication Dependency.

* Bổ sung kiểm tra dữ liệu đầu vào:

  * Kiểm tra kiểu dữ liệu.
  * Kiểm tra độ dài và định dạng.
  * Loại bỏ khoảng trắng không cần thiết.
  * Từ chối giá trị rỗng hoặc không hợp lệ.
  * Hạn chế request gây truy vấn dữ liệu quá lớn.

* Chuẩn hóa mã trạng thái HTTP:

  * `200 OK` khi truy vấn hoặc cập nhật thành công.
  * `401 Unauthorized` khi thiếu hoặc sử dụng token không hợp lệ.
  * `404 Not Found` khi tài nguyên không tồn tại.
  * `409 Conflict` khi dữ liệu vi phạm ràng buộc duy nhất.
  * `422 Unprocessable Entity` khi dữ liệu đầu vào không hợp lệ.

* Kiểm tra quyền truy cập và bảo đảm người dùng chỉ thao tác được với dữ liệu thuộc tài khoản của mình.

* Kiểm tra dữ liệu được lưu và truy xuất chính xác trên Amazon RDS.

* Cập nhật phiên bản backend mới lên GitHub và Amazon EC2.
* Khởi động lại dịch vụ backend và xác nhận API tiếp tục hoạt động ổn định sau khi triển khai.

* Hỗ trợ frontend và thành phần AI kết nối với backend.

* Kiểm tra và xử lý các nhóm lỗi phát sinh trong quá trình tích hợp:

  * Sai địa chỉ API.
  * Lỗi CORS.
  * Thiếu hoặc sai Authorization Header.
  * Access Token không hợp lệ.
  * Dữ liệu request không đúng schema.
  * Response không đúng cấu trúc mà thành phần tích hợp yêu cầu.
  * Lỗi kết nối Amazon RDS.
  * Lỗi cấu hình môi trường trên Amazon EC2.

* Hoàn thành nền tảng backend để tiếp tục phát triển các API món ăn yêu thích, lịch sử tìm kiếm và lịch sử trò chuyện.