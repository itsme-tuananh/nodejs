Templating Engine
HTMLish Template = Node/Express Content + Templating Engine => Thay thế Placeholder/Snippet với HTML Content => HTML File

EJS - Sử dụng HTML thường và plain JavaScript trong template
Pug (Jade) - Sử dụng minimal HTML và custom template language
Handlebar - Sử dụng HTML thường và custom template language

app.set('key', 'value') - Set Global Configuration Value và có thể truy cập bằng app.get('key')
app.set('view engine', '...') - Thiết lập View Engine
app.set('views', '...') - Thiết lập thư mục views (chứa Template) (mặc định là views)
res.render('...', { Dynamic Data sử dụng trong Template }) - Render Template
