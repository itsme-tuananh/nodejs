Middleware - Những Function có cấu trúc (req, res, next) => { ... } được thực thi với mỗi Request được gửi đến
Request => Middleware =next()=> Middleware =res.send()=> Response
Sử dụng app.use((req, res, next) => { Thực thi với mỗi Request được gửi đến }) để sử dụng Middleware
Sử dụng next() cho phép Request tiếp tục tới Middleware tiếp theo

Request đi qua các Middleware theo thứ tự từ trên xuống dưới

.use() xử lí Request với bất cứ method nào
.get(),... sử dụng exact path thay vì match path như .use()

res.sendFile() nhận vào một đường dẫn tuyệt đối tới File được gửi đi
Sử dụng path.join() để tạo đường dẫn tuyệt đối tương thích với các File System khác nhau
\_\_dirname - Lưu trữ đường dẫn tuyệt đối tới thư mục chứa File sử dụng nó

public Folder chứa Content luôn được expose tới public và không cần permission để access
express.static() - Nhận vào đường dẫn tuyệt đối tới Folder chứa Static File và serve Static File (statically - Không được xử lí bởi Express Router hoặc Middleware khác mà trực tiếp được forward tới File System)
File Request sẽ được tự động forward tới Folder chứa Static File
