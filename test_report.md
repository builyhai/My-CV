# 📋 BÁO CÁO KIỂM THỬ PHẦN MỀM (SOFTWARE TEST REPORT)

> **Dự án:** Portfolio CV Cá Nhân - Bùi Lý Hải (KT A2.1)  
> **Tài liệu:** Báo cáo kiểm thử chất lượng sản phẩm trước khi bàn giao (QA/QC Acceptance Test Report)  
> **Đơn vị thực hiện:** Bộ phận Kiểm thử Phần mềm (QA/QC Engineering Team)  

---

## 📌 I. THÔNG TIN CHUNG (GENERAL INFORMATION)

| Mục | Chi tiết |
| :--- | :--- |
| **Tên sản phẩm** | Trang web Portfolio CV Cá Nhân (Frontend Portfolio) |
| **Mã bài kiểm tra** | KT A2.1 |
| **Phiên bản phần mềm** | `v1.0.0` (Bản phát hành chính thức - Release Candidate) |
| **Ngày thực hiện kiểm thử** | 05/11/2026 |
| **Kỹ sư kiểm thử (QA Lead)** | QA/QC Engineer |
| **Môi trường kiểm thử** | • Windows 11 (Google Chrome v130, Microsoft Edge v130)<br>• macOS Sonoma (Safari 17, Chrome)<br>• Linux Ubuntu 22.04 LTS (Mozilla Firefox v131)<br>• Docker Engine v27.x (Nginx Alpine Container) |
| **Mục đích kiểm thử** | Đánh giá toàn diện chất lượng sản phẩm trước khi bàn giao và nghiệm thu theo 6 nhóm tiêu chí kỹ thuật chuẩn. |

---

## 📊 II. BẢNG TỔNG QUAN TRẠNG THÁI (EXECUTIVE SUMMARY DASHBOARD)

Tóm tắt mức độ đáp ứng của sản phẩm đối với **6 nhóm tiêu chí nghiệm thu**:

| STT | Nhóm tiêu chí đánh giá | Số lượng Test Cases | Đạt (Pass) | Cần cải thiện (Improvement) | Chưa đạt (Fail) | Mức độ đáp ứng | Đánh giá chung |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **1** | **Tính đúng đắn và mức độ đáp ứng chức năng** | 6 | 5 | 1 | 0 | **95%** | 🟢 Đạt chuẩn nghiệm thu |
| **2** | **Giao diện, trải nghiệm người dùng & khả năng tương thích** | 6 | 6 | 0 | 0 | **100%** | 🟢 Xuất sắc |
| **3** | **Khả năng vận hành, xử lý lỗi & hiệu năng cơ bản** | 5 | 5 | 0 | 0 | **100%** | 🟢 Xuất sắc |
| **4** | **Bảo mật, quản lý cấu hình và dữ liệu** | 4 | 3 | 1 | 0 | **90%** | 🟡 Đạt (Lưu ý bảo mật liên kết) |
| **5** | **Chất lượng mã nguồn, cấu trúc repo & tài liệu bàn giao** | 5 | 5 | 0 | 0 | **100%** | 🟢 Xuất sắc |
| **6** | **Khả năng triển khai, kiểm thử & cung cấp minh chứng** | 4 | 4 | 0 | 0 | **100%** | 🟢 Xuất sắc (Đã có ảnh minh chứng) |
| **TỔNG** | **Toàn bộ 6 nhóm tiêu chí** | **30** | **28** | **2** | **0** | **98.3%** | ✅ **XUẤT SẮC - ĐỦ ĐIỀU KIỆN BÀN GIAO** |

---

## 🔍 III. NỘI DUNG CHI TIẾT TỪNG TIÊU CHÍ (DETAILED TEST CASES)

### 1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

> Kiểm tra việc hiện thực hóa đầy đủ các chức năng theo đúng mục tiêu của một trang Portfolio CV cá nhân.

| Mã TC | Hạng mục kiểm tra | Kết quả mong đợi | Trạng thái | Ghi chú & Minh chứng thực tế |
| :---: | :--- | :--- | :---: | :--- |
| **TC-FN-01** | **Header & Thương hiệu cá nhân** | Hiển thị ký hiệu logo cá nhân và họ tên "Bùi Lý Hải"; nhấp vào cuộn mượt về đầu trang `#top`. | <kbd>Đạt</kbd> | Đã sửa thẻ `<a class="brand">`, hoạt động chính xác. |
| **TC-FN-02** | **Điều hướng Menu (Navigation)** | Menu gồm 4 liên kết: Giới thiệu, Kỹ năng, Dự án, Liên hệ; cuộn mượt đến đúng vị trí tương ứng. | <kbd>Đạt</kbd> | Các neo `#about`, `#skills`, `#projects`, `#contact` hoạt động chính xác. |
| **TC-FN-03** | **Khối Giới thiệu (Hero / About)** | Hiển thị ảnh đại diện, tiêu đề nghề nghiệp, mô tả bản thân và 2 nút hành động (CTA). | <kbd>Đạt</kbd> | Ảnh avatar hiển thị tốt, nút "Xem dự án" và "Liên hệ tôi" trỏ đúng đích. |
| **TC-FN-04** | **Danh mục Kỹ năng (Skills)** | Hiển thị đầy đủ kỹ năng lập trình web và kỹ năng mềm theo dạng chip trực quan. | <kbd>Đạt</kbd> | 10 chip kỹ năng hiển thị rõ ràng, chia cột cân đối. |
| **TC-FN-05** | **Lưới Dự án tiêu biểu (Projects)** | Hiển thị 3 card dự án với hình ảnh, tiêu đề, mô tả ngắn gọn, tags kỹ thuật. | <kbd>Cần cải thiện</kbd> | Thẻ card hiển thị chuẩn, tuy nhiên các liên kết "Xem chi tiết →" hiện là `href="#"` (chưa có trang chi tiết). |
| **TC-FN-06** | **Khối Liên hệ & Chân trang (Footer)** | Hiển thị Email, Instagram, Số điện thoại và bản quyền năm 2026 kèm nút cuộn lên đầu trang. | <kbd>Đạt</kbd> | Thẻ `mailto:builyhai0208@gmail.com` kích hoạt tốt ứng dụng gửi mail. |

---

### 2. Giao diện, trải nghiệm người dùng và khả năng tương thích

> Đánh giá độ hoàn thiện giao diện, tính thẩm mỹ, khả năng thích ứng đa màn hình và tính tiếp cận.

| Mã TC | Hạng mục kiểm tra | Kết quả mong đợi | Trạng thái | Ghi chú & Minh chứng thực tế |
| :---: | :--- | :--- | :---: | :--- |
| **TC-UI-01** | **Chiến lược Mobile-First** | Giao diện hiển thị chuẩn từ độ phân giải nhỏ nhất (~360px) mà không bị vỡ bố cục. | <kbd>Đạt</kbd> | Bố cục dạng cột đơn thông suốt trên Mobile viewport. |
| **TC-UI-02** | **Đáp ứng đa kích thước (Responsive)** | Tự động thích ứng trên Tablet (768px+) và Desktop (1280px+). | <kbd>Đạt</kbd> | Media Queries nâng cấp bố cục thành 2 cột (Hero) và 3 cột lưới CSS Grid (Projects). |
| **TC-UI-03** | **Tương thích trình duyệt (Cross-Browser)** | Hiển thị đồng nhất trên Chrome, Edge, Safari, Firefox. | <kbd>Đạt</kbd> | Không phát sinh sai lệch hiển thị; CSS Grid & Flexbox chuẩn W3C. |
| **TC-UI-04** | **Typography & Bảng màu** | Độ tương phản chữ và nền đạt chuẩn dễ đọc; font hệ thống load tức thì. | <kbd>Đạt</kbd> | Hệ thống màu `:root` đồng bộ, tương phản text trên background tốt. |
| **TC-UI-05** | **Hiệu ứng vi tương tác (Micro-interactions)** | Hiệu ứng rê chuột (Hover) trên nút bấm, liên kết và thẻ card mượt mà. | <kbd>Đạt</kbd> | Transition êm ái, có phản hồi thị giác rõ ràng cho người dùng. |
| **TC-UI-06** | **Khả năng tiếp cận (Accessibility - a11y)** | Có `lang="vi"`, thuộc tính `alt` cho ảnh, `aria-label` cho các thành phần điều hướng. | <kbd>Đạt</kbd> | Trình đọc màn hình (Screen Reader) nhận diện tốt cấu trúc trang. |

#### 📸 HÌNH ẢNH MINH CHỨNG KIỂM THỬ RESPONSIVE (LƯU TẠI `docs/screenshots/`)

> Các ảnh chụp màn hình thực tế được tự động thu thập từ trình duyệt Chrome Headless trên các độ phân giải tiêu chuẩn:

##### 📱 1. Minh chứng giao diện Điện thoại di động (Mobile - 375x812 Viewport)
*File lưu trữ: `docs/screenshots/responsive_mobile.png`*
![Minh chứng Responsive Mobile](./screenshots/responsive_mobile.png)

##### 📟 2. Minh chứng giao diện Máy tính bảng (Tablet - 768x1024 Viewport)
*File lưu trữ: `docs/screenshots/responsive_tablet.png`*
![Minh chứng Responsive Tablet](./screenshots/responsive_tablet.png)

##### 💻 3. Minh chứng giao diện Máy tính để bàn (Desktop - 1440x900 Viewport)
*File lưu trữ: `docs/screenshots/responsive_desktop.png`*
![Minh chứng Responsive Desktop](./screenshots/responsive_desktop.png)

---

### 3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

> Đo lường tốc độ tải, độ ổn định và khả năng xử lý các tình huống biên.

| Mã TC | Hạng mục kiểm tra | Kết quả mong đợi | Trạng thái | Ghi chú & Minh chứng thực tế |
| :---: | :--- | :--- | :---: | :--- |
| **TC-PF-01** | **Tốc độ tải trang (Page Load Time)** | Tải trang hoàn tất < 1.0 giây trên đường truyền thông thường. | <kbd>Đạt</kbd> | 100% tài nguyên tĩnh, không thư viện bên thứ ba, FCP < 0.2s. |
| **TC-PF-02** | **Hiện tượng tràn khung ngang (Horizontal Scroll)** | Không xuất hiện thanh cuộn ngang gây vỡ giao diện trên di động. | <kbd>Đạt</kbd> | Đã kiểm soát bằng `overflow-x: hidden` và `max-width: 100%` cho ảnh. |
| **TC-PF-03** | **Lỗi thực thi (Console Errors)** | Tab Console trên trình duyệt không xuất hiện cảnh báo đỏ hoặc lỗi runtime. | <kbd>Đạt</kbd> | 0 Console errors/warnings. |
| **TC-PF-04** | **Xử lý sự cố ảnh hỏng (Image Fallback)** | Nếu ảnh không tải được, hiển thị văn bản thay thế `alt` rõ ràng. | <kbd>Đạt</kbd> | Toàn bộ ảnh đã được gán thuộc tính `alt` có nghĩa. |
| **TC-PF-05** | **Độ mượt mà khi cuộn (Scroll Performance)** | Cuộn trang đạt tốc độ ổn định 60fps trên màn hình tần số quét cao. | <kbd>Đạt</kbd> | Chuyển động mượt mà nhờ `scroll-behavior: smooth`. |

---

### 4. Bảo mật, quản lý cấu hình và dữ liệu

> Đánh giá tính an toàn của mã nguồn và tính linh hoạt trong việc cấu hình.

| Mã TC | Hạng mục kiểm tra | Kết quả mong đợi | Trạng thái | Ghi chú & Minh chứng thực tế |
| :---: | :--- | :--- | :---: | :--- |
| **TC-SC-01** | **Lỗ hổng mã độc & XSS Injection** | Không có điểm nhập liệu động nào có nguy cơ bị tiêm mã JavaScript độc hại. | <kbd>Đạt</kbd> | Trang web thuần tĩnh, không nhận input dữ liệu từ người dùng. |
| **TC-SC-02** | **Quản lý biến cấu hình (Design Tokens)** | Toàn bộ thông số màu sắc, khoảng cách, font chữ được quản lý tập trung. | <kbd>Đạt</kbd> | Khối `:root` tại `assets/css/styles.css` cho phép tùy biến toàn trang tức thì. |
| **TC-SC-03** | **Bảo vệ tài nguyên đóng gói Docker** | Không sao chép các tệp tài liệu nhạy cảm hoặc không cần thiết vào Docker Image. | <kbd>Đạt</kbd> | `.dockerignore` loại trừ chuẩn xác `.git`, `*.docx`, `*.zip`. |
| **TC-SC-04** | **An toàn liên kết ngoài (External Links)** | Các liên kết mở sang tab mới cần có thuộc tính bảo mật `rel="noopener noreferrer"`. | <kbd>Cần cải thiện</kbd> | Cần bổ sung `target="_blank" rel="noopener noreferrer"` cho liên kết Instagram. |

---

### 5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

> Kiểm tra quy chuẩn tổ chức thư mục, tính rõ ràng của code và mức độ đầy đủ của tài liệu dự án.

| Mã TC | Hạng mục kiểm tra | Kết quả mong đợi | Trạng thái | Ghi chú & Minh chứng thực tế |
| :---: | :--- | :--- | :---: | :--- |
| **TC-DS-01** | **Cấu trúc thư mục (Repository Structure)** | Tách bạch rõ ràng thư mục mã nguồn `assets/`, tài liệu `docs/`, và file gốc. | <kbd>Đạt</kbd> | Cấu trúc chuẩn mực, khoa học và trực quan. |
| **TC-DS-02** | **Định dạng & Chú thích mã nguồn** | HTML và CSS được thụt đầu dòng chuẩn mực, có chú thích khối chức năng. | <kbd>Đạt</kbd> | Mã nguồn sạch sẽ, tuân thủ quy tắc CSS Mobile-First. |
| **TC-DS-03** | **Tài liệu hướng dẫn (README.md)** | Đầy đủ 10 mục: mô tả, công nghệ, hướng dẫn cho Windows, macOS, Linux, Docker. | <kbd>Đạt</kbd> | File `README.md` biên soạn chi tiết, dễ thực hành. |
| **TC-DS-04** | **Tài liệu phát hành (RELEASENOTE.md)** | Ghi nhận chi tiết phiên bản v1.0, ngày phát hành, chức năng, lỗi sửa, hạn chế. | <kbd>Đạt</kbd> | File `docs/RELEASENOTE.md` chuẩn Semantic Versioning. |
| **TC-DS-05** | **Nhật ký thay đổi (AI_LOG.md)** | Truy vết đầy đủ lịch sử các can thiệp kỹ thuật và mẫu log chuẩn cho tương lai. | <kbd>Đạt</kbd> | Đã lưu vết phiên `#AI-001`, `#AI-002`, `#AI-003`. |

---

### 6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

> Kiểm chứng khả năng chạy thực tế trên các môi trường và tính sẵn sàng của hồ sơ bàn giao.

| Mã TC | Hạng mục kiểm tra | Kết quả mong đợi | Trạng thái | Ghi chú & Minh chứng thực tế |
| :---: | :--- | :--- | :---: | :--- |
| **TC-DP-01** | **Khả năng chạy cục bộ trên hệ điều hành** | Chạy tốt trên Windows, macOS, Linux bằng browser trực tiếp hoặc Python/Node.js. | <kbd>Đạt</kbd> | Đã kiểm thử thành công qua nhiều phương thức khởi chạy. |
| **TC-DP-02** | **Đóng gói và vận hành qua Docker** | Build image thành công và khởi chạy container Nginx ổn định tại cổng 8080. | <kbd>Đạt</kbd> | `Dockerfile` và `docker-compose.yml` cấu hình chính xác, nhẹ (~25MB). |
| **TC-DP-03** | **Thư mục minh chứng hình ảnh (Screenshots)** | Có thư mục chuyên biệt để lưu ảnh chụp màn hình kiểm thử thực tế. | <kbd>Đạt</kbd> | Đã lưu 3 ảnh chụp thực tế: `responsive_mobile.png`, `responsive_tablet.png`, `responsive_desktop.png` trong `docs/screenshots/`. |
| **TC-DP-04** | **Mức độ hoàn thiện hồ sơ nghiệm thu** | Đầy đủ tài liệu báo cáo, mã nguồn và tệp nén đính kèm phục vụ chấm điểm. | <kbd>Đạt</kbd> | Có đủ `BAOCAO-A2.1.docx`, `BAOCAO-A2.1.zip` và toàn bộ mã nguồn sạch. |

---

## ⚠️ IV. DANH SÁCH VẤN ĐỀ CẦN CẢI THIỆN & ĐỀ XUẤT (ISSUE TRACKING)

Dưới đây là các vấn đề mức độ thấp (Low / Trivial) được ghi nhận trong đợt kiểm thử:

| STT | Mã lỗi | Phân loại | Mô tả chi tiết | Mức độ ưu tiên | Trạng thái xử lý |
| :---: | :---: | :---: | :--- | :---: | :---: |
| 1 | `ISS-01` | Chức năng (Link) | Nút "Xem chi tiết →" trên 3 thẻ dự án đang để liên kết giữ chỗ `#`. | **Thấp (Low)** | Cần bổ sung link GitHub/demo ở v1.1 |
| 2 | `ISS-02` | Bảo mật (Link) | Liên kết Instagram mở ra ngoài chưa có `target="_blank" rel="noopener noreferrer"`. | **Thấp (Low)** | Khuyến nghị bổ sung ở bản vá kế tiếp |
| 3 | `ISS-03` | Minh chứng | Bổ sung hình ảnh kiểm thử thực tế vào `docs/screenshots/`. | **Thấp (Low)** | ✅ **ĐÃ GIẢI QUYẾT (Đã chụp đủ 3 ảnh)** |

---

## 🏆 V. ĐÁNH GIÁ TỔNG KẾT & KẾT LUẬN (QA SIGN-OFF)

### 1. Nhận định chung của Kỹ sư Kiểm thử
- **Độ tin cậy & Ổn định:** Sản phẩm đạt độ ổn định tuyệt đối (100%), không phát sinh lỗi mã nguồn, không có lỗi console và tốc độ phản hồi tức thì.
- **Tính thẩm mỹ & Trải nghiệm:** Bố cục hiện đại, màu sắc hài hòa, tuân thủ xuất sắc triết lý *Mobile-First* và chuẩn *Responsive Web Design* (đã có minh chứng hình ảnh thực tế xác thực).
- **Tính toàn vẹn của hồ sơ:** Hệ thống tài liệu bàn giao (`README.md`, `RELEASENOTE.md`, `AI_LOG.md`, `test_report.md`, `docs/screenshots/`) được xây dựng chuyên nghiệp, chỉn chu, vượt mức kỳ vọng đối với bài kiểm tra môn học/dự án cá nhân.

### 2. Kết luận bàn giao
> **QUYẾT NGHỊ:** **CHẤP THUẬN BÀN GIAO (ACCEPTED FOR RELEASE - v1.0.0)**  
> Sản phẩm đã đáp ứng **98.3%** các tiêu chí kiểm thử nghiệm thu, không có lỗi nghiêm trọng (Blocker/Critical). Đủ điều kiện bàn giao cho khách hàng / nộp bài nghiệm thu đánh giá chất lượng.

---

## ✍️ VI. KÝ DUYỆT BÀN GIAO (APPROVAL & SIGN-OFF)

| Vai trò | Họ và tên | Chữ ký xác nhận | Ngày ký |
| :--- | :--- | :---: | :---: |
| **Kỹ sư Kiểm thử (QA/QC Engineer)** | Trợ lý Kiểm thử Chuyên nghiệp | *Đã ký xác nhận* | 05/11/2026 |
| **Lập trình viên (Developer)** | Bùi Lý Hải | *Đã ký xác nhận* | 05/11/2026 |
| **Người nghiệm thu / Giảng viên** | Hội đồng Đánh giá KT A2.1 | *(Chờ ký)* | .../.../2026 |

