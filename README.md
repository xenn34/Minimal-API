Tóm tắt kiến thức bản thânm học được về Minimal APIs

1. Khái niệm Minimal APIs
- Minimal APIs là cách tạo các API HTTP (kiểu dịch vụ web) với cú pháp đơn giản, dễ hiểu và ít phụ thuộc vào các thành phần phức tạp.  
- Điểm nổi bật của Minimal APIs là **gọn gàng** và **hiệu quả**, rất phù hợp khi bạn muốn làm các ứng dụng nhỏ hoặc **microservices** (các dịch vụ nhỏ trong hệ thống lớn).

2. Cách lưu dữ liệu: Entity Framework Core với In-Memory Database
- Đây là công cụ quản lý dữ liệu dễ dàng.  
- In-Memory Database giống một "cơ sở dữ liệu tạm thời" chạy trên bộ nhớ, không cần cài đặt phức tạp.  
- Phù hợp cho **test code** hoặc các dự án không muốn mất thời gian setup database thật.

3. Các phương thức làm việc với dữ liệu trong API:
- **GET:** Dùng để **lấy dữ liệu** từ server.
- **POST:** Khi cần **thêm dữ liệu mới**
- **PUT:** Dùng để **cập nhật toàn bộ** một mục nào đó.
- **DELETE:** Dùng để **xóa** dữ liệu trên server.

4. Sự khác biệt giữa PUT và PATCH:
- **PUT:** Gửi **toàn bộ** dữ liệu của mục cần sửa. Nghĩa là mình phải gửi cả những phần không thay đổi.  
  - Ví dụ: Nếu muốn đổi tên khách hàng, mình vẫn phải gửi cả địa chỉ, số điện thoại... dù nó không thay đổi.  
- **PATCH:** Gửi **một phần** dữ liệu để cập nhật. Chỉ cần gửi những gì cần thay đổi, tiết kiệm băng thông hơn.  
  - Ví dụ: Chỉ gửi phần "tên khách hàng" mới thay vì toàn bộ thông tin.

5. TypedResults: Tối ưu hóa API
- Đây là cách để cải thiện **khả năng kiểm thử** và giúp tạo tài liệu API (OpenAPI) dễ dàng hơn.  
- TypedResults trả về các kết quả rõ ràng hơn, như "200 OK", "404 Not Found", giúp ta dễ dàng xử lý hơn khi test ứng dụng.

6. Dependency Injection (DI): Quản lý phụ thuộc
- DI giúp bạn thêm các thành phần như **database context** vào ứng dụng một cách gọn gàng.  

7. Quản lý lỗi trong ứng dụng
- Trong môi trường **phát triển**, ta có thể cấu hình để hiển thị chi tiết lỗi liên quan đến cơ sở dữ liệu.  
- Điều này rất hữu ích để debug và tìm nguyên nhân lỗi nhanh chóng.

8. Cấu hình route dễ dàng với MapGroup
- Minimal APIs cho phép nhóm các route lại với nhau bằng cách sử dụng MapGroup.  
- Điều này giúp gọn gàng hơn và dễ quản lý khi ứng dụng có nhiều API.

9. Kestrel Web Server
- Kestrel là **máy chủ web mặc định** dùng để chạy và kiểm tra ứng dụng.  
- Không cần cấu hình gì nhiều, chỉ cần chạy là ứng dụng sẽ hoạt động ngay lập tức.
