# Smart-Farm – Hệ thống trang trại thông minh

## 1. Mô tả dự án

Smart-Farm là hệ thống IoT hỗ trợ trang trại Lan theo dõi nhiệt độ, độ ẩm đất và tự động tưới cây khi cần. **Mục tiêu là giúp người nông dân chăm sóc cây thuận tiện và tiết kiệm nước.**

## 2. Phân tích hệ thống

Input (Đầu vào): Dữ liệu nhiệt độ, độ ẩm đất từ cảm biến.

Process (Xử lý): Bộ điều khiển nhận dữ liệu, so sánh với ngưỡng đã cài đặt và xác định có cần tưới hay không.

Output (Đầu ra): Điều khiển máy bơm và ghi lại trạng thái hoạt động.

SoC (Phân tách trách nhiệm) giúp chia hệ thống thành các phần riêng như đọc cảm biến, xử lý dữ liệu và điều khiển máy bơm.

## 3. Hướng dẫn cài đặt

1. Kết nối cảm biến với bộ điều khiển.
2. Kết nối máy bơm qua mạch điều khiển phù hợp.
3. Cài đặt ngưỡng nhiệt độ và độ ẩm theo loại cây.
4. Khởi động và kiểm tra dữ liệu trước khi bật chế độ tự động.

## 4. Tính năng

- [x] Theo dõi nhiệt độ và độ ẩm đất.
- [x] Xử lý dữ liệu cảm biến.
- [x] Điều khiển máy bơm tưới cây.
- [x] Ghi nhật ký hoạt động.

## 5. Bảng thông số

| Thiết bị | Chức năng |
|---|---|
| Cảm biến nhiệt độ | Đo nhiệt độ không khí |
| Cảm biến độ ẩm | Đo độ ẩm đất |
| Bộ điều khiển IoT | Xử lý dữ liệu và ra quyết định |
| Máy bơm | Cung cấp nước cho cây |

## Chu kỳ Fetch–Decode–Execute

> Fetch (Lấy lệnh): CPU lấy lệnh từ bộ nhớ.
>
> Decode (Giải mã): CPU giải mã lệnh để xác định công việc cần làm.
>
> Execute (Thực thi): CPU thực hiện lệnh. Chương trình điều khiển gửi tín hiệu bật máy bơm khi đủ điều kiện tưới.

## Mô hình kim tự tháp DIKW

```text
             WISDOM
        Quyết định tưới an toàn
              --------
           KNOWLEDGE
       Nhận biết đất đang khô
             ------
          INFORMATION
      So sánh số đo với ngưỡng
    ---------------
              DATA
       Nhiệt độ, độ ẩm đất
```
