# APIS
# Giới thiệu về Postman

## Postman là gì?
Postman là một công cụ mạnh mẽ và phổ biến dành cho việc phát triển, kiểm thử, và quản lý các API. Với Postman, người dùng có thể gửi các yêu cầu HTTP, xem và kiểm tra các phản hồi, tự động hóa các kịch bản kiểm thử và hợp tác trong phát triển API.

## Các tính năng chính của Postman

- **Gửi yêu cầu HTTP**: Hỗ trợ đầy đủ các loại yêu cầu HTTP như GET, POST, PUT, DELETE, PATCH, OPTIONS.
- **Quản lý yêu cầu và bộ sưu tập**: Người dùng có thể tạo và quản lý các yêu cầu, tổ chức chúng thành các bộ sưu tập để dễ dàng kiểm thử.
- **Biến và môi trường**: Hỗ trợ biến số và môi trường để tái sử dụng các yêu cầu với dữ liệu động.
- **Kiểm thử tự động**: Hỗ trợ viết các kịch bản kiểm thử bằng JavaScript để tự động hóa quá trình kiểm thử.
- **Chia sẻ và hợp tác**: Hỗ trợ chia sẻ các bộ sưu tập và tài liệu API với nhóm phát triển.
- **Tích hợp và mở rộng**: Tích hợp với nhiều công cụ CI/CD và mở rộng tính năng thông qua các plugin.

# Báo cáo kiểm thử Dog API

## Mục tiêu kiểm thử
- Mục tiêu: Đảm bảo các chức năng chính của Dog API hoạt động chính xác và hiệu quả.
- Phạm vi: Kiểm thử các endpoint chính như /breeds, /breeds/{id}, /random, và /search.

## Kết quả kiểm thử

### 1. GET /breeds
- **Mã trạng thái**: 200 OK
- **Nội dung phản hồi**: Danh sách các giống chó.
- **Kết quả**: Thành công

### 2. GET /breeds/{id} (ID hợp lệ)
- **Mã trạng thái**: 200 OK
- **Nội dung phản hồi**: Thông tin chi tiết về giống chó có ID = 68f47c5a-5115-47cd-9849-e45d3c378f12.
- **Kết quả**: Thành công

### 3. GET /breeds/{id} (ID không hợp lệ)
- **Mã trạng thái**: 404 Not Found
- **Nội dung phản hồi**: Lỗi "Not Found".
- **Kết quả**: Thành công

 **Kết quả**: Thành công

### 4. GET /search?q={query} (có kết quả)
- **Mã trạng thái**: 200 OK
- **Nội dung phản hồi**: Danh sách các giống chó phù hợp với từ khóa "breeds".
- **Kết quả**: Thành công

### 6. GET /search?q={query} (không có kết quả)
- **Mã trạng thái**: 404 Not Found
- **Nội dung phản hồi**: Lỗi "Not Found".
- **Kết quả**: Thành công

## Khuyến nghị
- API hoạt động ổn định và phản hồi chính xác với các yêu cầu.
- Cần duy trì kiểm thử định kỳ để đảm bảo API luôn hoạt động đúng và bảo mật.
