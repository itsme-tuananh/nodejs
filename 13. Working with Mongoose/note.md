ODM - Object-Document Mapping

Core Concept
Schema & Model - User
Instance - const user = new User()
Query - User.find()

"modals" Collection sẽ được tạo tự động với mỗi "Model" được định nghĩa
Sử dụng Object trong phép gán sẽ tự động gán \_id của Object đó
.populate() - Tham chiếu Document trong Collection khác
.select() - Tùy chọn Field sẽ được truy vấn
ref - Model được sử dụng trong quá trình populate

.\_doc - Truy cập tất cả Field trong một Object từ một \_id
