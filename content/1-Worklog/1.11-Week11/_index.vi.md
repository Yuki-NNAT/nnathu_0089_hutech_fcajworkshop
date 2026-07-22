---
title: "Worklog Tuần 11"
date: 2026-06-27
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Kiểm thử toàn bộ hệ thống AI Recipe Finder theo các luồng sử dụng chính.
* Kiểm tra khả năng phối hợp giữa frontend, Amazon Cognito, FastAPI backend, thành phần AI và Amazon RDS.
* Phát hiện, phân loại và khắc phục các lỗi còn tồn tại sau quá trình tích hợp.
* Rà soát và tối ưu hiệu năng của backend và cơ sở dữ liệu.
* Hoàn thiện phiên bản triển khai trên AWS.
* Cập nhật tài liệu kỹ thuật phục vụ vận hành và bàn giao hệ thống.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Xây dựng checklist kiểm thử toàn bộ hệ thống dựa trên các chức năng đã hoàn thiện.<br>- Xác định các luồng kiểm thử chính gồm đăng nhập, xác thực người dùng, xem danh sách công thức, xem chi tiết công thức và truy xuất dữ liệu dinh dưỡng.<br>- Xác định các luồng có sự tham gia của frontend, backend, Amazon Cognito, thành phần AI và Amazon RDS.<br>- Chuẩn bị dữ liệu kiểm thử hợp lệ, không hợp lệ và các trường hợp biên.<br>- Xác định kết quả mong đợi và mã trạng thái HTTP tương ứng với từng trường hợp.<br>- Phân công và thống nhất cách ghi nhận lỗi với các thành viên trong nhóm. | 29/06/2026 | 29/06/2026 |  |
| 3 | - Thực hiện kiểm thử toàn bộ các luồng chính từ giao diện đến backend và cơ sở dữ liệu.<br>- Kiểm tra quá trình đăng nhập thông qua Amazon Cognito và chuyển Access Token đến backend.<br>- Kiểm tra các API công khai và API yêu cầu xác thực.<br>- Kiểm tra việc đồng bộ thông tin người dùng với bảng users trên Amazon RDS.<br>- Kiểm tra khả năng truy xuất danh sách, chi tiết công thức và dữ liệu dinh dưỡng.<br>- Phối hợp kiểm tra luồng trao đổi dữ liệu giữa backend và thành phần AI.<br>- Theo dõi log để ghi nhận lỗi, thời điểm phát sinh và thành phần liên quan.<br>- Tổng hợp kết quả kiểm thử theo từng chức năng của hệ thống. | 30/06/2026 | 30/06/2026 |  |
| 4 | - Phân loại các lỗi đã ghi nhận theo frontend, backend, Amazon Cognito, thành phần AI, cơ sở dữ liệu hoặc cấu hình triển khai.<br>- Khắc phục các lỗi thuộc phạm vi backend và cơ sở dữ liệu.<br>- Điều chỉnh endpoint, Pydantic Schema, xử lý ngoại lệ hoặc thông báo lỗi nếu cần thiết.<br>- Kiểm tra các trường hợp token thiếu, token không hợp lệ, dữ liệu đầu vào sai hoặc không tìm thấy tài nguyên.<br>- Kiểm tra việc rollback transaction khi thao tác cơ sở dữ liệu xảy ra lỗi.<br>- Thực hiện kiểm thử hồi quy đối với các chức năng đã được điều chỉnh.<br>- Ghi nhận những lỗi cần phối hợp với thành viên frontend hoặc AI để tiếp tục xử lý. | 01/07/2026 | 01/07/2026 |  |
| 5 | - Kiểm tra thời gian phản hồi của các API được sử dụng thường xuyên.<br>- Rà soát truy vấn lấy danh sách, chi tiết công thức, dữ liệu dinh dưỡng và thông tin người dùng.<br>- Kiểm tra việc sử dụng phân trang để giới hạn lượng dữ liệu trả về.<br>- Rà soát các index liên quan đến những trường thường xuyên tìm kiếm hoặc liên kết.<br>- Kiểm tra cấu hình SQLAlchemy connection pool và khả năng tái sử dụng kết nối đến Amazon RDS.<br>- Theo dõi CPU, bộ nhớ, trạng thái dịch vụ và log vận hành trên Amazon EC2.<br>- Điều chỉnh những điểm gây phản hồi chậm hoặc sử dụng tài nguyên chưa hợp lý.<br>- Kiểm tra lại kết quả và thời gian phản hồi sau khi tối ưu. | 02/07/2026 | 02/07/2026 |  |
| 6 | - Cập nhật mã nguồn đã khắc phục lỗi và tối ưu lên GitHub.<br>- Triển khai phiên bản backend hoàn thiện lên Amazon EC2.<br>- Khởi động lại dịch vụ backend và kiểm tra trạng thái hoạt động.<br>- Kiểm tra lại các API và luồng tích hợp quan trọng sau khi triển khai.<br>- Rà soát cấu hình biến môi trường, CORS và kết nối Amazon RDS.<br>- Kiểm tra log nhằm bảo đảm không xuất hiện lỗi nghiêm trọng sau khi cập nhật.<br>- Hoàn thiện tài liệu API, hướng dẫn cấu hình, triển khai và vận hành backend.<br>- Cập nhật kiến trúc, cấu trúc mã nguồn và các lưu ý kỹ thuật phục vụ bàn giao.<br>- Tổng hợp kết quả kiểm thử, lỗi đã xử lý và những hạn chế còn tồn tại. | 03/07/2026 | 03/07/2026 |  |

### Kết quả dự kiến tuần 11:

* Hoàn thành checklist kiểm thử toàn bộ hệ thống AI Recipe Finder.
* Kiểm tra các luồng chính gồm:

  * Đăng nhập và xác thực bằng Amazon Cognito.
  * Gửi Access Token từ frontend đến backend.
  * Đồng bộ và truy xuất thông tin người dùng.
  * Xem danh sách và chi tiết công thức.
  * Truy xuất dữ liệu dinh dưỡng.
  * Trao đổi dữ liệu giữa backend và thành phần AI.
  * Kết nối và truy xuất dữ liệu trên Amazon RDS.

* Ghi nhận và phân loại các lỗi theo từng thành phần của hệ thống.
* Khắc phục các lỗi thuộc phạm vi backend và cơ sở dữ liệu.
* Kiểm tra lại các chức năng đã sửa nhằm hạn chế phát sinh lỗi hồi quy.
* Xác nhận backend xử lý phù hợp đối với token không hợp lệ, dữ liệu sai và tài nguyên không tồn tại.
* Rà soát thời gian phản hồi của các API chính.
* Tối ưu truy vấn, phân trang, index và cấu hình kết nối cơ sở dữ liệu nếu cần thiết.
* Kiểm tra trạng thái tài nguyên và dịch vụ backend trên Amazon EC2.
* Cập nhật phiên bản mã nguồn hoàn thiện lên GitHub.
* Triển khai và xác nhận phiên bản backend cuối cùng hoạt động ổn định trên Amazon EC2.
* Hoàn thiện tài liệu API, cấu hình, triển khai và vận hành backend.
* Tổng hợp kết quả kiểm thử, các lỗi đã xử lý và những hạn chế còn tồn tại.
* Chuẩn bị nội dung phục vụ viết báo cáo và bàn giao dự án trong Tuần 12.