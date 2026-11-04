# 🌐 PORTFOLIO CV CÁ NHÂN - BÙI LÝ HẢI

> **Dự án:** Trang web Portfolio & CV cá nhân trực tuyến (Bài kiểm tra KT A2.1)  
> **Tác giả:** Bùi Lý Hải  
> **Vai trò:** Frontend Developer / Web Developer  

---

## 📌 Bảng mục lục
1. [Giới thiệu & Mô tả dự án](#-1-giới-thiệu--mô-tả-dự-án)
2. [Tính năng nổi bật](#-2-tính-năng-nổi-bật)
3. [Công nghệ sử dụng](#-3-công-nghệ-sử-dụng)
4. [Cấu trúc thư mục](#-4-cấu-trúc-thư-mục)
5. [Yêu cầu môi trường](#-5-yêu-cầu-môi-trường)
6. [Cài đặt dự án](#-6-cài-đặt-dự-án)
7. [Cấu hình & Tùy biến](#-7-cấu-hình--tùy-biến)
8. [Hướng dẫn chạy thử](#-8-hướng-dẫn-chạy-thử)
   - [Windows](#81-trên-hệ-điều-hành-windows)
   - [macOS](#82-trên-hệ-điều-hành-macos)
   - [Linux](#83-trên-hệ-điều-hành-linux)
   - [Docker](#84-chạy-bằng-docker--docker-compose)
9. [Thông tin liên hệ](#-9-thông-tin-liên-hệ)
10. [Bản quyền & Giấy phép](#-10-bản-quyền--giấy-phép)

---

## 📖 1. Giới thiệu & Mô tả dự án

Trang web **Portfolio CV** của **Bùi Lý Hải** là một ứng dụng web tĩnh giới thiệu hồ sơ năng lực cá nhân, các kỹ năng chuyên môn, dự án tiêu biểu và thông tin liên hệ của một lập trình viên Frontend.

Dự án được xây dựng với các tiêu chí cốt lõi:
- **Mobile-First Design:** Bố cục và trải nghiệm người dùng được tối ưu hóa trước tiên cho màn hình điện thoại thông minh, sau đó mở rộng linh hoạt cho máy tính bảng (Tablet) và máy tính để bàn (Desktop).
- **Ngữ nghĩa chuẩn HTML5 (Semantic HTML5):** Cấu trúc tài liệu rõ ràng, hỗ trợ tối đa cho các công cụ tìm kiếm (SEO) và trình đọc màn hình dành cho người khiếm thị (Accessibility / a11y).
- **CSS3 hiện đại:** Quản lý giao diện thông qua hệ thống biến tập trung (Design Tokens / CSS Custom Properties), kết hợp bố cục linh hoạt Flexbox và CSS Grid.
- **Tối ưu tốc độ tải:** Thuần HTML/CSS, không phụ thuộc vào các thư viện JavaScript cồng kềnh, tải trang tức thì và hoạt động mượt mà trên mọi nền tảng.

---

## ✨ 2. Tính năng nổi bật

- 🧭 **Header & Điều hướng mượt mà:** Thanh menu cố định, hỗ trợ cuộn mượt (Smooth Scrolling) trực tiếp đến từng phân đoạn nội dung trên trang.
- 👤 **Giới thiệu bản thân (Hero / About):** Trình bày ngắn gọn về bản thân, định hướng nghề nghiệp, ảnh đại diện và các nút thao tác nhanh (Call-to-Action).
- 💡 **Danh mục kỹ năng (Skill Chips):** Trình bày kỹ năng chuyên môn (HTML5, CSS3, Flexbox/Grid, Responsive, Git, Photoshop, Python,...) dưới dạng các chip trực quan, đẹp mắt.
- 🗂️ **Dự án tiêu biểu (Project Cards Grid):** Hiển thị danh sách dự án bằng hệ thống lưới (CSS Grid) tự co giãn, mỗi dự án gồm ảnh đại diện, tóm tắt, tag công nghệ và liên kết chi tiết.
- 📬 **Kênh liên hệ (Contact Section):** Tích hợp thông tin liên hệ đa kênh: Email (kèm liên kết `mailto:`), Mạng xã hội (Instagram) và Số điện thoại liên lạc.
- 📱 **Tương thích mọi thiết bị (Responsive):** Tự động thích ứng trên mọi độ phân giải màn hình từ mobile (~360px), tablet (768px+) đến desktop (1280px+).

---

## 🛠️ 3. Công nghệ sử dụng

| Công nghệ | Vai trò / Mục đích |
| :--- | :--- |
| **HTML5** | Xây dựng cấu trúc tài liệu ngữ nghĩa (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<footer>`) |
| **CSS3** | Tạo kiểu giao diện, Responsive Web Design, hiệu ứng chuyển động, bố cục Flexbox & CSS Grid |
| **CSS Custom Properties** | Hệ thống biến Design Tokens (`:root`) đồng bộ màu sắc, typography, khoảng cách |
| **Nginx / Web Servers** | Máy chủ phục vụ web tĩnh khi chạy trên môi trường cục bộ hoặc Docker |
| **Docker** | Đóng gói và triển khai ứng dụng trong môi trường container hóa đồng nhất |

---

## 📂 4. Cấu trúc thư mục

```plaintext
KT A2.1/
├── assets/
│   ├── css/
│   │   └── styles.css          # File stylesheet chính (Design tokens, Mobile-first, Grid, Flexbox)
│   └── img/                    # Thư mục hình ảnh đại diện, ảnh dự án
│       ├── ảnh.jpg
│       ├── ảnh2.jpg
│       ├── ảnh3.jpg
│       ├── gs25.jpg
│       ├── thuysi.webp
│       └── vinhhalong.jpg
├── index.html                  # File giao diện HTML chính
├── README.md                   # Tài liệu hướng dẫn sử dụng dự án
├── BAOCAO-A2.1.docx            # Báo cáo học tập / kiểm tra
└── BAOCAO-A2.1.zip             # Bản nén tài liệu dự án
```

---

## 💻 5. Yêu cầu môi trường

Để xem hoặc phát triển dự án, máy tính cần đáp ứng:

### 1. Yêu cầu tối thiểu (để xem trang web):
- Mọi hệ điều hành: **Windows 10/11**, **macOS 10.15+**, **Linux (Ubuntu, Debian, Fedora, Arch,...)**.
- Bất kỳ trình duyệt web hiện đại nào: Google Chrome, Microsoft Edge, Mozilla Firefox, Apple Safari, Opera, Brave,...

### 2. Yêu cầu phát triển / chạy thử cục bộ (tùy chọn):
- **Công cụ dòng lệnh / Máy chủ web tĩnh:**
  - Python 3.x (thường tích hợp sẵn trên macOS/Linux hoặc cài trên Windows)
  - HOẶC Node.js (phiên bản 16 trở lên)
  - HOẶC Extension **Live Server** trong Visual Studio Code.
- **Docker:** Cài đặt Docker Desktop hoặc Docker Engine (nếu muốn chạy thử dạng container).

---

## 📥 6. Cài đặt dự án

### Cách 1: Tải mã nguồn hoặc giải nén
1. Sao chép hoặc giải nén thư mục `KT A2.1` vào thư mục làm việc của bạn.
2. Đảm bảo giữ nguyên cấu trúc thư mục con `assets/css/` và `assets/img/`.

### Cách 2: Clone qua Git (nếu dự án được lưu trên Git)
```bash
git clone <URL_REPOSITORY_CUA_BAN>
cd "KT A2.1"
```

---

## ⚙️ 7. Cấu hình & Tùy biến

### 7.1. Chỉnh sửa nội dung cá nhân (`index.html`)
- **Thông tin giới thiệu:** Mở file `index.html` và chỉnh sửa các đoạn văn bản trong thẻ `<section id="about">`.
- **Kỹ năng:** Thêm hoặc bớt các thẻ `<li class="skill-chip">Tên kỹ năng</li>` trong `<section id="skills">`.
- **Dự án:** Thay đổi thông tin dự án, ảnh minh họa trong `<section id="projects">`.
- **Thông tin liên hệ:** Cập nhật email, số điện thoại, mạng xã hội trong `<section id="contact">`.

### 7.2. Tùy chỉnh màu sắc & giao diện (`assets/css/styles.css`)
Bạn có thể dễ dàng thay đổi màu sắc chủ đạo, font chữ hoặc khoảng cách tại khối `:root` ở đầu file `assets/css/styles.css`:

```css
:root {
  /* Bảng màu chính */
  --color-primary: #2563eb;      /* Màu xanh thương hiệu */
  --color-primary-dark: #1d4ed8; /* Màu xanh đậm khi hover */
  --color-accent: #7c3aed;       /* Màu tím tạo điểm nhấn */
  --color-text: #1e293b;         /* Màu chữ chính */
  --color-text-soft: #64748b;    /* Màu chữ phụ */
  --color-bg: #09b2ea;           /* Màu nền trang */
  --color-surface: #f8fafc;      /* Màu nền khối nội dung */
  --color-border: #000204;       /* Màu đường viền */
  
  /* Font chữ & Bố cục */
  --font-base: system-ui, -apple-system, sans-serif;
  --container-max: 1200px;
  --radius: 12px;
}
```

---

## 🚀 8. Hướng dẫn chạy thử

Dự án là trang web tĩnh (Static Web), bạn có thể chạy bằng nhiều cách khác nhau tùy theo hệ điều hành hoặc qua Docker.

---

### 8.1. Trên hệ điều hành Windows

#### Phương án 1: Mở trực tiếp bằng trình duyệt (Nhanh nhất)
1. Mở thư mục dự án trong **File Explorer**.
2. Nhấp đúp chuột trái vào file `index.html` (hoặc chuột phải chọn **Open with** > **Google Chrome** / **Microsoft Edge**).

#### Phương án 2: Sử dụng Python HTTP Server
1. Mở cửa sổ **PowerShell** hoặc **Command Prompt** tại thư mục dự án:
   ```powershell
   cd "E:\Bùi Lý Hải\KT A2.1"
   ```
2. Khởi chạy máy chủ:
   ```powershell
   python -m http.server 8000
   ```
3. Mở trình duyệt và truy cập: [http://localhost:8000](http://localhost:8000)

#### Phương án 3: Sử dụng Node.js (`serve` hoặc `http-server`)
```powershell
# Chạy tức thì không cần cài đặt vĩnh viễn
npx serve .
# Hoặc
npx http-server -p 8000
```
Truy cập địa chỉ hiển thị trên màn hình terminal (thường là `http://localhost:3000` hoặc `http://localhost:8000`).

#### Phương án 4: Dùng Visual Studio Code
1. Mở thư mục `KT A2.1` bằng VS Code.
2. Cài extension **Live Server** (của Ritwick Dey).
3. Chuột phải vào file `index.html` và chọn **Open with Live Server** (hoặc bấm nút *Go Live* ở góc dưới cùng bên phải).

---

### 8.2. Trên hệ điều hành macOS

#### Phương án 1: Mở trực tiếp bằng lệnh Terminal hoặc Finder
```bash
# Mở bằng trình duyệt mặc định
open index.html

# Hoặc chỉ định mở bằng Safari / Google Chrome
open -a "Safari" index.html
open -a "Google Chrome" index.html
```

#### Phương án 2: Sử dụng Python 3 tích hợp sẵn
1. Mở ứng dụng **Terminal**.
2. Di chuyển đến thư mục dự án:
   ```bash
   cd "/đường_dẫn_tới/KT A2.1"
   ```
3. Chạy lệnh:
   ```bash
   python3 -m http.server 8080
   ```
4. Mở trình duyệt và truy cập: [http://localhost:8080](http://localhost:8080)

#### Phương án 3: Sử dụng Node.js
```bash
npx serve .
```

---

### 8.3. Trên hệ điều hành Linux

#### Phương án 1: Mở trực tiếp từ Terminal
```bash
# Sử dụng xdg-open để mở bằng trình duyệt mặc định của hệ thống
xdg-open index.html
```

#### Phương án 2: Sử dụng Python 3 HTTP Server
1. Mở cửa sổ Terminal tại thư mục dự án:
   ```bash
   cd "/path/to/KT A2.1"
   ```
2. Khởi chạy server:
   ```bash
   python3 -m http.server 8080
   ```
3. Truy cập trình duyệt tại địa chỉ: [http://localhost:8080](http://localhost:8080)

#### Phương án 3: Sử dụng máy chủ Nginx hoặc Apache có sẵn trên Linux
Sao chép mã nguồn vào thư mục phục vụ web của Nginx/Apache:
```bash
sudo cp -r . /var/www/html/portfolio
sudo systemctl restart nginx
```
Truy cập: [http://localhost/portfolio](http://localhost/portfolio)

---

### 8.4. Chạy bằng Docker & Docker Compose

Docker giúp chạy trang web trong môi trường web server Nginx Alpine nhẹ, chuẩn hóa và bảo mật mà không cần cài đặt bất kỳ công cụ lập trình nào trên máy chủ.

#### Cách 1: Chạy ngay lập tức bằng 1 lệnh Docker (Không cần tạo file)

- **Trên Windows (PowerShell):**
  ```powershell
  docker run -d --name cv-portfolio -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
  ```

- **Trên macOS / Linux:**
  ```bash
  docker run -d --name cv-portfolio -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
  ```

- **Kiểm tra kết quả:** Mở trình duyệt truy cập: [http://localhost:8080](http://localhost:8080)
- **Dừng và gỡ container:**
  ```bash
  docker stop cv-portfolio && docker rm cv-portfolio
  ```

---

#### Cách 2: Sử dụng Dockerfile (Đóng gói thành Image hoàn chỉnh)

1. Tạo file mang tên `Dockerfile` tại thư mục gốc của dự án với nội dung:
   ```dockerfile
   # Sử dụng Nginx Alpine siêu nhẹ (~20MB)
   FROM nginx:alpine

   # Sao chép toàn bộ mã nguồn vào thư mục phục vụ của Nginx
   COPY . /usr/share/nginx/html

   # Mở cổng 80
   EXPOSE 80

   # Lệnh chạy mặc định
   CMD ["nginx", "-g", "daemon off;"]
   ```

2. Tạo file `.dockerignore` để tránh sao chép các tệp tài liệu thừa:
   ```plaintext
   .git
   *.docx
   *.zip
   ```

3. Build Docker Image:
   ```bash
   docker build -t builyhai-portfolio:latest .
   ```

4. Khởi chạy Container:
   ```bash
   docker run -d -p 8080:80 --name my-portfolio builyhai-portfolio:latest
   ```

5. Truy cập tại: [http://localhost:8080](http://localhost:8080)

---

#### Cách 3: Sử dụng Docker Compose

1. Tạo file `docker-compose.yml` tại thư mục gốc dự án:
   ```yaml
   version: '3.8'

   services:
     portfolio:
       image: nginx:alpine
       container_name: cv_portfolio_app
       ports:
         - "8080:80"
       volumes:
         - .:/usr/share/nginx/html:ro
       restart: always
   ```

2. Khởi chạy:
   ```bash
   docker compose up -d
   ```

3. Dừng ứng dụng:
   ```bash
   docker compose down
   ```

---

## 📞 9. Thông tin liên hệ

Mọi đóng góp ý kiến hoặc liên hệ công việc, vui lòng kết nối qua các kênh dưới đây:

- **Họ và tên:** Bùi Lý Hải
- **Chuyên môn:** Frontend Developer / Web Developer
- **Email:** [builyhai0208@gmail.com](mailto:builyhai0208@gmail.com)
- **Số điện thoại:** [0981 867 208](tel:0981867208)
- **Instagram:** [@linie.haeir_](https://instagram.com/linie.haeir_)
- **Địa điểm:** Việt Nam

---

## 📜 10. Bản quyền & Giấy phép

- Dự án được xây dựng phục vụ cho mục đích học tập và hồ sơ năng lực cá nhân.
- Bản quyền thuộc về © 2026 **Bùi Lý Hải**. Mọi quyền được bảo lưu.
- Được cấp phép tự do tham khảo và phát triển cho mục đích giáo dục phi thương mại.

