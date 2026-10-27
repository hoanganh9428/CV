# CV Portfolio - Nguyễn Văn Hoàng Anh

Website CV/portfolio cá nhân giới thiệu Nguyễn Văn Hoàng Anh, các kỹ năng, dự án tiêu biểu và thông tin liên hệ. Giao diện được xây dựng theo hướng responsive, có thể chạy trực tiếp trên trình duyệt hoặc phục vụ bằng web server tĩnh.

## Chức năng

- Giới thiệu cá nhân và định hướng Frontend Developer.
- Trình bày các kỹ năng như HTML, CSS, JavaScript, responsive design, Git/GitHub và Figma.
- Hiển thị các thẻ dự án mẫu: Landing Page, Todo List, Weather Dashboard và Blog cá nhân.
- Điều hướng nhanh đến phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp liên kết email và trang cá nhân.
- Tương thích với các kích thước màn hình khác nhau.

> Các dự án trên trang là nội dung giới thiệu mẫu. Một số liên kết “Xem chi tiết” hiện chưa trỏ đến trang dự án cụ thể.

## Công nghệ

- HTML5: cấu trúc nội dung và ngữ nghĩa trang.
- CSS3: giao diện, Flexbox, CSS Grid và responsive layout.
- SVG nhúng: hình minh họa mẫu cho các thẻ dự án.
- Nginx (tùy chọn): phục vụ website trong Docker.

Đây là website tĩnh, không có backend, cơ sở dữ liệu, bước biên dịch hay phụ thuộc npm.

## Cấu trúc dự án

```text
.
├── index.html
├── README.md
└── assets/
    ├── css/
    │   └── styles.css
    └── img/
        └── avatar.jpg
```

## Yêu cầu môi trường

### Chỉ xem website

- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Không cần cài Node.js hay chạy lệnh cài thư viện.

### Chạy bằng máy chủ cục bộ

Chọn một trong các cách sau:

- Python 3; hoặc
- Docker Desktop trên Windows/macOS, hay Docker Engine trên Linux.

## Cài đặt

Tải hoặc sao chép repository về máy, sau đó mở terminal tại thư mục dự án:

```bash
git clone https://github.com/hoanganh9428/CV.git
cd CV
```

Nếu đã có mã nguồn trên máy, chuyển terminal đến thư mục chứa `index.html` thay vì chạy lại lệnh clone. Không cần cài đặt thêm gói.

## Cấu hình và tùy chỉnh

Không có tệp cấu hình môi trường (`.env`) hoặc cấu hình máy chủ bắt buộc. Để cá nhân hóa website:

1. Chỉnh nội dung, thông tin liên hệ, tiêu đề và liên kết dự án trong `index.html`.
2. Thay ảnh `assets/img/avatar.jpg` bằng ảnh đại diện của bạn; nên giữ tên và đường dẫn này, hoặc cập nhật thuộc tính `src` trong `index.html`.
3. Chỉnh màu sắc, kiểu chữ và bố cục trong `assets/css/styles.css`.
4. Kiểm tra các liên kết dự án đang dùng `href="#"` và thay bằng địa chỉ phù hợp.

## Chạy thử

### Cách nhanh: mở trực tiếp

Mở `index.html` bằng trình duyệt. Cách này phù hợp để xem trang cơ bản; dùng máy chủ cục bộ nếu muốn trải nghiệm gần với môi trường triển khai hơn.

### Windows

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có nhưng đã cài Python, dùng:

```powershell
python -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Control+C`.

### Linux

Mở terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

Nếu Python chưa được cài đặt, có thể xem trực tiếp `index.html` hoặc dùng phương án Docker bên dưới.

### Docker (Windows, macOS và Linux)

Cài và khởi động Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux). Từ terminal tại thư mục dự án, chạy lệnh tương ứng:

**PowerShell (Windows):**

```powershell
docker run --rm --name cv-portfolio -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**Command Prompt (Windows):**

```cmd
docker run --rm --name cv-portfolio -p 8080:80 -v "%cd%:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS/Linux:**

```bash
docker run --rm --name cv-portfolio -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Lệnh trên tải image `nginx:alpine` nếu cần, gắn thư mục dự án ở chế độ chỉ đọc và phục vụ website tại <http://localhost:8080>. Giữ terminal mở khi sử dụng; nhấn `Ctrl+C` để dừng và xóa container.

Nếu cổng `8080` đã được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`, rồi truy cập cổng mới tương ứng.

## Kiểm tra

- Mở trang và xác nhận ảnh đại diện, CSS cùng các phần nội dung hiển thị đúng.
- Thử các liên kết điều hướng ở đầu trang và liên kết email/GitHub/TikTok trong phần Liên hệ.
- Thu nhỏ cửa sổ hoặc mở trên thiết bị di động để kiểm tra bố cục responsive.

## Thông tin liên hệ

- **Email:** [hoanganh942008@gmail.com](mailto:hoanganh942008@gmail.com)
- **GitHub:** [hoanganh9428](https://github.com/hoanganh9428)
- **TikTok:** [@hoagahn9428](https://www.tiktok.com/@hoagahn9428)