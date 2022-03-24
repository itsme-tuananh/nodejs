GraphQL API - Stateless, Client-Independent API for exchanging data with higher query flexibility

Cách GraphQL hoạt động
Một Node (+ Express) Server thông thường!
Client gửi Request tới Server thông qua MỘT Endpoint duy nhất (thông thường POST /graphql) (Sử dụng POST bởi POST Request Body chứa Query Expression (để định nghĩa Data Structure của Data được trả về))
Server-side Resolver phân tích Request Body, Fetch và Prepare và Return Data

Một GraphQL Query
{
query { | => Operation Type. Other Type: mutation, subscription
user { | => Operation 'Endpoint'
name |
age | => Requested Field
}
}
}

Operation Type
Query - Nhận Data ('GET')
Mutation - Thay đổi Data ('POST', 'PUT', 'PATCH', 'DELETE')
Subscription - Thiết lập kết nối thời gian thực thông qua Websocket

GraphQL Big Picture
Client => Server (POST /graphql) => Type Definition: Query Definition (như Route) | Mutation Definition (như Route) | Subscription Definition (như Route) => Resolver (chứa Server-side Logic) (như Controller)

Data được "lọc" ở Server và trả về Client. Client không cần "lọc" Data cần thiết từ Response với tất cả Data
