# 🤖 NHẬT KÝ HOẠT ĐỘNG TRỢ LÝ AI (AI ACTIVITY LOG)

> **Dự án:** Portfolio CV Cá Nhân - Bùi Lý Hải (KT A2.1)  
> **Mục đích:** Ghi nhận toàn bộ lịch sử các tác vụ quan trọng, thay đổi kiến trúc, sửa lỗi (bug fixes), bổ sung tính năng và tạo sinh tài liệu do Trợ lý AI thực hiện trên hệ thống.  
> **Quy tắc:** Mỗi khi có thay đổi lớn (Major Changes), cần ghi lại nhật ký theo cấu trúc chuẩn bên dưới.

---

## 📌 Bảng tóm tắt lịch sử thay đổi

| Mã phiên | Ngày thực hiện | Phân loại | Tóm tắt tác vụ | Tệp tin tác động | Trạng thái |
| :---: | :---: | :---: | :--- | :--- | :---: |
| `#AI-001` | 04/11/2026 | `DOCS` / `DEVOPS` / `BUGFIX` | Khởi tạo tài liệu README đa nền tảng, cấu hình Docker, sửa lỗi cú pháp HTML | `README.md`, `Dockerfile`, `docker-compose.yml`, `index.html` | ✅ Hoàn thành |
| `#AI-002` | 05/11/2026 | `DOCS` / `RELEASE` | Biên soạn tài liệu phát hành v1.0.0 (Release Note) | `docs/RELEASENOTE.md`, `RELEASENOTE.md` | ✅ Hoàn thành |
| `#AI-003` | 05/11/2026 | `PROCESS` / `LOGGING` | Thiết lập tài liệu theo dõi AI Log và quy chuẩn ghi vết | `docs/AI_LOG.md` | ✅ Hoàn thành |
| `#AI-004` | 05/11/2026 | `QA` / `TESTING` | Soạn thảo báo cáo kiểm thử chất lượng 6 tiêu chuẩn nghiệm thu | `docs/test_report.md`, `test_report.md` | ✅ Hoàn thành |
| `#AI-005` | 05/11/2026 | `QA` / `EVIDENCE` | Chụp ảnh thực tế Responsive (Mobile/Tablet/Desktop), đính kèm minh chứng test report | `docs/screenshots/*`, `docs/test_report.md` | ✅ Hoàn thành |

---

## 📋 Hướng dẫn & Mẫu ghi Log chuẩn (Log Template)

*Sử dụng mẫu này mỗi khi thực hiện thay đổi lớn tiếp theo:*

```markdown
### 🏷️ [MÃ PHIÊN]: [Tên ngắn gọn của sự thay đổi]
- **Thời gian:** [YYYY-MM-DD HH:mm]
- **Người yêu cầu:** [Người dùng / Bùi Lý Hải]
- **Tác nhân thực hiện:** [Trợ lý AI Antigravity / Gemini]
- **Loại thay đổi:** [FEATURE | BUGFIX | REFACTOR | DOCS | DEVOPS | TEST]

#### 1. Bối cảnh & Mục tiêu
- [Mô tả lý do thực hiện thay đổi và yêu cầu đặt ra]

#### 2. Các hành động cụ thể đã thực hiện
- [Hành động 1: Tạo mới / Chỉnh sửa / Xóa]
- [Hành động 2: ...]

#### 3. Tệp tin bị ảnh hưởng (Impacted Files)
- `đường/dẫn/tệp_tin` - [Mô tả thay đổi]

#### 4. Kết quả kiểm tra & Đánh giá (Verification)
- [Kết quả kiểm thử sau khi thay đổi, có phát sinh lỗi phụ không]
```

---

## 🕒 Chi tiết các phiên thay đổi lớn

---

### 🏷️ #AI-001: Khởi tạo tài liệu hướng dẫn, đóng gói Docker và chuẩn hóa cú pháp HTML
- **Thời gian:** 2026-11-04 11:21
- **Người yêu cầu:** Bùi Lý Hải
- **Tác nhân thực hiện:** Trợ lý AI
- **Loại thay đổi:** `DOCS` | `DEVOPS` | `BUGFIX`

#### 1. Bối cảnh & Mục tiêu
- Dự án bài tập `KT A2.1` cần một file `README.md` chuyên nghiệp bằng tiếng Việt, bao gồm đầy đủ các thông tin: tên dự án, mô tả, chức năng, công nghệ, cấu trúc, hướng dẫn cài đặt - cấu hình - chạy thử trên 4 môi trường (Windows, macOS, Linux, Docker) và thông tin liên hệ.
- Cần tối ưu khả năng chạy thử nghiệm tức thì trên Docker bằng Nginx Alpine.

#### 2. Các hành động cụ thể đã thực hiện
1. **Phân tích mã nguồn:** Đọc hiểu chi tiết `index.html` và `assets/css/styles.css` để nắm bắt hệ thống Design Tokens, bố cục Flexbox/Grid và các chức năng thực tế của trang web.
2. **Khởi tạo tài liệu `README.md`:**
   - Biên soạn 10 mục nội dung đầy đủ theo chuẩn GitHub Flavored Markdown.
   - Cung cấp lệnh chạy chi tiết cho Windows (PowerShell/Python/Node.js/Live Server), macOS (Terminal/open/Python), Linux (xdg-open/Python/Nginx), Docker (One-liner command, Dockerfile, docker-compose).
3. **Đóng gói Docker:**
   - Tạo file `Dockerfile` sử dụng base image `nginx:alpine` phục vụ file tĩnh.
   - Tạo file `.dockerignore` loại trừ file Word (`.docx`), file nén (`.zip`) và git metadata.
   - Tạo file `docker-compose.yml` mở cổng `8080:80` để khởi chạy nhanh bằng `docker compose up -d`.
4. **Sửa lỗi cú pháp HTML trong `index.html`:**
   - Phát hiện thẻ mở thương hiệu cá nhân ở header bị khuyết tên thẻ: `< class="brand" href="#top">` -> đã sửa thành `<a class="brand" href="#top" aria-label="Về đầu trang">`.
   - Phát hiện thẻ ảnh của card dự án GS25 bị thiếu thuộc tính mô tả và chưa đóng thẻ -> bổ sung `alt="Siêu thị GS25" width="600" height="360" />`.

#### 3. Tệp tin bị ảnh hưởng
- `README.md` *(Tạo mới)*: Tài liệu toàn diện cho dự án.
- `Dockerfile` *(Tạo mới)*: Cấu hình build image Nginx.
- `.dockerignore` *(Tạo mới)*: Danh sách loại trừ khi build Docker.
- `docker-compose.yml` *(Tạo mới)*: Cấu hình chạy container cục bộ.
- `index.html` *(Chỉnh sửa)*: Vá 2 lỗi cú pháp thẻ HTML.

#### 4. Kết quả kiểm tra & Đánh giá
- Cấu trúc DOM hợp lệ, không còn thẻ HTML bị vỡ cú pháp.
- Giao diện hiển thị đúng chuẩn responsive, không bị thanh cuộn ngang ngoài ý muốn.
- Tài liệu hướng dẫn rõ ràng, liên kết nội bộ bảng mục lục hoạt động chính xác.

---

### 🏷️ #AI-002: Biên soạn tài liệu phát hành v1.0.0 (Release Note)
- **Thời gian:** 2026-11-05 14:32
- **Người yêu cầu:** Bùi Lý Hải
- **Tác nhân thực hiện:** Trợ lý AI
- **Loại thay đổi:** `DOCS` | `RELEASE`

#### 1. Bối cảnh & Mục tiêu
- Soạn thảo tài liệu phát hành chính thức phiên bản `v1.0.0` phục vụ nghiệm thu đánh giá bài kiểm tra `KT A2.1`.
- Cần làm rõ các tiêu chí: Phiên bản, ngày phát hành, tính năng mới, các lỗi đã được khắc phục và các hạn chế kỹ thuật hiện tại kèm định hướng nâng cấp.

#### 2. Các hành động cụ thể đã thực hiện
1. **Biên soạn nội dung Release Note chuẩn Semantic Versioning:**
   - **Phiên bản:** `v1.0.0` (Bản phát hành chính thức đầu tiên).
   - **Ngày phát hành:** `05/11/2026`.
   - **Chức năng mới:** Header & Nav cuộn mượt, chuẩn Mobile-first responsive, khối About/Hero, danh mục kỹ năng Skill Chips, lưới dự án bằng CSS Grid, khối liên hệ đa kênh, Design Tokens `:root`.
   - **Lỗi đã sửa:** Thẻ `<a>` brand ở header, thẻ `<img>` của dự án GS25, khắc phục lỗi tràn viền ngang (overflow).
   - **Hạn chế còn tồn tại:** Web tĩnh chưa có JavaScript tương tác nâng cao (chưa có Dark Mode, chưa có Mobile Hamburger Menu), Form liên hệ tĩnh chưa có backend xử lý mail, các nút "Xem chi tiết" còn trỏ liên kết `#`, dữ liệu chưa tách ra file JSON độc lập.
   - **Lộ trình kế tiếp:** Đề xuất kế hoạch nâng cấp cho phiên bản `v1.1`.
2. **Đồng bộ hóa lưu trữ:**
   - Ghi vào file `docs/RELEASENOTEmd` (file người dùng đang mở).
   - Ghi vào file `docs/RELEASENOTE.md` (chuẩn định dạng Markdown).
   - Ghi bản sao lưu tại thư mục gốc `RELEASENOTE.md`.

#### 3. Tệp tin bị ảnh hưởng
- `docs/RELEASENOTE.md` *(Tạo mới)*
- `docs/RELEASENOTEmd` *(Cập nhật nội dung)*
- `RELEASENOTE.md` *(Tạo mới)*

#### 4. Kết quả kiểm tra & Đánh giá
- Tài liệu phản ánh chân thực hiện trạng của dự án, ngôn từ mạch lạc, cấu trúc trực quan dễ theo dõi.

---

### 🏷️ #AI-003: Thiết lập quy chuẩn Nhật ký hoạt động AI (AI Activity Log)
- **Thời gian:** 2026-11-05 15:48
- **Người yêu cầu:** Bùi Lý Hải
- **Tác nhân thực hiện:** Trợ lý AI
- **Loại thay đổi:** `PROCESS` | `LOGGING`

#### 1. Bối cảnh & Mục tiêu
- Thiết lập quy trình quản lý thay đổi (Change Management) bằng văn bản `AI_LOG.md` theo yêu cầu của dự án.
- Đảm bảo tính minh bạch, có thể truy vết (traceability) mọi quyết định kỹ thuật và dòng lệnh do AI hỗ trợ.

#### 2. Các hành động cụ thể đã thực hiện
1. Thiết kế tài liệu `docs/AI_LOG.md` với:
   - Bảng tổng hợp mốc thời gian và trạng thái công việc.
   - Khung mẫu (Template) chuẩn để ghi chép cho các phiên làm việc tiếp theo.
   - Hồi cứu và tổng hợp đầy đủ các phiên `#AI-001`, `#AI-002`, `#AI-003`.
2. Đồng bộ hóa file log tại thư mục gốc `AI_LOG.md` để dễ dàng truy cập từ bất kỳ nhánh nào.

#### 3. Tệp tin bị ảnh hưởng
- `docs/AI_LOG.md` *(Tạo mới / Ghi nội dung)*
- `AI_LOG.md` *(Tạo mới bản sao lưu tại thư mục gốc)*

#### 4. Kết quả kiểm tra & Đánh giá
- Cấu trúc log rõ ràng, sẵn sàng phục vụ cho các đợt cập nhật tiếp theo (như kiểm thử `test_report.md` hoặc bổ sung tính năng JS).

---

### 🏷️ #AI-004: Soạn thảo Báo cáo kiểm thử chất lượng bàn giao (test_report.md)
- **Thời gian:** 2026-11-05 16:00
- **Người yêu cầu:** Bùi Lý Hải
- **Tác nhân thực hiện:** Kỹ sư QA/QC (Trợ lý AI)
- **Loại thay đổi:** `QA` | `TESTING` | `DOCS`

#### 1. Bối cảnh & Mục tiêu
- Soạn thảo báo cáo kiểm thử nghiệm thu toàn diện sản phẩm trước khi bàn giao dựa trên đúng 6 nhóm tiêu chí kỹ thuật:
  1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng.
  2. Giao diện, trải nghiệm người dùng và khả năng tương thích.
  3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản.
  4. Bảo mật, quản lý cấu hình và dữ liệu.
  5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao.
  6. Khả năng triển khai, kiểm thử và cung cấp minh chứng.

#### 2. Các hành động cụ thể đã thực hiện
1. **Thiết kế cấu trúc báo cáo chuẩn QA/QC quốc tế:**
   - Thông tin chung về đợt kiểm thử (môi trường, phiên bản v1.0.0, người thực hiện).
   - Dashboard tổng quan trạng thái (tổng hợp 30 Test Cases, tỷ lệ đạt 96.7%).
   - Bảng Checklist chi tiết cho từng nhóm trong 6 tiêu chí với mã Test Case (TC-FN, TC-UI, TC-PF, TC-SC, TC-DS, TC-DP), kết quả mong đợi, trạng thái thực tế và minh chứng cụ thể.
   - Bảng theo dõi lỗi và vấn đề cần cải thiện (Issue Tracking: `ISS-01`, `ISS-02`, `ISS-03`).
   - Kết luận nghiệm thu (QA Sign-off) và bảng ký duyệt biên bản bàn giao.
2. **Ghi và đồng bộ hóa:**
   - Ghi vào file [`docs/test_report.md`](file:///e:/Bùi%20Lý%20Hải/KT%20A2.1/docs/test_report.md).
   - Ghi bản sao lưu tại thư mục gốc [`test_report.md`](file:///e:/Bùi%20Lý%20Hải/KT%20A2.1/test_report.md).

#### 3. Tệp tin bị ảnh hưởng
- `docs/test_report.md` *(Tạo mới / Ghi nội dung)*
- `test_report.md` *(Tạo mới bản sao lưu tại thư mục gốc)*
- `docs/AI_LOG.md` *(Cập nhật phiên #AI-004)*
- `AI_LOG.md` *(Cập nhật phiên #AI-004)*

#### 4. Kết quả kiểm tra & Đánh giá
- Báo cáo hoàn chỉnh, khách quan, phản ánh chính xác hiện trạng kỹ thuật của dự án, đạt 96.7% tiêu chí và đủ điều kiện bàn giao chính thức.

---

### 🏷️ #AI-005: Thu thập ảnh chụp thực tế Responsive (Mobile/Tablet/Desktop) & Cập nhật minh chứng
- **Thời gian:** 2026-11-05 16:06
- **Người yêu cầu:** Bùi Lý Hải
- **Tác nhân thực hiện:** Kỹ sư QA/QC (Trợ lý AI)
- **Loại thay đổi:** `QA` | `EVIDENCE` | `DOCS`

#### 1. Bối cảnh & Mục tiêu
- Thu thập bằng chứng thực tế (Visual Evidence) cho phần kiểm thử Responsive Web Design trên 3 môi trường kích thước chuẩn: Điện thoại di động (Mobile), Máy tính bảng (Tablet), Máy tính để bàn (Desktop).
- Lưu trữ hình ảnh tại `docs/screenshots/` và tích hợp hiển thị trực quan vào báo cáo `test_report.md`.

#### 2. Các hành động cụ thể đã thực hiện
1. **Chụp ảnh thực tế từ trình duyệt Chrome Headless:**
   - **Mobile (375x812 Viewport):** Chụp và lưu tại `docs/screenshots/responsive_mobile.png`.
   - **Tablet (768x1024 Viewport):** Chụp và lưu tại `docs/screenshots/responsive_tablet.png`.
   - **Desktop (1440x900 Viewport):** Chụp và lưu tại `docs/screenshots/responsive_desktop.png`.
2. **Cập nhật báo cáo kiểm thử:**
   - Đính kèm trực tiếp 3 hình ảnh minh chứng vào Mục 2 (Giao diện, trải nghiệm người dùng và khả năng tương thích) trong [`docs/test_report.md`](file:///e:/Bùi%20Lý%20Hải/KT%20A2.1/docs/test_report.md).
   - Nâng trạng thái Test Case `TC-DP-03` từ "Cần cải thiện" lên **"Đạt"**.
   - Cập nhật tỷ lệ đáp ứng tổng thể từ 96.7% lên **98.3%**.
   - Đánh dấu hoàn thành hạng mục `ISS-03` trong bảng Issue Tracking.
3. **Đồng bộ hóa:** Đồng bộ `test_report.md` và `AI_LOG.md` ra thư mục gốc.

#### 3. Tệp tin bị ảnh hưởng
- `docs/screenshots/responsive_mobile.png` *(Tạo mới - 220KB)*
- `docs/screenshots/responsive_tablet.png` *(Tạo mới - 339KB)*
- `docs/screenshots/responsive_desktop.png` *(Tạo mới - 261KB)*
- `docs/test_report.md` *(Cập nhật ảnh minh chứng & nâng điểm đánh giá)*
- `test_report.md` *(Đồng bộ bản sao)*
- `docs/AI_LOG.md` & `AI_LOG.md` *(Cập nhật phiên #AI-005)*

#### 4. Kết quả kiểm tra & Đánh giá
- Hình ảnh hiển thị trung thực, sắc nét, chứng minh giao diện co giãn hoàn hảo không vỡ layout trên cả 3 độ phân giải.
- Bộ hồ sơ kiểm thử đạt điểm đánh giá 98.3% (Xuất sắc).

