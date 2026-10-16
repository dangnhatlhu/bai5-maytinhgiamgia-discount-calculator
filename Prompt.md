# Máy tính giảm giá

## Prompt

Hãy viết một trang web Máy tính giảm giá bằng HTML và JavaScript. Người dùng nhập số tiền hóa đơn. Nếu hóa đơn lớn hơn 500.000đ thì được giảm 10%; nếu không thì không giảm. Hiển thị số tiền hóa đơn, số tiền giảm và số tiền cuối cùng phải trả. Toàn bộ mã JavaScript đặt trong file `index.html`, đồng thời ghi prompt và phần giải thích code bằng tiếng Việt trong file `Prompt.md`.

## Giải thích code

- **Ô nhập số tiền:** Trường `input` kiểu `number` cho phép người dùng nhập hóa đơn bằng đồng nguyên. Thuộc tính `min="0"` ngăn số âm và `step="1"` yêu cầu số nguyên thông qua giao diện.
- **Xử lý biểu mẫu:** Khi người dùng bấm **Tính tiền**, sự kiện `submit` được xử lý. `event.preventDefault()` ngăn trang tải lại.
- **Chuyển và kiểm tra dữ liệu:** `Number()` chuyển nội dung ô nhập thành số. `Number.isFinite()`, `Number.isInteger()` và điều kiện số âm giúp kiểm tra dữ liệu trước khi tính.
- **Tính giảm giá:** Biến `discountRate` nhận giá trị `0.1` khi hóa đơn **lớn hơn** 500.000đ; các trường hợp còn lại nhận `0`. Vì vậy, hóa đơn đúng 500.000đ không được giảm.
- **Tính tiền phải trả:** Tiền giảm bằng hóa đơn nhân với tỷ lệ giảm; tiền phải trả bằng hóa đơn trừ tiền giảm.
- **Định dạng và hiển thị:** Hàm `formatCurrency()` dùng `Intl.NumberFormat` để hiển thị số tiền theo định dạng tiền Việt Nam. Kết quả được trình bày bên dưới biểu mẫu.
