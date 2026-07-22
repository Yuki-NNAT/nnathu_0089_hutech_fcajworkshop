---
title: "Worklog Tuần 10"
date: 2026-06-20
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Hoàn thiện các chức năng backend cần thiết cho quá trình tích hợp hệ thống.
* Kiểm tra lại kết nối đã được thiết lập từ tuần trước giữa frontend, Amazon Cognito và backend.
* Kiểm tra khả năng trao đổi dữ liệu giữa backend và thành phần AI.
* Tiếp nhận và phân tích các lỗi phát sinh trong quá trình tích hợp.
* Điều chỉnh API, cấu trúc dữ liệu và cấu hình backend theo kết quả kiểm tra.
* Xác nhận các thành phần có thể kết nối và hoạt động đúng theo luồng đã thiết kế.
* Chuẩn bị hệ thống cho giai đoạn kiểm thử tổng thể trong tuần tiếp theo.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Rà soát tiến độ các chức năng backend đã triển khai.<br>- Đối chiếu danh sách API hiện có với nhu cầu sử dụng của frontend và thành phần AI.<br>- Xác định các endpoint, trường dữ liệu hoặc chức năng cần điều chỉnh để phục vụ quá trình tích hợp.<br>- Kiểm tra sự thống nhất giữa tên trường, kiểu dữ liệu và cấu trúc response.<br>- Tổng hợp các nội dung cần trao đổi với từng thành viên trong nhóm.<br>- Xây dựng checklist kiểm tra giữa frontend, backend, cơ sở dữ liệu và thành phần AI. | 22/06/2026 | 22/06/2026 |  |
| 3 | - Hoàn thiện các chức năng backend còn cần thiết cho quá trình tích hợp.<br>- Điều chỉnh Pydantic Schema theo cấu trúc dữ liệu mà các thành phần sử dụng.<br>- Chuẩn hóa định dạng request và response của các API liên quan.<br>- Kiểm tra khả năng xử lý các trường dữ liệu tùy chọn hoặc bị thiếu.<br>- Bổ sung thông báo lỗi phù hợp để thành phần gọi API có thể nhận biết nguyên nhân.<br>- Kiểm tra sự tương thích của API sau khi điều chỉnh. | 23/06/2026 | 23/06/2026 |  |
| 4 | - Kiểm tra lại kết nối đã được thiết lập từ tuần trước giữa frontend, Amazon Cognito và backend.<br>- Kiểm tra frontend gọi API thông qua địa chỉ backend được triển khai trên Amazon EC2.<br>- Đối chiếu URL, phương thức HTTP, Authorization Header, query parameter và request body.<br>- Kiểm tra Access Token được gửi đúng định dạng Bearer Token khi gọi các API yêu cầu xác thực.<br>- Kiểm tra cấu trúc response và mã trạng thái HTTP mà frontend nhận được.<br>- Kiểm tra cấu hình CORS đối với localhost và địa chỉ frontend trên AWS Amplify.<br>- Theo dõi log backend để ghi nhận các lỗi phát sinh trong quá trình trao đổi dữ liệu. | 24/06/2026 | 24/06/2026 |  |
| 5 | - Phối hợp với thành viên frontend để kiểm tra các luồng gọi API từ giao diện.<br>- Kiểm tra dữ liệu request và response trong quá trình frontend sử dụng backend.<br>- Phối hợp với thành viên AI để kiểm tra khả năng truy xuất dữ liệu công thức và dinh dưỡng thông qua backend.<br>- Đối chiếu endpoint và cấu trúc dữ liệu đầu vào, đầu ra mà thành phần AI sử dụng.<br>- Kiểm tra các trường hợp thiếu dữ liệu, dữ liệu không hợp lệ hoặc không tìm thấy tài nguyên.<br>- Theo dõi log request để xác định vị trí phát sinh lỗi.<br>- Phân loại lỗi thuộc frontend, backend, thành phần AI, cơ sở dữ liệu hoặc cấu hình triển khai.<br>- Ghi nhận kết quả kiểm tra và các nội dung cần điều chỉnh. | 25/06/2026 | 25/06/2026 |  |
| 6 | - Điều chỉnh backend dựa trên các lỗi và phản hồi nhận được trong quá trình tích hợp.<br>- Sửa các trường hợp không thống nhất giữa request và response.<br>- Điều chỉnh Pydantic Schema, endpoint, cấu hình CORS hoặc biến môi trường nếu cần thiết.<br>- Kiểm tra lại các luồng kết nối đã xảy ra lỗi sau khi sửa.<br>- Kiểm tra dữ liệu được lưu và truy xuất chính xác trên Amazon RDS.<br>- Cập nhật mã nguồn backend lên GitHub và triển khai phiên bản mới trên Amazon EC2.<br>- Khởi động lại dịch vụ và kiểm tra trạng thái hoạt động sau khi triển khai.<br>- Tổng hợp các vấn đề đã xử lý và những nội dung còn phụ thuộc vào tiến độ của thành viên khác.<br>- Chuẩn bị hệ thống cho giai đoạn kiểm thử tổng thể trong tuần tiếp theo. | 26/06/2026 | 26/06/2026 |  |

### Kết quả dự kiến tuần 10:

* Rà soát và hoàn thiện các chức năng backend cần thiết cho quá trình tích hợp.
* Thống nhất cấu trúc request và response giữa backend với các thành phần sử dụng API.
* Hoàn thành checklist kiểm tra kết nối giữa:

  * Frontend.
  * FastAPI backend.
  * Thành phần AI.
  * Amazon Cognito.
  * Amazon RDS.
  * Amazon EC2.

* Kiểm tra lại kết nối frontend đã được thiết lập từ tuần trước.
* Kiểm tra frontend gửi Access Token đúng định dạng khi gọi các API yêu cầu xác thực.
* Kiểm tra URL, phương thức HTTP, header, query parameter và request body do frontend gửi.
* Kiểm tra cấu hình CORS đối với localhost và địa chỉ frontend trên AWS Amplify.
* Kiểm tra cấu trúc response và mã trạng thái HTTP mà frontend nhận được.
* Kiểm tra khả năng trao đổi dữ liệu giữa backend và thành phần AI.
* Kiểm tra khả năng truy xuất dữ liệu công thức và dinh dưỡng thông qua backend.
* Ghi nhận và phân loại các lỗi theo từng thành phần của hệ thống.
* Điều chỉnh Pydantic Schema, endpoint, cấu hình CORS, biến môi trường và cách xử lý lỗi dựa trên kết quả tích hợp.
* Kiểm tra lại các luồng đã được điều chỉnh và xác nhận dữ liệu được truyền đúng định dạng.
* Cập nhật phiên bản backend đã điều chỉnh lên GitHub và triển khai trên Amazon EC2.
* Kiểm tra trạng thái hoạt động của backend sau khi triển khai phiên bản mới.
* Tổng hợp những nội dung chưa thể kiểm tra do còn phụ thuộc vào tiến độ của thành viên khác.
* Chuẩn bị phiên bản hệ thống cho hoạt động kiểm thử toàn bộ ở tuần tiếp theo.