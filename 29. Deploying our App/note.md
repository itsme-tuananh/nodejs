Preparing the Code for Production
Sử dụng Environment Variable - Tránh hard-coded Value trong Code
Sử dụng Production API Key - Đừng có mà sử dụng Testing Stripe API
Giảm Error Output Detail - Không gửi thông tin nhạy cảm tới User
Set Secure Response Header - Implement best practice
Thêm Asset Compression - Giảm Response Size |
Thiết lập Logging - Cập nhập chuyện gì đang xảy ra |
Sử dụng SSL/TLS - Encrypt Data trong quá trình truyền tải | => Thường được xử lí bởi Hosting Provider

Thiết lập Environment Variable
Với Nodemon: Sử dụng nodemon.json
{
"env": {
"KEY": "VALUE",
"KEY": "VALUE",
...
}
}
Với Node: Sử dụng package.json
{
"scripts": {
"start": "KEY=VALUE KEY=VALUE ... node app.js"
}
}
NODE_ENV: Thường được tự động set bởi Hosting Provider, xác định Environment Mode của ứng dụng (Development hoặc Production)
