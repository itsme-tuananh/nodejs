Cách Authentication hoạt động trong RESTful API
Client gửi Request với Auth Data tới Server
=> Server trả về cho Client một Token (được tạo bởi Server và chỉ có thể được xác thực bởi chính Server đó)
=> Client lưu Token trong Storage (Browser Storage)
=> Token đã được lưu trữ được gửi đi cùng để xác thực Request tiếp theo

Token
JSON Data + Signature (có thể được xác nhận bởi Server (thông qua Secret Key)) => JSON Web Token (JWT)

Authorization Header của Request chứa Token với định dạng: 'Bearer ' + JWT => Một Convention (không bắt buộc) biểu thị rằng đây là một Authentication Token, thường sử dụng cho JSON Web Token
