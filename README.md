Tạo một backend web cơ bản bằng Spring Boot (phiên bản mới nhất) sử dụng MySQL làm cơ sở dữ liệu.  
Yêu cầu chi tiết:
1. Cấu trúc project chuẩn Maven:
    - src/main/java/... (code)
    - src/main/resources/application.properties
    - pom.xml

2. Các chức năng cơ bản:
    - REST API cho entity "User" gồm: id, username, email, password.
    - Các endpoint:
      GET /api/users → lấy danh sách người dùng
      GET /api/users/{id} → lấy 1 người dùng
      POST /api/users → thêm mới
      PUT /api/users/{id} → cập nhật
      DELETE /api/users/{id} → xóa
    - Có xử lý lỗi cơ bản (UserNotFoundException, Validation, v.v.)

3. Cấu hình database:
    - Dùng MySQL
    - Cấu hình trong application.properties với các biến môi trường:
      spring.datasource.url=${DATABASE_URL}
      spring.datasource.username=${DATABASE_USERNAME}
      spring.datasource.password=${DATABASE_PASSWORD}
    - spring.jpa.hibernate.ddl-auto=update

5. Thêm file `.gitignore` chuẩn cho Spring Boot + Maven.


Mục tiêu: Dự án có thể chạy local và deploy trực tiếp lên Railway mà không cần chỉnh sửa thêm.