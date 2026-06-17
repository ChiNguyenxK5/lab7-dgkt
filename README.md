# BÁO CÁO KIỂM THỬ API

**Tên Dự Án:** Test Collection of APIs

**Ngày Kiểm Thử:** 17/06/2026

**Người Kiểm Thử:** Nguyễn Mạnh Chí

---

# 1. Mục Tiêu Kiểm Thử

Sử dụng Postman để kiểm thử các API RESTful công khai của JSONPlaceholder nhằm đánh giá khả năng gửi yêu cầu HTTP, xử lý dữ liệu và phản hồi từ máy chủ.

---

# 2. Môi Trường Kiểm Thử

* Công cụ: Postman Desktop
* API được sử dụng: JSONPlaceholder
* URL cơ sở:

```text
https://jsonplaceholder.typicode.com
```

---

# 3. Phương Pháp Kiểm Thử

* Kiểm thử thủ công trên Postman.
* Gửi các yêu cầu GET, POST, PUT.
* Kiểm tra mã trạng thái HTTP (Status Code).
* So sánh kết quả thực tế với kết quả mong đợi.

---

# 4. Kịch Bản Kiểm Thử

---

## Kịch Bản Kiểm Thử Lần 1

### Tên Kịch Bản

Kiểm thử lấy danh sách bài viết

### Mục Đích

Kiểm tra khả năng truy xuất dữ liệu từ API bằng phương thức GET.

### Phương Thức HTTP

```text
GET
```

### URL

```text
https://jsonplaceholder.typicode.com/posts
```

### Tham Số

Không có

### Kết Quả Mong Đợi

Trả về danh sách các bài viết dưới dạng JSON.

### Kết Quả Thực Tế

API trả về danh sách bài viết thành công.

### Trạng Thái

✅ Thành công

### Kết quả sau khi kiểm thử

<img width="1920" height="1020" alt="Screenshot 2026-06-17 075507" src="https://github.com/user-attachments/assets/b3dd1bfa-15b8-4d36-bb41-bbda884389b3" />


### Kết quả kiểm thử chi tiết

```json
[
  {
    "userId": 1,
    "id": 1,
    "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
    "body": "quia et suscipit..."
  },
  {
    "userId": 1,
    "id": 2,
    "title": "qui est esse",
    "body": "est rerum tempore vitae..."
  }
]
```

### Mã trạng thái trả về

```text
200 OK
```

---

## Kịch Bản Kiểm Thử Lần 2

### Tên Kịch Bản

Kiểm thử cập nhật dữ liệu bài viết

### Mục Đích

Kiểm tra khả năng cập nhật dữ liệu bằng phương thức PUT.

### Phương Thức HTTP

```text
PUT
```

### URL

```text
https://jsonplaceholder.typicode.com/posts/1
```

### Dữ Liệu Gửi Đi

```json
{
  "id": 1,
  "title": "update test",
  "body": "update hello",
  "userId": 1
}
```

### Kết Quả Mong Đợi

API nhận dữ liệu và trả về nội dung đã được cập nhật.

### Kết Quả Thực Tế

API trả về dữ liệu cập nhật thành công.

### Trạng Thái

✅ Thành công

### Kết quả sau khi kiểm thử

<img width="1920" height="1020" alt="Screenshot 2026-06-17 075814" src="https://github.com/user-attachments/assets/6c0ea72d-7998-4a32-adc8-8360323c9f95" />

### Kết quả kiểm thử chi tiết

```json
{
  "id": 1,
  "title": "update test",
  "body": "update hello",
  "userId": 1
}
```

### Mã trạng thái trả về

```text
200 OK
```

---

## Kịch Bản Kiểm Thử Lần 3

### Tên Kịch Bản

Kiểm thử tạo mới bài viết

### Mục Đích

Kiểm tra khả năng thêm dữ liệu bằng phương thức POST.

### Phương Thức HTTP

```text
POST
```

### URL

```text
https://jsonplaceholder.typicode.com/posts
```

### Dữ Liệu Gửi Đi

```json
{
  "title": "postman",
  "body": "hello",
  "userId": 1
}
```

### Kết Quả Mong Đợi

Tạo mới bài viết thành công và trả về ID mới.

### Kết Quả Thực Tế

API trả về dữ liệu vừa được tạo cùng ID mới.

### Trạng Thái

✅ Thành công

### Kết quả sau khi kiểm thử

<img width="1920" height="1020" alt="Screenshot 2026-06-17 080024" src="https://github.com/user-attachments/assets/4f1ebd95-8988-45a7-b142-fee9c385fa02" />


### Kết quả kiểm thử chi tiết

```json
{
  "title": "postman",
  "body": "hello",
  "userId": 1,
  "id": 101
}
```

### Mã trạng thái trả về

```text
201 Created
```

---

## Kịch Bản Kiểm Thử Lần 4

### Tên Kịch Bản

Kiểm thử truy cập tài nguyên không tồn tại

### Mục Đích

Kiểm tra khả năng xử lý lỗi khi truy cập dữ liệu không tồn tại.

### Phương Thức HTTP

```text
GET
```

### URL

```text
https://jsonplaceholder.typicode.com/posts/9999
```

### Tham Số

Không có

### Kết Quả Mong Đợi

Hệ thống trả về lỗi tài nguyên không tồn tại.

### Kết Quả Thực Tế

API trả về lỗi 404 Not Found.

### Trạng Thái

❌ Không thành công

### Kết quả sau khi kiểm thử

<img width="1920" height="1020" alt="Screenshot 2026-06-17 080153" src="https://github.com/user-attachments/assets/19c2359d-5605-41c5-946c-4682d1e5ef03" />


### Kết quả kiểm thử chi tiết

```json
{}
```

### Mã trạng thái trả về

```text
404 Not Found
```

---

## Kịch Bản Kiểm Thử Lần 5

### Tên Kịch Bản

Kiểm thử lấy chi tiết bài viết theo ID

### Mục Đích

Kiểm tra khả năng truy xuất dữ liệu theo ID cụ thể.

### Phương Thức HTTP

```text
GET
```

### URL

```text
https://jsonplaceholder.typicode.com/posts/1
```

### Tham Số

```text
id = 1
```

### Kết Quả Mong Đợi

Trả về thông tin bài viết có ID = 1.

### Kết Quả Thực Tế

API trả về đúng dữ liệu của bài viết số 1.

### Trạng Thái

✅ Thành công

### Kết quả sau khi kiểm thử

<img width="1920" height="1020" alt="Screenshot 2026-06-17 080207" src="https://github.com/user-attachments/assets/22635534-8f6f-47ec-b14b-5e711b5af422" />


### Kết quả kiểm thử chi tiết

```json
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit suscipit recusandae consequuntur expedita et cum reprehenderit molestiae ut ut quas totam nostrum rerum est autem sunt rem eveniet architecto"
}
```

### Mã trạng thái trả về

```text
200 OK
```

---

# 5. Kết Quả Kiểm Thử

| Nội dung                  | Kết quả |
| ------------------------- | ------- |
| Tổng số kịch bản kiểm thử | 5       |
| Số lần thành công         | 4       |
| Số lần thất bại           | 1       |
| Tỷ lệ thành công          | 80%     |

---

# 6. Phát Hiện Lỗi

### ID Lỗi

```text
404 Not Found
```

### Mô Tả Lỗi

Người dùng gửi yêu cầu tới tài nguyên không tồn tại:

```text
https://jsonplaceholder.typicode.com/posts/9999
```

Máy chủ không tìm thấy dữ liệu tương ứng nên trả về mã lỗi 404.

### Mức Độ Ảnh Hưởng

Thấp

### Ghi Chú / Đề Xuất

* Kiểm tra sự tồn tại của tài nguyên trước khi gửi yêu cầu.
* Xây dựng cơ chế xử lý ngoại lệ khi nhận mã lỗi 404.
* Hiển thị thông báo phù hợp cho người dùng khi dữ liệu không tồn tại.

---

# 7. Kết Luận

Việc kiểm thử trên Postman cho thấy API JSONPlaceholder hoạt động ổn định với các phương thức GET, POST và PUT. Các phản hồi từ máy chủ đúng với mong đợi, thời gian phản hồi nhanh và dữ liệu trả về đúng định dạng JSON. Hệ thống cũng xử lý chính xác các trường hợp lỗi khi truy cập tài nguyên không tồn tại bằng mã trạng thái **404 Not Found**. Tổng tỷ lệ thành công đạt **80%**.
