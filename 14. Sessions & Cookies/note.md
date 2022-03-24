Cookie được lưu trữ trên Client-Side
Server set Cookie thông qua Response Header
Cookie sau khi được set sẽ tự động được đính kèm với từng Request tới Server

Expire= - Set thời gian hết hạn (Thời điểm hết hạn)
Max-Age= - Set thời gian hết hạn (Thời gian tồn tại)
Domain= - Set Domain nhận Cookie (Có thể được sử dụng để track User)
Secure - Cookie chỉ được set nếu sử dụng HTTPS
HttpOnly - Ngăn chặn truy cập Cookie thông qua Client-Side JavaScript

Session Cookie - expire khi đóng Browser
Permanent Cookie - expire khi tới một Age/Expiry Date nhất định

Session được lưu trữ trên Server-Side (Session Storage trong Database)
Liên kết với User/Client thông qua Cookie (Cookie lưu Id (hashed) của Session) (Có thể là Session Cookie hoặc Permanent Cookie)
