# My-CV — Portfolio Nguyễn Việt Cường

Trang CV/portfolio cá nhân giới thiệu Nguyễn Việt Cường, các kỹ năng Frontend và một số dự án đã thực hiện. Giao diện được thiết kế responsive, phù hợp với điện thoại, máy tính bảng và máy tính.

## Chức năng

- Giới thiệu cá nhân và định hướng Frontend Developer.
- Hiển thị các kỹ năng: HTML5, CSS3, JavaScript, responsive design, Git/GitHub và Figma.
- Trưng bày bốn dự án kèm hình ảnh, mô tả và liên kết xem dự án.
- Điều hướng đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Bố cục responsive, sử dụng Flexbox và CSS Grid.

## Công nghệ

- HTML5
- CSS3 (Flexbox, CSS Grid, custom properties và media queries)
- JavaScript được liệt kê trong kỹ năng và dự án; trang portfolio hiện tại không cần bước build.
- Nginx (tùy chọn, dùng để chạy bằng Docker)

## Yêu cầu môi trường

Để xem trang, chỉ cần trình duyệt web hiện đại. Dự án là trang tĩnh nên không yêu cầu cài Node.js, npm, cơ sở dữ liệu hay biên dịch mã nguồn.

Tùy cách chạy, bạn có thể cần thêm:

- **Máy chủ cục bộ:** Python 3 (không bắt buộc nếu mở trực tiếp tệp HTML).
- **Docker:** Docker Engine hoặc Docker Desktop đang hoạt động.
- **Chỉnh sửa mã nguồn:** một trình soạn thảo văn bản bất kỳ.

## Cài đặt

### Windows

Mở PowerShell và chuyển đến thư mục dự án:

```powershell
cd "D:\Học trên lớp\Lesson07\My-CV"
```

### macOS và Linux

Mở Terminal và chuyển đến thư mục dự án (thay đường dẫn bên dưới bằng vị trí bạn đã lưu dự án):

```bash
cd "/đường/dẫn/đến/My-CV"
```

Không cần cài đặt thư viện. Nếu bạn nhận được mã nguồn dưới dạng tệp nén, hãy giải nén trước khi thực hiện các bước tiếp theo.

## Cấu hình

Dự án hiện không sử dụng tệp cấu hình, biến môi trường hay thông tin bí mật.

- Sửa nội dung, thông tin liên hệ và liên kết dự án trong `index.html`.
- Sửa màu sắc, bố cục và kiểu chữ trong `assets/css/styles.css`.
- Thay ảnh đại diện hoặc ảnh dự án trong `assets/img/`; giữ nguyên tên tệp hoặc cập nhật đường dẫn tương ứng trong `index.html`.

## Chạy thử

### Mở trực tiếp

Mở tệp `index.html` bằng trình duyệt. Cách này không cần cài thêm công cụ; để có trải nghiệm ổn định hơn, bạn có thể dùng máy chủ cục bộ như hướng dẫn bên dưới.

### Windows

Trong PowerShell, tại thư mục dự án, chạy:

```powershell
py -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

Nếu lệnh `py` không có trên máy, cài Python 3 hoặc mở trực tiếp `index.html`.

### macOS và Linux

Trong Terminal, tại thư mục dự án, chạy:

```bash
python3 -m http.server 8000
```

Mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

### Docker

Đảm bảo Docker đã khởi động, sau đó chạy lệnh tại thư mục dự án. Lần đầu chạy, Docker sẽ tải image Nginx nếu máy chưa có image này. Container phục vụ các tệp dự án trên cổng `8080`; nhấn `Ctrl+C` để dừng.

**Windows (PowerShell):**

```powershell
$projectPath = (Get-Location).Path
docker run --rm --name my-cv -p 8080:80 --mount "type=bind,source=$projectPath,target=/usr/share/nginx/html,readonly" nginx:alpine
```

**macOS/Linux (Terminal):**

```bash
docker run --rm --name my-cv -p 8080:80 --mount "type=bind,source=$(pwd),target=/usr/share/nginx/html,readonly" nginx:alpine
```

Sau khi container khởi động, mở <http://localhost:8080>. Nếu cổng `8080` đang được sử dụng, đổi phần `-p 8080:80` thành một cổng khác, ví dụ `-p 8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Thông tin liên hệ

- **Tác giả:** Nguyễn Việt Cường
- **Email:** [cuongnguyen259208@gmail.com](mailto:cuongnguyen259208@gmail.com)
- **GitHub:** [cuongnguyen259208-sudo](https://github.com/cuongnguyen259208-sudo)
