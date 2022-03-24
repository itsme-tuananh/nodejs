Các loại lỗi khác nhau
Technical/Network Error - Show Error Page tới User
"Expected" Error - Thông báo với User, có thể thử lại
Bug/Logical Error - Fix trong Development
Làm việc với lỗi
Error được throw
=> Synchronous Code: try-catch | Asynchronous Code: then()-catch() => Trực tiếp xử lí lỗi | Sử dụng Express Error Handling Function
Không có Error được throw
=> Validate Value => Throw Error | Trực tiếp xử lí "Error"
==> Error Page | Intended Page/Response với thông tin lỗi | Redirect

next(error) - Khi gọi next() với một Error Object truyền vào làm tham số, khi có lỗi xảy ra sẽ bỏ qua hết những Middleware thông thường và thực thi Error Handling Middleware. Nếu có nhiều hơn một Error Handling Middleware, sẽ được thực thi theo thứ tự từ trên xuống
(error, req, res, next) => {
// Error Handling Middleware
}

throw new Error('...') ở Sync Code được xử lí tại Error Handling Middleware
throw new Error('...') ở Async Code không được xử lí tại Error Handling Middleware, phải dùng next(error)

Error & Http Response Code
2xx (Success)
200 - Hoạt động thành công
201 - Thành công, Resource được tạo
3xx (Redirect)
301 - Được di chuyển vĩnh viễn
4xx (Client-side Error)
401 - Chưa authenticated
403 - Chưa authorized
404 - Not found
422 - Invalid Input
5xx (Server-side Error)
500 - Server-side Error
