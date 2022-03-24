Core Module
http - Launch Server, gửi Request
https - Launch SSL Server
...

Node.js Program Lifecycle
node app.js => Bắt đầu Script => Parse Code, Register Variable & Function => Event Loop (The Node Application) - Luôn chạy khi có Event Listener được registered => process.exit

Stream - Quá trình truyền tải dữ liệu ở Request Body tới Server theo từng phần nhỏ nhằm làm việc với Data sớm nhất có thể
Buffer - Cho phép làm việc với những phần dữ liệu được chia nhỏ trong quá trình Stream

Single Thread, Event Loop & Blocking Code
Incoming Request => <Your Code> (Single JavaScript Thread)
Event Loop (Xử lí Event Callback), bắt đầu chạy khi Code chạy
Worker Pool (Thực hiện "the Heavy Lifting", có thể chạy trên nhiều Thread khác nhau), Trigger Callback khi hoàn thành tác vụ được gửi đến
The Event Loop
=> Timers (Thực thi setTimeout, setInterval Callback)
=> Pending Callback (Thực thi I/O (Input & Output - Disk & Network Operation (~Blocking Operation)) -related Callback đã bị hoãn lại)
=> Poll (Nhận I/O Event mới, thực thi Callback của chúng (nếu có thể), hoặc hoãn thực thi và đưa về Pending Callback, hoặc nhảy về Timer Execution)
=> Check (Thực thi setImmediate() Callback)
=> Close Callback (Thực thi tất cả "Close" Event Callback)
=> process.exit (nếu refs == 0)

Import
const ... = require('core module / path')
Export
module.exports = ...
module.exports = {
key: value,
...
}
<=>
module.exports.key = value
...
=> Shortcut cho multiple export
exports.key = value
...

---

SUMMARY

Cách Web hoạt động
Client => Request => Server => Response => Client

Program Lifecycle & Event Loop
Node.js chạy non-blocking JS Code và sử dụng một Event-Driven Code ("Event Loop") để thực thi logic
Một chương trình Node thoát khi không còn tác vụ để thực thi
Lưu ý: createServer() Event mặc định không bao giờ hoàn thành

Asynchronous Code
JS Code là non-blocking
Sử dụng Callback và Event => Thứ tự thay đổi

Request & Response
Parse Request Data theo từng "Chunk" (Stream & Buffer)
Tránh "Double Response"

Node.js & Core Module
Node.js bao gồm nhiều Core Module (http, fs, path,...)
Core Module có thể được import vào bất cứ file nào để sử dụng
Import thông qua require('module')

The Node Module System
Import thông qua require('./path-to-file') với custom file hoặc require('module') với Core & Third-party Module
Export thông qua module.exports hoặc chỉ exports (với multiple export)
