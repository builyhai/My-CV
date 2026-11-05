# 📝 THÔNG TIN PHÁT HÀNH (RELEASE NOTE)

## 📌 Tổng quan dự án
- **Tên dự án:** Portfolio CV Cá Nhân - Bùi Lý Hải (KT A2.1)
- **Tác giả:** Bùi Lý Hải
- **Mục tiêu:** Trang web hồ sơ năng lực cá nhân, giới thiệu kỹ năng và dự án Frontend chuẩn Responsive Mobile-First.

---

## 🚀 Phiên bản: v1.0.0
- **Ngày phát hành:** 05/11/2026
- **Trạng thái:** Bản phát hành chính thức đầu tiên (Initial Production Release)

---

### ✨ 1. Chức năng mới (New Features)

#### 🧭 Giao diện & Điều hướng
- **Thanh Header & Navigation mượt mà:**
  - Tích hợp nhận diện thương hiệu cá nhân với logo ký hiệu và họ tên.
  - Menu điều hướng nhanh hỗ trợ cuộn mượt (*Smooth Scrolling*) đến từng khu vực: *Giới thiệu*, *Kỹ năng*, *Dự án*, *Liên hệ*.
- **Thiết kế Mobile-First & Responsive toàn diện:**
  - Tối ưu hóa hiển thị từ kích thước màn hình nhỏ nhất (~360px) trên di động.
  - Sử dụng Media Queries nâng cấp mượt mà lên màn hình máy tính bảng (768px+) và máy tính để bàn (1280px+).

#### 👤 Khối nội dung hồ sơ cá nhân
- **Phần Giới thiệu (Hero / About):**
  - Trình bày thông tin giới thiệu, định hướng nghề nghiệp và các nút kêu gọi hành động (*Call-to-Action*).
  - Tích hợp ảnh đại diện cá nhân bo góc, khung hiển thị đồng bộ.
- **Danh mục Kỹ năng (Skills):**
  - Trình bày các kỹ năng chuyên môn (HTML5, CSS3, Flexbox, Grid, Responsive, Git, Photoshop, Python,...) dưới dạng các thẻ chip (*Skill Chips*) trực quan, bo tròn thẩm mỹ.
- **Lưới Dự án tiêu biểu (Project Grid):**
  - Hiển thị danh mục dự án thông qua bố cục lưới linh hoạt *CSS Grid* tự động co giãn (`grid-template-columns`).
  - Mỗi thẻ dự án (*Card*) gồm ảnh minh họa, tiêu đề, tóm tắt nội dung, tag thể loại và liên kết xem chi tiết.
- **Khối Liên hệ (Contact):**
  - Tích hợp thông tin liên hệ đa kênh: Email (liên kết mở trình gửi mail `mailto:`), Mạng xã hội Instagram và Số điện thoại hotline.

#### 🛠️ Kỹ thuật & Cấu trúc nền tảng
- **Chuẩn ngữ nghĩa HTML5 & SEO / Accessibility:**
  - Sử dụng toàn bộ các thẻ ngữ nghĩa chuẩn (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<footer>`).
  - Cung cấp đầy đủ thuộc tính `lang="vi"`, meta tags, tiêu đề trang và văn bản thay thế `alt` cho hình ảnh hỗ trợ trình đọc màn hình.
- **Quản lý giao diện bằng Design Tokens (CSS Variables):**
  - Tập trung hóa màu sắc, kích thước font chữ, khoảng cách (*spacing*), độ bo góc (*border-radius*) và đổ bóng (*box-shadow*) tại `:root`.
- **Hỗ trợ đóng gói & Triển khai Container:**
  - Bổ sung cấu hình `Dockerfile`, `docker-compose.yml`, và `.dockerignore` chạy trên nền Nginx Alpine siêu nhẹ.
  - Cung cấp tài liệu hướng dẫn vận hành chi tiết trong `README.md` cho Windows, macOS, Linux và Docker.

---

### 🐛 2. Lỗi đã sửa (Bug Fixes)

Trong quá trình hoàn thiện và kiểm thử phiên bản v1.0, các lỗi sau đã được khắc phục triệt để:

- **Sửa lỗi cú pháp thẻ thương hiệu ở Header:**
  - *Hiện tượng:* Thẻ mở bị thiếu tên thẻ `< class="brand" href="#top">` làm ảnh hưởng đến cấu trúc DOM.
  - *Khắc phục:* Bổ sung chuẩn xác thẻ neo `<a class="brand" href="#top" aria-label="Về đầu trang">`.
- **Sửa lỗi thiếu thuộc tính và đóng thẻ `<img>` tại Card dự án GS25:**
  - *Hiện tượng:* Thẻ `<img>` của dự án Siêu thị GS25 bị khuyết thuộc tính mô tả và chưa đóng thẻ hợp lệ trước thẻ `<div class="card-body">`.
  - *Khắc phục:* Bổ sung đầy đủ thuộc tính `alt="Siêu thị GS25"`, thiết lập `width="600"`, `height="360"` và đóng thẻ chuẩn theo quy chuẩn HTML5.
- **Loại bỏ hiện tượng tràn viền ngang (Horizontal Overflow):**
  - *Khắc phục:* Thiết lập `box-sizing: border-box`, `max-width: 100%` cho toàn bộ hình ảnh và cấu hình `overflow-x: hidden` tại `body` đảm bảo không bị thanh cuộn ngang gây vỡ giao diện trên thiết bị di động.

---

### ⚠️ 3. Hạn chế còn tồn tại (Known Limitations)

Mặc dù phiên bản v1.0 đã đáp ứng đầy đủ yêu cầu của bài kiểm tra và hoạt động ổn định, dự án vẫn còn một số điểm giới hạn:

1. **Website tĩnh thuần HTML/CSS, chưa có kịch bản JavaScript:**
   - Chưa có tính năng chuyển đổi chế độ giao diện Sáng / Tối (*Light / Dark Mode*).
   - Menu điều hướng trên điện thoại chưa có nút thu gọn / mở rộng dạng Hamburger (*Off-canvas Menu*).
   - Chưa có bộ lọc (filter) hoặc tìm kiếm dự án động theo từ khóa/danh mục.
2. **Biểu mẫu liên hệ tĩnh:**
   - Khu vực liên hệ hiện chỉ cung cấp thông tin và liên kết `mailto:`, chưa có Form nhập trực tiếp (Name, Email, Message) gửi dữ liệu về máy chủ hoặc dịch vụ email tự động (như EmailJS hay Formspree).
3. **Liên kết dự án ở trạng thái chờ:**
   - Các nút "Xem chi tiết →" trên các thẻ dự án hiện tại đang trỏ tới `#` (placeholder), chưa liên kết đến các trang chi tiết bài viết (Case study) hoặc demo trực tiếp của từng sản phẩm.
4. **Quản lý dữ liệu thủ công:**
   - Mọi thay đổi về kỹ năng hoặc danh sách dự án đều phải chỉnh sửa trực tiếp trong mã nguồn `index.html`, chưa tích hợp hệ thống quản lý nội dung (Headless CMS hoặc file dữ liệu JSON độc lập).

---

### 🔮 4. Kế hoạch phát triển phiên bản tiếp theo (Roadmap v1.1)

- [ ] Bổ sung JavaScript cho hiệu ứng tương tác, hoạt ảnh cuộn trang (Scroll Animations / AOS).
- [ ] Thêm nút Toggle chuyển đổi Dark Mode / Light Mode.
- [ ] Tích hợp Form liên hệ tương tác gửi email tự động qua EmailJS.
- [ ] Xây dựng trang chi tiết riêng cho từng dự án tiêu biểu.
- [ ] Tách dữ liệu dự án và kỹ năng ra file `data.json` để dễ bảo trì và mở rộng.

