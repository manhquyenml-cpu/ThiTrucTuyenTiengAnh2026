# CUỘC THI TRỰC TUYẾN TIẾNG ANH & HỘI NHẬP QUỐC TẾ - THPT 2026
**ĐOÀN TNCS HỒ CHÍ MINH XÃ MƯỜNG LẦM - BAN TỔ CHỨC CUỘC THI**
*Nền tảng thi trắc nghiệm trực tuyến chuẩn A1–A2 & Kiến thức ASEAN cho Đoàn viên, Thanh niên học sinh THPT*

---

## 📌 Tổng Quan Hệ Thống
Hệ thống được phát triển chuyên nghiệp, phục vụ các hội thi học sinh giỏi, ngày hội thanh niên hội nhập quốc tế do Đoàn TNCS Hồ Chí Minh và Ban Giám hiệu các trường THPT phát động.

### 🌟 Tính Năng Nổi Bật:
1. **Phần thi chuẩn hóa:**
   - **Phần 1 (12 câu):** Tiếng Anh giao tiếp cơ bản A1–A2 (Chào hỏi, mượn đồ dùng học tập, chỉ đường, ngữ pháp thì hiện tại/quá khứ/tương lai, đọc hiểu biển báo/thông báo trường học).
   - **Phần 2 (8 câu):** Kiến thức Hội nhập quốc tế & ASEAN (Lịch sử thành lập, Việt Nam gia nhập, thủ đô, biểu tượng bó lúa, di sản Angkor Wat, bản sắc "hòa nhập không hòa tan", văn hóa ứng xử không gian mạng).
   - Ngân hàng **30 câu hỏi mẫu chuẩn xác** với lời giải thích chi tiết, hệ thống chọn ngẫu nhiên 20 câu (12 câu P1 + 8 câu P2) cho mỗi lượt thi.

2. **Phòng thi thông minh & Giám sát Chống gian lận:**
   - Đồng hồ đếm ngược 15:00 phút (tự động nộp bài khi hết giờ).
   - Thanh tiến độ trực quan (%) và Bảng ma trận 20 câu hỏi (Đã làm, Chưa làm, Đang làm, Đánh dấu xem lại).
   - **Hệ thống Chống gian lận (Anti-cheating):** Giám sát sự kiện chuyển tab (`visibilitychange`) hoặc rời màn hình (`blur`). 
     - Lần 1: Cảnh báo nhắc nhở kèm âm thanh.
     - Lần 2: Cảnh báo nghiêm trọng lần cuối.
     - Lần 3: Tự động khóa và nộp bài thi ngay lập tức!

3. **Kết quả & Giấy Chứng Nhận Điện Tử (E-Certificate):**
   - Chấm điểm thang điểm 100 (5đ/câu), tính thời gian chính xác từng giây.
   - Phân loại danh hiệu vinh danh:
     - 90 – 100 điểm: **Đại sứ Hội nhập Xuất sắc 🏆**
     - 75 – 89 điểm: **Công dân Toàn cầu Tiềm năng 🌟**
     - 50 – 74 điểm: **Thanh niên Hội nhập Tích cực 🎯**
     - Dưới 50 điểm: **Chiến sĩ Lan tỏa Văn hóa 🤝**
   - **E-Certificate độ nét cao (2000 x 1414 Canvas Retina):** Khung viền mạ vàng kép, hoa văn chứng chỉ trang trọng, logo Đoàn TNCS Hồ Chí Minh & ASEAN, thông tin thí sinh, điểm số, mã tra cứu trực tuyến, con dấu đỏ và chữ ký số Ban Tổ Chức. Cho phép **Tải ảnh PNG sắc nét** bằng 1 click để chia sẻ lên mạng xã hội.
   - **Xem lại đáp án chi tiết:** Phân tích đáp án đúng/sai kèm giải thích cặn kẽ bằng tiếng Việt cho từng câu hỏi.

4. **Trang Quản Trị Ban Tổ Chức (`/admin`):**
   - Dashboard KPI: Tổng số lượt thi, điểm trung bình, điểm cao nhất, tỷ lệ giỏi/xuất sắc.
   - Biểu đồ phổ điểm trực quan.
   - Bộ lọc danh sách thí sinh: Theo Trường THPT, Khối (10, 11, 12), tìm kiếm theo tên hoặc SBD.
   - **Xuất Báo Cáo Excel (.CSV)** với chuẩn UTF-8 BOM tiếng Việt, mở trực tiếp bằng Microsoft Excel không lỗi font.
   - **Trình Quản Lý Ngân Hàng Câu Hỏi:** Thêm, Sửa, Xóa câu hỏi hoặc Khôi phục 30 câu mặc định.

---

## 🚀 Hướng Dẫn Sử Dụng & Khởi Chạy

### Cách 1: Mở trực tiếp bằng trình duyệt (Nhanh nhất - Không cần server)
Nhấp đúp chuột trực tiếp vào file:
`public/index.html`
hoặc kéo thả file này vào Google Chrome, Microsoft Edge, Firefox, Cốc Cốc. Hệ thống hoạt động 100% đầy đủ tính năng (làm bài, tính giờ, chống gian lận, xuất ảnh chứng nhận PNG, bảng xếp hạng và trang quản trị).

### Cách 2: Khởi chạy qua Node.js Server
Trong thư mục dự án:
```bash
node server.js
```
Hoặc dùng Antigravity Node:
```bash
agy-node server.js
```
Truy cập:
- Giao diện thi: `http://localhost:3000`
- Giao diện Quản trị BTC: `http://localhost:3000/admin`
- Tải file CSV báo cáo: `http://localhost:3000/api/export-csv`

---

### Cách 3: Đưa Lên GitHub Pages (Trực Tuyến Miễn Phí)
Hệ thống đã được tối ưu hoàn toàn cho GitHub Pages:
1. Đẩy mã nguồn lên repository trên GitHub.
2. Vào **Settings** trên GitHub repository -> Mục **Pages**.
3. Tại phần **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: chọn **main** (hoặc **master**) và thư mục **/ (root)**.
   - Nhấn **Save**.
4. Trang web sẽ chạy trực tuyến hoàn hảo tại: `https://<ten-tai-khoan>.github.io/<ten-repo>/`!
*(Đã cấu hình sẵn tệp `.nojekyll`, nhúng trực tiếp dữ liệu 56 học sinh và bộ câu hỏi độc lập không phụ thuộc backend).*

---

## 📁 Cấu Trúc Thư Mục
```
english-integration-contest/
├── .nojekyll                # Cấu hình bỏ qua Jekyll trên GitHub Pages
├── index.html               # Trang chính tại thư mục gốc (cho GitHub Pages)
├── app.js                   # Logic ứng dụng độc lập
├── style.css                # Tệp định dạng CSS
├── logo-doan.png            # Huy hiệu Đoàn TNCS Hồ Chí Minh
├── data/
│   ├── questions.json       # Ngân hàng 30 câu hỏi A1-A2 & Hội nhập ASEAN
│   └── submissions.json     # Dữ liệu 56 học sinh THPT Mường Lầm
├── public/                  # Thư mục public phụ trợ cho Node.js server
├── server.js                # HTTP Server & REST API backend (Node.js)
└── README.md                # Tài liệu hướng dẫn sử dụng
```
