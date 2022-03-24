REST - Representational State Transfer - Truyền Data thay vì User Interface

JSON - JavaScript Object Notation

API Endpoint - Sự kết hợp của một cặp HTTP Method và một Path cụ thể
HTTP Method (HTTP Verb)
GET - Get một Resource từ Server
POST - Post một Resource lên Server (create or append a Resource)
PUT - Put một Resource lên Server (create or overwrite a Resource)
PATCH - Update một phần của một Resource đã tồn tại trên Server
DELETE - Delete một Resource trên Server
OPTIONS - Quyết định Request tiếp theo có được cho phép hay không (được gửi tự động)
Với mỗi HTTP Method, có thể thực hiện bất cứ hành động gì mà không bị giới hạn, tuy nhiên nên tuân thủ những quy tắc trên

REST Principle

Uniform Interface - API Endpoint được định nghĩa rõ ràng với Request & Response Data Structure được định nghĩa rõ ràng

Stateless Interaction - Server và Client không lưu trữ bất kì lịch sử kết nối nào, mỗi Request được xử lí riêng biệt

Cacheable - Server có thể set Caching Header để cho phép Client cache Response
Client-Server - Server và Client là riêng biệt, Client không quan tâm tới lưu trữ dữ liệu lâu dài
Layered System - Server có thể forward Request tới API khác
Code on Demand - Executable Code có thể được truyền từ Server tới Client

CORS - Cross-Origin Resource Sharing
Client và Server cùng một Origin (Domain + Port) mặc định có thể tự do trao đổi dữ liệu
Client và Server khác Origin (Domain + Port) mặc định không thể tự do trao đổi dữ liệu => CORS Error
=> Chỉnh sửa Header của mỗi Response trả về từ Server
res.setHeader('Access-Control-Allow-Origin', '\*')
res.setHeader('Access-Control-Allow-Methods', 'GET, POST, PUT, PATCH, DELETE')
res.setHeader('Access-Control-Allow-Headers', 'Content-Type, Authorization')
