---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Nghiên cứu các dịch vụ Amazon RDS, Amazon EC2 và Amazon Cognito.
* Tìm hiểu chức năng, thành phần và cách hoạt động của từng dịch vụ.
* Đánh giá vai trò của các dịch vụ trong dự án AI Recipe Finder.
* Tìm hiểu cách backend kết nối và truy vấn dữ liệu từ Amazon RDS.
* Tìm hiểu cách Amazon Cognito xác thực người dùng cho frontend và backend.
* Tìm hiểu phương thức kết nối giữa Amazon EC2, Amazon RDS và Amazon Cognito.
* Xác định các yêu cầu cơ bản về mạng, phân quyền và bảo mật khi kết nối các dịch vụ AWS.

### Các công việc thực hiện trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Nghiên cứu tổng quan về Amazon RDS.<br>- Tìm hiểu vai trò của Amazon RDS trong việc triển khai và quản lý cơ sở dữ liệu quan hệ trên AWS.<br>- Tìm hiểu các thành phần cơ bản như DB instance, database engine, storage, endpoint, port và backup.<br>- Khảo sát các hệ quản trị cơ sở dữ liệu được Amazon RDS hỗ trợ.<br>- Xem xét khả năng sử dụng Amazon RDS for MySQL để lưu trữ dữ liệu món ăn, dinh dưỡng, người dùng và lịch sử hoạt động của dự án. | 11/05/2026 | 11/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.html> |
| 3 | - Nghiên cứu tổng quan về Amazon EC2.<br>- Tìm hiểu chức năng của EC2 trong việc cung cấp máy chủ ảo trên AWS.<br>- Tìm hiểu các thành phần như EC2 instance, Amazon Machine Image, instance type, key pair, storage và Elastic IP.<br>- Tìm hiểu Security Group và các quy tắc inbound, outbound.<br>- Xem xét khả năng sử dụng EC2 để triển khai và vận hành backend FastAPI của dự án. | 12/05/2026 | 12/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/><br><https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html><br><https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html> |
| 4 | - Nghiên cứu tổng quan về Amazon Cognito.<br>- Tìm hiểu vai trò của Cognito trong việc quản lý đăng ký, đăng nhập và xác thực người dùng.<br>- Tìm hiểu User Pool, App Client, Hosted UI và các thông tin xác thực dạng token.<br>- Tìm hiểu quy trình đăng ký, xác nhận tài khoản, đăng nhập và đăng xuất.<br>- Xem xét cách sử dụng Cognito để bảo vệ những chức năng yêu cầu đăng nhập, đặc biệt là chatbot AI và dữ liệu cá nhân của người dùng. | 13/05/2026 | 13/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/><br><https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html><br><https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools.html> |
| 5 | - Tìm hiểu phương thức kết nối giữa Amazon EC2 và Amazon RDS.<br>- Nghiên cứu vai trò của VPC, subnet, endpoint, port và Security Group trong quá trình kết nối.<br>- Tìm hiểu cách backend trên EC2 sử dụng thông tin kết nối để truy cập cơ sở dữ liệu RDS.<br>- Tìm hiểu cách giới hạn quyền truy cập cơ sở dữ liệu bằng Security Group thay vì mở kết nối cho tất cả địa chỉ IP.<br>- Xem xét các biện pháp bảo vệ thông tin đăng nhập cơ sở dữ liệu và sử dụng kết nối mã hóa. | 14/05/2026 | 14/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ConnectToInstance.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/database-authentication.html> |
| 6 | - Tìm hiểu luồng kết nối giữa frontend, Amazon Cognito, backend trên EC2 và Amazon RDS.<br>- Nghiên cứu cách frontend chuyển người dùng đến Cognito để đăng nhập và nhận token xác thực.<br>- Tìm hiểu cách frontend gửi token kèm theo yêu cầu API đến backend.<br>- Tìm hiểu cách backend kiểm tra token trước khi xử lý các API được bảo vệ.<br>- Xác định rằng backend sử dụng thông tin người dùng đã xác thực để truy vấn hoặc cập nhật dữ liệu tương ứng trong Amazon RDS.<br>- Tổng hợp vai trò và phương thức kết nối giữa các dịch vụ đã nghiên cứu. | 15/05/2026 | 15/05/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools.html><br><https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-user-pools-using-tokens-with-identity-providers.html><br><https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html> |

### Kết quả đạt được tuần 4:

* Hiểu được Amazon RDS là dịch vụ cơ sở dữ liệu quan hệ được quản lý trên AWS.

* Xác định Amazon RDS for MySQL có thể được sử dụng để lưu trữ:

  * Dữ liệu công thức và thông tin món ăn.
  * Dữ liệu dinh dưỡng.
  * Thông tin người dùng.
  * Danh sách món ăn yêu thích.
  * Lịch sử tìm kiếm và lịch sử trò chuyện.

* Hiểu được các thành phần cơ bản của Amazon RDS:

  * DB instance.
  * Database engine.
  * Endpoint và port.
  * Storage.
  * Backup.
  * Security Group.

* Hiểu được Amazon EC2 cung cấp máy chủ ảo để triển khai và vận hành ứng dụng trên AWS.

* Xác định Amazon EC2 có thể được sử dụng để triển khai backend FastAPI của dự án AI Recipe Finder.

* Hiểu được các thành phần EC2 cơ bản như:

  * Amazon Machine Image.
  * Instance type.
  * Key pair.
  * Security Group.
  * Storage.
  * Public IP và Elastic IP.

* Hiểu được Security Group hoạt động như một tường lửa ảo, kiểm soát lưu lượng truy cập vào và ra khỏi tài nguyên AWS.

* Hiểu được Amazon Cognito hỗ trợ quản lý đăng ký, đăng nhập, đăng xuất và xác thực người dùng.

* Tìm hiểu được các thành phần chính của Amazon Cognito:

  * **User Pool:** Quản lý tài khoản và thông tin người dùng.
  * **App Client:** Đại diện cho ứng dụng sử dụng Cognito để xác thực.
  * **Hosted UI:** Cung cấp giao diện đăng ký và đăng nhập được Cognito quản lý.
  * **Token:** Chứa thông tin và trạng thái xác thực của người dùng.

* Xác định Cognito sẽ được sử dụng để bảo vệ chatbot AI và các API liên quan đến dữ liệu cá nhân.

* Hiểu được phương thức kết nối cơ bản giữa EC2 và RDS:

  1. Backend FastAPI được triển khai trên EC2.
  2. Backend sử dụng endpoint, port và thông tin đăng nhập để kết nối RDS.
  3. Security Group của RDS chỉ cho phép kết nối từ EC2 trên cổng cơ sở dữ liệu cần thiết.
  4. Backend thực hiện truy vấn và trả kết quả về frontend thông qua API.

* Xác định được luồng xác thực dự kiến:

  1. Người dùng truy cập frontend.
  2. Frontend chuyển người dùng đến Amazon Cognito để đăng ký hoặc đăng nhập.
  3. Cognito xác thực thông tin và trả token cho frontend.
  4. Frontend gửi token trong các yêu cầu đến API được bảo vệ.
  5. Backend kiểm tra tính hợp lệ của token.
  6. Backend xử lý yêu cầu và truy cập dữ liệu tương ứng trong Amazon RDS.
  7. Kết quả được trả về frontend để hiển thị cho người dùng.

* Hiểu được vai trò của VPC, subnet, Security Group, endpoint và port trong việc kết nối các dịch vụ.

* Nhận biết được một số yêu cầu bảo mật cơ bản:

  * Không công khai thông tin đăng nhập cơ sở dữ liệu.
  * Không mở cổng RDS cho toàn bộ Internet nếu không cần thiết.
  * Chỉ cho phép những nguồn phù hợp kết nối đến EC2 và RDS.
  * Kiểm tra token trước khi cho phép truy cập API được bảo vệ.
  * Áp dụng nguyên tắc đặc quyền tối thiểu khi phân quyền.
  * Ưu tiên sử dụng kết nối được mã hóa khi truyền dữ liệu.

* Hoàn thành mục tiêu nghiên cứu Amazon RDS, Amazon EC2 và Amazon Cognito, tạo cơ sở để tiếp tục hoàn thiện kiến trúc và workflow của dự án trong tuần tiếp theo.