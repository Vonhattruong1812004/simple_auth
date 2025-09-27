# simple_auth

Đây là project thực hành về xác thực người dùng trong Node.js với hai kiểu: Basic Authentication và Cookie Authentication.

---

## Hướng dẫn test với POSTMAN

Sau khi đã cài đặt thư viện và chạy ứng dụng, bạn sử dụng POSTMAN để kiểm tra hai chức năng:

1. **Kiểm tra Basic Authentication:**
   - Trên POSTMAN, tạo một request mới với phương thức **GET**.
   - Nhập địa chỉ:
     ```
     http://localhost:3000/
     ```
   - Vào tab **Authorization**, chọn **Type** là `Basic Auth`.
     - Nhập **Username**: `admin`
     - Nhập **Password**: `123456`
   - Nhấn **Send** để gửi request.
   - Nếu thông tin đúng, bạn sẽ nhận về kết quả thành công. Nếu sai sẽ báo lỗi.

2. **Kiểm tra Cookie Authentication:**
   - Trên POSTMAN, tạo một request mới với phương thức **POST**.
   - Nhập địa chỉ:
     ```
     http://localhost:3001/login
     ```
   - Vào tab **Body**, chọn **raw** và định dạng là **JSON**.
     - Nhập vào:
       ```json
       {
         "username": "admin",
         "password": "12345"
       }
       ```
   - Nhấn **Send** để gửi request.
   - Sau khi đăng nhập thành công, chuyển sang tab **Cookies** trong POSTMAN để kiểm tra cookie mà server trả về. Bạn có thể dùng cookie này để test tiếp các API khác (nếu có).

---

## Ảnh kết quả test

### Kết quả test Basic Auth
![basic_auth_login](public/results/basic_auth_login.png)

### Kết quả test Cookie Auth
![cookie_auth_login](public/results/cookie_auth_login.png)

### Cookie sau khi đăng nhập
![cookie_auth_cookie](public/results/cookie_auth_cookie.png)