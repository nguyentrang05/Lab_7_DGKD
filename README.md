# Thực hành Postman
## Giới thiệu về Postman
- Postman hiện là một trong những công cụ phổ biến nhất được sử dụng trong kiểm thử API. Nó bắt đầu vào năm 2012 như một dự án phụ của Abhinav Asthana để đơn giản hóa quy trình làm việc API trong kiểm thử và phát triển. API là viết tắt của giao diện lập trình ứng dụng cho phép các ứng dụng phần mềm giao tiếp với nhau thông qua các lệnh gọi API.

- Với hơn 4 triệu người dùng hiện nay, Postman đã trở thành một công cụ được lựa chọn vì những lý do sau:

+ Khả năng truy cập - Để sử dụng Postman, người ta chỉ cần đăng nhập vào tài khoản của chính họ để dễ dàng truy cập các tệp mọi lúc, mọi nơi miễn là ứng dụng Postman được cài đặt trên máy tính.
+ Sử dụng Collection - Postman cho phép người dùng tạo collection cho các lệnh gọi API của họ. Mỗi collection có thể tạo các thư mục con và nhiều yêu cầu. Điều này giúp tổ chức lại các bộ kiểm thử của bạn.
+ Cộng tác - Collection và môi trường có thể được nhập hoặc xuất để dễ dàng chia sẻ tệp. Một liên kết trực tiếp cũng có thể được sử dụng để chia sẻ collection.
+ Tạo môi trường - Có nhiều môi trường hỗ trợ ít lặp lại các bài kiểm tra vì người ta có thể sử dụng cùng một collection nhưng cho một môi trường khác. Đây là nơi tham số hóa sẽ diễn ra mà chúng ta sẽ thảo luận trong các bài học tiếp theo.
+ Tạo các kiểm thử - Các điểm checkpoint như xác minh trạng thái phản hồi HTTP thành công có thể được thêm vào mỗi lệnh gọi API giúp đảm bảo phạm vi kiểm tra.
+ Kiểm thử tự động hóa - Thông qua việc sử dụng Collection Runner hoặc Newman, các bài kiểm thử có thể được chạy trong nhiều lần lặp lại tiết kiệm thời gian cho các bài kiểm thử lặp đi lặp lại.
+ Gỡ lỗi - Bảng điều khiển Postman giúp kiểm tra dữ liệu nào đã được truy xuất giúp dễ dàng gỡ lỗi kiểm thử.
+ Tích hợp liên tục - Với khả năng hỗ trợ tích hợp liên tục, các hoạt động phát triển được duy trì.
<img width="1600" height="1002" alt="image" src="https://github.com/user-attachments/assets/4aa5af01-0b31-4bd6-b3e2-5bda7e8ce5d4" />
**Hình 1. Giao diện của Postman**

## Thực hành kiểm thử API với Postman
API kiểm thử: `https://www.freepublicapis.com/free-music-api-2`

### GET Request – Tìm kiếm nghệ sĩ
Sử dụng phương thức `GET` để gửi yêu cầu tìm kiếm thông tin nghệ sĩ thông qua API của TheAudioDB.

| Thành phần | Giá trị |
|---|---|
| Method | `GET` |
| Endpoint |`/api/v1/json/123/search.php` |
| Query Parameter | `s=coldplay` |
| Status Code | `200 OK` |

 Kết quả: API trả về `200 OK` và thông tin của nghệ sĩ Coldplay dưới dạng JSON.

<img width="1601" height="1000" alt="image" src="https://github.com/user-attachments/assets/1b094550-7505-44a7-bb1b-c0b728a4eeb1" />
**Hình 2. Thực hiện GET Request tìm kiếm nghệ sĩ bằng Postman**

### GET Request – Tìm kiếm album

Sử dụng phương thức `GET` để tìm kiếm danh sách album của một nghệ sĩ thông qua API TheAudioDB.

| Thành phần | Giá trị |
|---|---|
| Method | `GET` |
| Endpoint | `/api/v1/json/123/searchalbum.php` |
| Query Parameter | `s=coldplay` |
| Status Code | `200 OK` |

Kết quả trả về là dữ liệu JSON chứa thông tin các album của nghệ sĩ Coldplay.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2eb09ba7-7c2c-4ca8-b695-2da6373c8883" />
**Hình 3. Thực hiện GET Request tìm kiếm Album bằng Postman**

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9e2f80ea-ea28-49d3-a592-6d6fd52eb858" />
**Hình 4. Thực hiện GET Request tìm kiếm Track bằng Postman**

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8b576bd8-1123-45d1-9af9-80f0f9a1f341" />
**Hình 5. Thực hiện GET Request tìm kiếm Track bằng Postman**

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4ce113ba-9deb-4b4d-b042-d9b89cc35ef7" />
**Hình 6. Thực hiện Post Request create post bằng Postman**

