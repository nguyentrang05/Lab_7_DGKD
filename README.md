# Thực hành Postman
## Giới thiệu về Postman
Postman hiện là một trong những công cụ phổ biến nhất được sử dụng trong kiểm thử API. Nó bắt đầu vào năm 2012 như một dự án phụ của Abhinav Asthana để đơn giản hóa quy trình làm việc API trong kiểm thử và phát triển. API là viết tắt của giao diện lập trình ứng dụng cho phép các ứng dụng phần mềm giao tiếp với nhau thông qua các lệnh gọi API.

Với hơn 4 triệu người dùng hiện nay, Postman đã trở thành một công cụ được lựa chọn vì những lý do sau:

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
### GET Request – Tìm kiếm bài hát

Sử dụng phương thức `GET` để tìm kiếm thông tin bài hát thông qua API của TheAudioDB.

| Thành phần | Giá trị |
|---|---|
| Method | `GET` |
| Endpoint | `/api/v1/json/123/searchtrack.php` |
| Query Parameter | `s=coldplay`, `t=yellow` |
| Status Code | `200 OK` |

Trong đó, `s` là tên nghệ sĩ và `t` là tên bài hát. API trả về thông tin của bài hát "Yellow" thuộc nghệ sĩ Coldplay dưới dạng JSON.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9e2f80ea-ea28-49d3-a592-6d6fd52eb858" />

**Hình 4. Thực hiện GET Request tìm kiếm Track bằng Postman**
### GET Request – Sử dụng HTTP Header

Thực hiện GET Request kết hợp với HTTP Header để chỉ định định dạng dữ liệu mà client mong muốn nhận từ API.

| Thành phần | Giá trị |
|---|---|
| Method | `GET` |
| Endpoint | `/api/v1/json/123/search.php` |
| Query Parameter | `s=coldplay` |
| Header | `Accept: application/json` |
| Status Code | `200 OK` |

Header `Accept: application/json` cho biết client mong muốn server trả về dữ liệu dưới dạng JSON.

Kết quả trả về là thông tin của nghệ sĩ Coldplay dưới dạng JSON.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8b576bd8-1123-45d1-9af9-80f0f9a1f341" />

**Hình 5. Thực hiện GET Request với Header bằng Postman**
### POST Request – Tạo dữ liệu

Sử dụng phương thức `POST` để gửi dữ liệu lên API và mô phỏng việc tạo một bài viết mới.

| Thành phần | Giá trị |
|---|---|
| Method | `POST` |
| Endpoint | `https://jsonplaceholder.typicode.com/posts` |
| Request Body | JSON |
| Status Code | `201 Created` |

Dữ liệu được gửi trong Request Body:

```json
{
    "title": "Postman Testing",
    "body": "This is a test post.",
    "userId": 1
}
```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4ce113ba-9deb-4b4d-b042-d9b89cc35ef7" />

**Hình 6. Thực hiện Post Request create post bằng Postman**
### PUT Request – Cập nhật dữ liệu

Sử dụng phương thức `PUT` để cập nhật toàn bộ thông tin của một bài viết.

| Thành phần | Giá trị |
|---|---|
| Method | `PUT` |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Request Body | JSON |
| Status Code | `200 OK` |

Dữ liệu được gửi trong Request Body:

```json
{
    "id": 1,
    "title": "Postman Testing Updated",
    "body": "This post has been updated using PUT.",
    "userId": 1
}
```
<img width="966" height="1027" alt="image" src="https://github.com/user-attachments/assets/803e94b0-471c-4281-a1cc-413d01c4090f" />

**Hình 7. Thực hiện Put Request update post bằng Postman**
### PATCH Request – Cập nhật một phần dữ liệu

Sử dụng phương thức `PATCH` để cập nhật một phần thông tin của bài viết.

| Thành phần | Giá trị |
|---|---|
| Method | `PATCH` |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Request Body | JSON |
| Status Code | `200 OK` |

Trong request này, chỉ trường `title` được cập nhật:

```json
{
    "title": "Postman Testing with PATCH"
}
```
<img width="966" height="1038" alt="image" src="https://github.com/user-attachments/assets/0a22ae0a-f5db-4fb1-a806-47b75d690686" />

**Hình 8. Thực hiện Patch Request update post bằng Postman**
### DELETE Request – Xóa dữ liệu

Sử dụng phương thức `DELETE` để gửi yêu cầu xóa một bài viết.

| Thành phần | Giá trị |
|---|---|
| Method | `DELETE` |
| Endpoint | `https://jsonplaceholder.typicode.com/posts/1` |
| Status Code | `200 OK` |
| Request Body | Không có |

DELETE Request không yêu cầu Request Body trong trường hợp này. API trả về `200 OK`, cho biết yêu cầu đã được xử lý thành công.

<img width="967" height="1021" alt="image" src="https://github.com/user-attachments/assets/f2c321eb-0c16-4d9f-98aa-e5f3c0077f94" />

**Hình 9. Thực hiện Delete Request bằng Postman**

### Test Script – Kiểm thử tự động Response

Postman cho phép sử dụng Test Script để tự động kiểm tra kết quả trả về từ API.

Trong bài thực hành, thực hiện kiểm tra HTTP Status Code:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response contains artists", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData.artists).to.not.be.empty;
});
```
<img width="967" height="1027" alt="image" src="https://github.com/user-attachments/assets/7c741081-17a0-4a86-b444-0aae9c736687" />

**Hình 10. Thực hiện Test Script bằng Postman**
