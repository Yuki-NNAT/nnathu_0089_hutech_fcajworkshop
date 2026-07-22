---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Kiểm tra và phân tích cấu trúc của các dataset đã lựa chọn.
* Làm sạch và chuẩn hóa dữ liệu công thức món ăn và dinh dưỡng.
* Kiểm tra chất lượng dữ liệu sau quá trình xử lý.
* Thiết kế cơ sở dữ liệu phù hợp với các chức năng của dự án.
* Xác định bảng, trường dữ liệu, khóa chính, khóa ngoại và quan hệ giữa các bảng.
* Tạo và cấu hình Amazon RDS for MySQL.
* Tạo các bảng cần thiết trên cơ sở dữ liệu.
* Import dữ liệu đã làm sạch vào Amazon RDS.
* Kiểm tra số lượng, cấu trúc và tính toàn vẹn của dữ liệu sau khi import.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Kiểm tra cấu trúc của dataset Food.com Recipes and Interactions.<br>- Xác định các trường dữ liệu cần sử dụng cho chức năng tìm kiếm và gợi ý món ăn.<br>- Phân tích kiểu dữ liệu, giá trị thiếu, dữ liệu không hợp lệ và các bản ghi trùng lặp.<br>- Kiểm tra các trường có cấu trúc phức tạp như nguyên liệu, nguyên liệu thô, bước chế biến và thẻ phân loại.<br>- Xây dựng quy trình tiền xử lý dữ liệu công thức bằng Python và pandas. | 25/05/2026 | 25/05/2026 | <https://www.kaggle.com/datasets/realalexanderwei/food-com-recipes-with-ingredients-and-tags/data> |
| 3 | - Làm sạch và chuẩn hóa dữ liệu công thức món ăn.<br>- Chuyển đổi các trường nguyên liệu, bước chế biến và thẻ phân loại về cấu trúc thống nhất.<br>- Phân tích và xử lý các bản ghi trùng lặp.<br>- Bổ sung các trường thống kê như số lượng nguyên liệu, số bước chế biến và số thẻ phân loại.<br>- Kiểm tra lại các trường bắt buộc và loại bỏ những bản ghi không đáp ứng yêu cầu.<br>- Phân tích dữ liệu USDA FoodData Central và trích xuất các trường cần thiết cho việc tra cứu calories.<br>- Chuẩn hóa dữ liệu dinh dưỡng thành cấu trúc phù hợp để import vào MySQL. | 26/05/2026 | 26/05/2026 | <https://fdc.nal.usda.gov/data-documentation.html> |
| 4 | - Thiết kế cơ sở dữ liệu cho dự án AI Recipe Finder.<br>- Xác định các thực thể chính gồm người dùng, công thức món ăn, dinh dưỡng, món ăn yêu thích, lịch sử tìm kiếm và lịch sử trò chuyện.<br>- Thiết kế các bảng `users`, `recipes`, `nutrition`, `favorites`, `search_history` và `chat_history`.<br>- Xác định kiểu dữ liệu, khóa chính, khóa ngoại và các ràng buộc cần thiết.<br>- Xác định các trường dữ liệu công thức có cấu trúc phức tạp sẽ được lưu dưới dạng JSON.<br>- Thiết kế index cho các trường thường xuyên được tìm kiếm hoặc sử dụng trong quan hệ giữa các bảng.<br>- Hoàn thiện tệp SQL tạo bảng và index. | 27/05/2026 | 27/05/2026 |  |
| 5 | - Tạo Amazon RDS DB instance sử dụng MySQL.<br>- Cấu hình khu vực triển khai, phiên bản MySQL, lớp DB instance và dung lượng lưu trữ.<br>- Thiết lập tên người dùng quản trị và thông tin kết nối cơ sở dữ liệu.<br>- Cấu hình VPC, subnet, Public access và Security Group.<br>- Thiết lập quy tắc truy cập cổng MySQL 3306 từ địa chỉ IP được cho phép.<br>- Kiểm tra trạng thái DB instance và lấy endpoint kết nối.<br>- Kết nối Amazon RDS từ MySQL Workbench bằng kết nối SSL.<br>- Tạo database và chạy tệp SQL để khởi tạo các bảng. | 28/05/2026 | 28/05/2026 | <https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.CreatingConnecting.MySQL.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ConnectToInstance.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.SSL.html> |
| 6 | - Xây dựng và chạy chương trình Python để import dữ liệu đã làm sạch vào Amazon RDS.<br>- Import dữ liệu dinh dưỡng vào bảng `nutrition`.<br>- Import dữ liệu công thức vào bảng `recipes` theo từng batch để hạn chế lỗi và sử dụng tài nguyên hiệu quả.<br>- Kiểm tra và xử lý các bản ghi có dữ liệu JSON không hợp lệ trong quá trình import.<br>- Đối chiếu số lượng bản ghi trước và sau khi nhập dữ liệu.<br>- Thực hiện các truy vấn mẫu để kiểm tra dữ liệu công thức và dinh dưỡng.<br>- Kiểm tra khóa chính, khóa ngoại, index và các ràng buộc của cơ sở dữ liệu.<br>- Tổng hợp kết quả và xác nhận dữ liệu sẵn sàng cho quá trình phát triển backend. | 29/05/2026 | 29/05/2026 |  |

### Kết quả đạt được tuần 6:

* Hoàn thành quá trình phân tích, làm sạch và chuẩn hóa dataset công thức món ăn từ Food.com.

* Dữ liệu công thức sau khi xử lý bao gồm các thông tin chính:

  * Mã công thức.
  * Tên món ăn.
  * Mô tả.
  * Danh sách nguyên liệu đã chuẩn hóa.
  * Danh sách nguyên liệu nguyên bản.
  * Các bước chế biến.
  * Số khẩu phần và kích thước khẩu phần.
  * Thẻ phân loại.
  * Các trường thống kê về nguyên liệu, bước chế biến và thẻ.

* Hoàn thành quá trình xử lý dữ liệu USDA FoodData Central.

* Dữ liệu dinh dưỡng được chuẩn hóa thành các trường chính:

  * Mã thực phẩm `fdc_id`.
  * Tên thực phẩm.
  * Loại dữ liệu.
  * Lượng calories.

* Hoàn thành kiểm tra chất lượng dữ liệu sau khi làm sạch:

  * Kiểm tra cấu trúc và kiểu dữ liệu.
  * Kiểm tra dữ liệu thiếu.
  * Kiểm tra bản ghi trùng lặp.
  * Kiểm tra các trường JSON.
  * Kiểm tra các giá trị không hợp lệ.
  * Kiểm tra ngẫu nhiên một số bản ghi sau xử lý.

* Hoàn thành thiết kế cơ sở dữ liệu cho dự án với các bảng:

  * `users`: Lưu thông tin người dùng được đồng bộ từ Amazon Cognito.
  * `recipes`: Lưu dữ liệu công thức món ăn.
  * `nutrition`: Lưu dữ liệu thực phẩm và calories.
  * `favorites`: Lưu danh sách món ăn yêu thích của người dùng.
  * `search_history`: Lưu lịch sử tìm kiếm.
  * `chat_history`: Lưu lịch sử trò chuyện với chatbot.

* Xác định được quan hệ chính giữa các bảng:

  * Một người dùng có thể lưu nhiều món ăn yêu thích.
  * Một công thức có thể được nhiều người dùng yêu thích.
  * Một người dùng có thể có nhiều lịch sử tìm kiếm.
  * Một người dùng có thể có nhiều nội dung trong lịch sử trò chuyện.
  * Dữ liệu người dùng liên kết với Amazon Cognito thông qua `cognito_sub`.

* Áp dụng khóa chính, khóa ngoại, ràng buộc duy nhất và index phù hợp để bảo đảm tính toàn vẹn và hỗ trợ truy vấn dữ liệu.

* Tạo thành công Amazon RDS DB instance với MySQL và hoàn thành các cấu hình cơ bản:

  * Lựa chọn phiên bản và lớp DB instance.
  * Cấu hình dung lượng lưu trữ.
  * Cấu hình VPC và Security Group.
  * Cấu hình cổng kết nối MySQL 3306.
  * Lấy endpoint của DB instance.
  * Kết nối bằng MySQL Workbench.
  * Sử dụng SSL để bảo vệ kết nối đến cơ sở dữ liệu.

* Tạo thành công database `food_ai_db` trên Amazon RDS và khởi tạo các bảng theo thiết kế.

* Import thành công dữ liệu vào Amazon RDS:

  * **Bảng `nutrition`:** 13.359 bản ghi.
  * **Bảng `recipes`:** Khoảng 402.000 bản ghi hợp lệ.

* Xác định một số bản ghi công thức không thể import do dữ liệu JSON không hợp lệ và thực hiện bỏ qua các bản ghi này để bảo đảm chất lượng cơ sở dữ liệu.

* Kiểm tra dữ liệu sau khi import bằng các truy vấn:

  * Đếm tổng số bản ghi trong từng bảng.
  * Truy vấn ngẫu nhiên dữ liệu công thức.
  * Kiểm tra danh sách nguyên liệu và bước chế biến.
  * Truy vấn dữ liệu calories theo mã thực phẩm.
  * Kiểm tra cấu trúc bảng, index và ràng buộc.

* Xác nhận hai bảng `recipes` và `nutrition` là nguồn dữ liệu tĩnh, chỉ đọc sau khi hoàn tất import.

* Hoàn thành việc chuẩn bị cơ sở dữ liệu trên Amazon RDS, sẵn sàng cho quá trình xây dựng và kết nối backend FastAPI trong tuần tiếp theo.