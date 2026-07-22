---
title: "Worklog Tuần 7"
date: 2026-05-30
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Xây dựng cấu trúc backend cho dự án bằng FastAPI.
* Kết nối backend với Amazon RDS for MySQL.
* Xây dựng ORM Model, Pydantic Schema, CRUD, Service và API Router.
* Phát triển các API phục vụ truy xuất dữ liệu công thức và dinh dưỡng.
* Kiểm tra hoạt động của API trên môi trường cục bộ.
* Tạo và cấu hình máy chủ Amazon EC2.
* Triển khai backend FastAPI lên Amazon EC2.
* Kết nối backend trên EC2 với cơ sở dữ liệu Amazon RDS.
* Rà soát mã nguồn theo các rủi ro liên quan trong OWASP Top 10.
* Bổ sung kiểm tra dữ liệu đầu vào và xử lý lỗi API.
* Kiểm tra lại hoạt động của backend sau khi triển khai.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Khởi tạo cấu trúc backend FastAPI cho dự án AI Recipe Finder.<br>- Tổ chức mã nguồn thành các thành phần gồm cấu hình, kết nối cơ sở dữ liệu, model, schema, CRUD, service và API router.<br>- Cài đặt các thư viện cần thiết như FastAPI, Uvicorn, SQLAlchemy, PyMySQL và Pydantic.<br>- Tạo tệp cấu hình môi trường để lưu thông tin kết nối cơ sở dữ liệu.<br>- Xây dựng SQLAlchemy Engine và cơ chế quản lý database session.<br>- Cấu hình connection pool, kiểm tra kết nối và đóng session sau mỗi request.<br>- Kiểm tra kết nối từ backend cục bộ đến database `food_ai_db` trên Amazon RDS. | 01/06/2026 | 01/06/2026 |  |
| 3 | - Xây dựng các ORM Model tương ứng với những bảng đã thiết kế trong Amazon RDS.<br>- Xây dựng model cho dữ liệu người dùng, công thức món ăn, dinh dưỡng, món ăn yêu thích và lịch sử hoạt động.<br>- Khai báo khóa chính, khóa ngoại, quan hệ và kiểu dữ liệu phù hợp.<br>- Xây dựng Pydantic Schema để kiểm tra và định dạng dữ liệu request, response.<br>- Tách schema danh sách công thức, chi tiết công thức và thông tin dinh dưỡng.<br>- Xây dựng lớp CRUD để thực hiện truy vấn dữ liệu bằng SQLAlchemy.<br>- Xây dựng Service Layer để xử lý nghiệp vụ và tách biệt logic khỏi API Router. | 02/06/2026 | 02/06/2026 |  |
| 4 | - Xây dựng API Router cho dữ liệu công thức món ăn và dinh dưỡng.<br>- Xây dựng API lấy danh sách công thức có phân trang.<br>- Xây dựng API lấy ngẫu nhiên công thức món ăn.<br>- Xây dựng API lấy chi tiết công thức theo mã công thức.<br>- Xây dựng API tra cứu thông tin dinh dưỡng theo `fdc_id`.<br>- Cấu hình Response Model cho từng API.<br>- Kiểm tra API bằng Swagger UI của FastAPI.<br>- Kiểm tra các trường hợp trả về thành công, không tìm thấy dữ liệu và tham số truy vấn không hợp lệ.<br>- Kiểm tra backend có thể truy xuất dữ liệu thực tế từ Amazon RDS. | 03/06/2026 | 03/06/2026 |  |
| 5 | - Tạo Amazon EC2 instance sử dụng hệ điều hành Ubuntu.<br>- Cấu hình key pair, VPC, Security Group và các quy tắc kết nối cần thiết.<br>- Kết nối đến EC2 thông qua SSH.<br>- Cài đặt Python, môi trường ảo, Git, Nginx và các thư viện cần thiết.<br>- Đưa mã nguồn backend từ GitHub lên EC2.<br>- Cấu hình biến môi trường và thông tin kết nối Amazon RDS.<br>- Chạy backend bằng Uvicorn và kiểm tra kết nối từ EC2 đến RDS.<br>- Tạo `systemd service` để backend tự động chạy và khởi động lại khi xảy ra lỗi.<br>- Cấu hình Nginx làm reverse proxy chuyển tiếp request đến FastAPI.<br>- Kiểm tra các API sau khi triển khai trên máy chủ EC2. | 04/06/2026 | 04/06/2026 | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html><br><https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-linux-inst-ssh.html> |
| 6 | - Rà soát mã nguồn backend dựa trên các nhóm rủi ro liên quan trong OWASP Top 10.<br>- Kiểm tra nguy cơ SQL Injection và xác nhận các truy vấn sử dụng SQLAlchemy thay vì ghép chuỗi SQL trực tiếp.<br>- Kiểm tra việc quản lý thông tin nhạy cảm và bảo đảm thông tin kết nối không được ghi trực tiếp trong mã nguồn.<br>- Kiểm tra tệp `.env` không được đưa lên GitHub.<br>- Giới hạn giá trị `page`, `limit` và các tham số đầu vào của API.<br>- Sử dụng Pydantic Schema để kiểm tra kiểu dữ liệu và ràng buộc dữ liệu đầu vào.<br>- Bổ sung xử lý trường hợp tài nguyên không tồn tại, dữ liệu không hợp lệ và lỗi truy vấn cơ sở dữ liệu.<br>- Chuẩn hóa mã trạng thái HTTP và nội dung phản hồi lỗi.<br>- Hạn chế trả thông tin lỗi nội bộ, stack trace hoặc thông tin cơ sở dữ liệu cho người dùng.<br>- Kiểm tra lại API sau khi bổ sung các biện pháp bảo mật và xử lý lỗi. | 05/06/2026 | 05/06/2026 | <https://owasp.org/www-project-top-ten/><br><https://owasp.org/www-project-api-security/> |

### Kết quả đạt được tuần 7:

* Hoàn thành cấu trúc backend FastAPI theo hướng phân chia trách nhiệm thành các thành phần:

  * API Router.
  * Dependencies.
  * ORM Model.
  * Pydantic Schema.
  * CRUD.
  * Service.
  * Database Session.
  * Cấu hình môi trường.

* Hoàn thành kết nối backend với database `food_ai_db` trên Amazon RDS for MySQL bằng SQLAlchemy và PyMySQL.

* Cấu hình quản lý kết nối cơ sở dữ liệu:

  * Kiểm tra trạng thái kết nối trước khi sử dụng.
  * Tái sử dụng kết nối thông qua connection pool.
  * Tự động rollback khi xảy ra lỗi.
  * Đóng database session sau khi xử lý request.
  * Sử dụng bộ ký tự `utf8mb4`.

* Xây dựng các ORM Model và Pydantic Schema phục vụ truy xuất, kiểm tra và định dạng dữ liệu.

* Hoàn thành các API cơ bản cho dữ liệu công thức:

  * `GET /recipes`: Lấy danh sách công thức có phân trang.
  * `GET /recipes/random`: Lấy ngẫu nhiên công thức món ăn.
  * `GET /recipes/{recipe_id}`: Lấy chi tiết một công thức theo mã.

* Hoàn thành API cho dữ liệu dinh dưỡng:

  * `GET /nutrition/{fdc_id}`: Tra cứu thông tin thực phẩm và calories theo mã USDA FoodData Central.

* Hoàn thành kiểm tra API bằng Swagger UI:

  * Kiểm tra dữ liệu trả về từ Amazon RDS.
  * Kiểm tra phân trang.
  * Kiểm tra tài nguyên tồn tại và không tồn tại.
  * Kiểm tra tham số không hợp lệ.
  * Kiểm tra cấu trúc response theo Pydantic Schema.
  * Kiểm tra mã trạng thái HTTP.

* Tạo và cấu hình thành công Amazon EC2 instance sử dụng Ubuntu để triển khai backend.

* Hoàn thành cài đặt môi trường vận hành trên EC2:

  * Python và môi trường ảo.
  * Các thư viện trong `requirements.txt`.
  * Git.
  * Uvicorn.
  * Nginx.
  * Systemd.

* Đưa mã nguồn backend từ GitHub lên Amazon EC2 và cấu hình các biến môi trường cần thiết.

* Kết nối thành công backend FastAPI trên Amazon EC2 với Amazon RDS for MySQL.

* Cấu hình `systemd service` để:

  * Backend chạy dưới dạng dịch vụ nền.
  * Tự động khởi động cùng máy chủ.
  * Tự động khởi động lại khi tiến trình gặp lỗi.
  * Hỗ trợ kiểm tra trạng thái và log của backend.

* Cấu hình Nginx làm reverse proxy cho ứng dụng FastAPI.

* Kiểm tra các API hoạt động và truy xuất được dữ liệu thực tế sau khi triển khai trên Amazon EC2.

* Hoàn thành rà soát các nội dung bảo mật liên quan đến OWASP Top 10 và OWASP API Security:

  * Hạn chế nguy cơ SQL Injection bằng truy vấn ORM có tham số.
  * Không lưu thông tin kết nối và thông tin nhạy cảm trực tiếp trong mã nguồn.
  * Loại trừ tệp `.env` khỏi Git.
  * Kiểm tra và giới hạn dữ liệu đầu vào.
  * Hạn chế thông tin chi tiết trong phản hồi lỗi.
  * Sử dụng đúng phương thức và mã trạng thái HTTP.
  * Kiểm tra cấu hình triển khai và quyền truy cập mạng.
  * Rà soát các thư viện phụ thuộc của backend.

* Bổ sung kiểm tra dữ liệu đầu vào bằng Pydantic:

  * Kiểm tra đúng kiểu dữ liệu.
  * Giới hạn giá trị tham số phân trang.
  * Từ chối các giá trị không hợp lệ.
  * Giảm nguy cơ request gây truy vấn dữ liệu quá lớn.

* Chuẩn hóa xử lý lỗi API:

  * Trả về `404 Not Found` khi tài nguyên không tồn tại.
  * Trả về `422 Unprocessable Entity` khi dữ liệu đầu vào không hợp lệ.
  * Xử lý và ghi log lỗi nội bộ mà không trả stack trace cho người dùng.
  * Rollback database session khi truy vấn hoặc xử lý dữ liệu gặp lỗi.

* Hoàn thành backend cơ bản và môi trường triển khai trên Amazon EC2, sẵn sàng cho giai đoạn tích hợp xác thực Amazon Cognito và phát triển các API theo người dùng trong tuần tiếp theo.