Cách Authentication được thực hiện
User = Login Request => Server - Database = Lưu thông tin User đã Authenticated => Session => Response (status code: 200) = Lưu Session ID => Cookie = Request Restricted Resource => ...

CSRF Attack - Cross-Site Request Forgery
Khiến User sử dụng một Fake Site (qua Link trong Mail,...) để gửi Request thực hiện một hành động nào đó tới Server (nhằm lợi dụng Session và Session Cookie của User đã login)

res.locals.someValueField - Set Local Variable (chỉ tồn tại trong View được render) được pass vào View
