# Báo cáo kiểm thử

- **Dự án:** CV Portfolio - Nguyễn Văn Hoàng Anh
- **Ngày kiểm thử:** 27/10/2026
- **Phạm vi:** `index.html`, `assets/css/styles.css` và tài nguyên trong `assets/`.
- **Môi trường kiểm tra giao diện:** Microsoft Edge, desktop 1440 × 1000 và mobile 390 × 844.
- **Minh chứng:** Ảnh chụp được lưu trong [`docs/screenshots/`](./screenshots/).

## 1. Tính đúng đắn

**Kết quả: Đạt trong phạm vi kiểm tra**

- Trang mở được trong trình duyệt và hiển thị các mục Giới thiệu, Kỹ năng, Dự án, Liên hệ.
- Các liên kết điều hướng nội bộ trỏ đến những mục tương ứng có trong trang.
- Ảnh đại diện và hình minh họa dự án tải thành công.
- **Hạn chế:** Các liên kết “Xem chi tiết” hiện trỏ đến `#`, chưa mở trang dự án thật.

**Minh chứng:** [Ảnh giao diện desktop](./screenshots/01-desktop.png), [ảnh giao diện mobile](./screenshots/02-mobile.png).

## 2. UI/UX

**Kết quả: Đạt một phần**

- Đã kiểm tra giao diện ở kích thước desktop và mobile.
- CSS có bố cục mobile-first, breakpoint tại 768px và 1280px, trạng thái focus bằng bàn phím và hỗ trợ `prefers-reduced-motion`.
- Ảnh có văn bản thay thế; điều hướng có nhãn hỗ trợ trình đọc màn hình.
- **Điểm cần cải thiện:** Ảnh mobile cho thấy một số nội dung dài sát mép và có dấu hiệu bị cắt. Cần điều chỉnh, kiểm tra lại trên các thiết bị thực tế.
- Chưa kiểm tra tương phản màu bằng công cụ, trình đọc màn hình hoặc thử nghiệm người dùng.

**Minh chứng:** [Ảnh desktop 1440 × 1000](./screenshots/01-desktop.png), [ảnh mobile 390 × 844](./screenshots/02-mobile.png).

## 3. Khả năng vận hành - xử lý lỗi

**Kết quả: Đạt với luồng hiển thị cơ bản; chưa kiểm tra tình huống lỗi**

- Đã mở trang tĩnh trong Microsoft Edge và xác nhận nội dung cùng các ảnh hiện có được tải.
- Website không cần máy chủ ứng dụng hoặc cơ sở dữ liệu để hiển thị nội dung.
- Chưa mô phỏng lỗi mất mạng, thiếu tệp ảnh/CSS hoặc truy cập đường dẫn không tồn tại. Website chưa có giao diện thông báo lỗi tùy chỉnh cho các trường hợp này.

**Minh chứng:** [Ảnh trang đang hiển thị](./screenshots/01-desktop.png).

## 4. Bảo mật

**Kết quả: Đã rà soát mã nguồn cơ bản; chưa kiểm thử bảo mật chuyên sâu**

- Website là trang tĩnh; trong phạm vi mã nguồn được rà soát, không thấy biểu mẫu nhập liệu, mã JavaScript ứng dụng, API, đăng nhập hoặc xử lý dữ liệu người dùng.
- Không có cơ sở dữ liệu hoặc thông tin xác thực cấu hình trong trang.
- Chưa đánh giá bảo mật máy chủ, HTTPS, DNS hoặc dịch vụ bên thứ ba; chưa chạy công cụ quét lỗ hổng.

**Minh chứng:** Rà soát mã nguồn `index.html` và `assets/css/styles.css`. Ảnh giao diện không thay thế cho kiểm thử bảo mật.

## 5. Chất lượng mã nguồn

**Kết quả: Đã rà soát cấu trúc; chưa chạy bộ kiểm tra tự động**

- HTML dùng các phần tử ngữ nghĩa như `header`, `nav`, `main`, `section` và `footer`.
- CSS được tách khỏi HTML; bố cục sử dụng Flexbox, Grid và media query.
- Các ảnh có `alt`, điều hướng có nhãn hỗ trợ truy cập.
- Các liên kết dự án dạng `href="#"` cần được cập nhật khi có địa chỉ đích.
- Chưa chạy HTML/CSS validator, accessibility audit, linter hoặc kiểm thử tự động; chưa kết luận mã nguồn không có lỗi.

**Minh chứng:** Đối chiếu `index.html` và `assets/css/styles.css`; chưa có ảnh kết quả validator hoặc linter.

## 6. Khả năng triển khai

**Kết quả: Phù hợp triển khai dạng website tĩnh; chưa xác nhận trên hosting**

- Dự án không có bước build hoặc phụ thuộc npm; có thể được phục vụ bằng web server tĩnh.
- CSS và ảnh được tham chiếu bằng đường dẫn tương đối.
- Đã mở trang từ tệp cục bộ; chưa triển khai lên hosting, GitHub Pages hoặc Docker để kiểm tra URL công khai, HTTPS và đường dẫn khi đặt trong thư mục con.

**Minh chứng:** [Ảnh trang chạy cục bộ](./screenshots/01-desktop.png). Ảnh này xác nhận trang hiển thị trong trình duyệt, không xác nhận đã triển khai lên hosting.

## Danh sách ảnh minh chứng

| Tệp | Nội dung |
|---|---|
| [`01-desktop.png`](./screenshots/01-desktop.png) | Giao diện tại viewport desktop 1440 × 1000 |
| [`02-mobile.png`](./screenshots/02-mobile.png) | Giao diện tại viewport mobile 390 × 844 |

Các ảnh được chụp từ website bằng Microsoft Edge. Đánh giá bảo mật và chất lượng mã nguồn dựa trên rà soát mã nguồn, không dựa riêng vào ảnh giao diện. Các mục ghi “chưa kiểm thử” cần được xác nhận bổ sung trước khi phát hành chính thức.
