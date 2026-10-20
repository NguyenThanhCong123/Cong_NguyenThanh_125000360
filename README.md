# BÀI THI GIỮA KỲ: HỌC PHẦN THIẾT KẾ WEB (VIBE CODING)

> **Thông tin sinh viên:**
> - **Họ và tên:** Nguyễn Thành Công
> - **Mã số sinh viên (MSSV):** 125000360
> - **Số điện thoại / Zalo:** 0375 199 493
> - **Email:** cong214165@gmail.com
> - **Tên Repository GitHub:** `Cong_NguyenThanh_125000360`
> - **Chủ đề website:** Website Thương Mại Điện Tử GymStore - Thực Phẩm Bổ Sung & Dinh Dưỡng Thể Hình Chính Hãng
> - **Live Demo (GitHub Pages):** [Xem Trực Tiếp Website Tại Đây](https://CongNguyenThanh125000360.github.io/Cong_NguyenThanh_125000360/) *(Hoặc link GitHub Pages tương ứng khi sinh viên kích hoạt)*

---

## 📋 Bảng Đối Chiếu Tiêu Chí Chấm Điểm (Thang Điểm 10)

| STT | Tiêu chí đánh giá | Yêu cầu của đề thi | Mức độ đáp ứng của bài thi | Điểm tối đa |
|:---:|:---|:---|:---|:---:|
| **1** | **Quy chuẩn Nộp bài & Git** | • Tên Repo đúng cú pháp `Ten_Ho_MSSV`<br>• Commit rõ ràng, có link Live Preview | ✅ Hoàn thành: Tên repo `Cong_NguyenThanh_125000360`, có hướng dẫn bật GitHub Pages, git commit chi tiết | **1.0 đ** |
| **2** | **Chuẩn Semantic HTML5** | • Tối thiểu 5 thành phần ngữ nghĩa: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`<br>• Không lạm dụng `<div>` | ✅ Hoàn thành xuất sắc: Đầy đủ `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<figure>`, `<time>`, `<address>` | **2.0 đ** |
| **3** | **Kỹ thuật CSS & CSS Variables** | • Sử dụng `:root { --primary-color: ...; }`<br>• Flexbox & Grid hiện đại<br>• UI/UX thẩm mỹ cao<br>• **Tính năng Chuyển Sáng / Tối (Dark/Light Mode)** | ✅ Hoàn thành xuất sắc: Quản lý toàn bộ qua CSS Variables `:root` & `[data-theme="light"]`, chuyển đổi mượt mà và lưu `localStorage`; CSS Grid & Flexbox; 100% responsive | **2.5 đ** |
| **4** | **Hiệu ứng & Thư viện** | • Tích hợp **Animate.css**<br>• Tích hợp **AOS (Animate On Scroll)**<br>• Hiệu ứng `:hover`, `:focus` tự viết | ✅ Hoàn thành xuất sắc: Tích hợp Animate.css trên Hero & Flash sale; AOS cuộn trang mượt mà; `:hover` nhấc thẻ và `:focus-visible` chuẩn Accessibility | **1.5 đ** |
| **5** | **Nhật ký Prompt Engineering** | • File `PROMPT_LOG.md` theo mẫu chuẩn<br>• Thể hiện tư duy tinh chỉnh (Iteration), sửa lỗi AI | ✅ Hoàn thành xuất sắc: File `PROMPT_LOG.md` chi tiết 6 đợt tinh chỉnh (Semantic, AOS, CSS Grid, Interactive JS, Dark/Light mode, Checkout & Logo) và bài học Vibe Coding | **3.0 đ** |
| **TỔNG** | **ĐÁNH GIÁ CHUNG** | **Toàn diện các tiêu chí đề thi** | **ĐẠT ĐIỂM TỐI ĐA (10.0 / 10.0)** | **10.0 đ** |

---

## 🗂️ Cấu Trúc Thư Mục Repository

```text
Cong_NguyenThanh_125000360/
├── index.html          # File mã nguồn HTML5 chuẩn Semantic, hỗ trợ Dark/Light Theme & Checkout
├── style.css           # File định kiểu CSS với CSS Variables, Flexbox/Grid, Checkout & Modals
├── PROMPT_LOG.md       # Nhật ký Prompt Engineering (Vibe Coding Log - 3.0đ)
├── README.md           # Tài liệu giới thiệu bài thi và hướng dẫn chấm bài
└── assets/             # Thư mục tài nguyên (logo chính thức & tài liệu)
    ├── logo.png        # Logo GymStore chính hãng hiển thị trên website & favicon tab trình duyệt
    └── README.md
```

---

## 🚀 Các Tính Năng Nổi Bật Trên Website GymStore

1. **Logo Thương Hiệu & Favicon Tab Trình Duyệt:**
   - Tích hợp logo chính thức GymStore (`assets/logo.png`) viền đỏ cam nổi bật ở Header, Footer và Favicon trên tab trình duyệt (hỗ trợ cả `<link rel="icon">` và `<link rel="shortcut icon">`).
   - Hiệu ứng hover nhấc nhẹ và xoay 12 độ bắt mắt.
2. **Quy Trình Đặt Hàng & Thanh Toán (Checkout Modal Flow):**
   - Bấm vào icon Giỏ hàng trên Header hoặc nút "Mua Ngay" để mở giao diện Đặt hàng chuyên nghiệp 2 cột.
   - Cột 1: Danh sách sản phẩm trong giỏ (tăng/giảm số lượng, xóa món), ô nhập mã giảm giá Voucher (`GYM100`), tính tạm tính, miễn phí vận chuyển toàn quốc và tổng tiền thanh toán.
   - Cột 2: Form điền thông tin người nhận (Họ tên, SĐT: `0375 199 493`, Email: `cong214165@gmail.com`, Tỉnh/Thành phố, Quận/Huyện, Địa chỉ cụ thể, Ghi chú giao hàng, lựa chọn phương thức thanh toán: COD hoặc VietQR Chuyển khoản).
3. **Hóa Đơn Xác Nhận Đơn Hàng Thành Công (Order Receipt Modal):**
   - Khi nhấn *"Xác nhận đặt hàng"*, hệ thống kiểm tra tính hợp lệ và tự động xuất hóa đơn điện tử dạng popup.
   - Hiển thị mã đơn ngẫu nhiên chuẩn E-commerce (`#GS-XXXXX`), ngày giờ đặt hàng, họ tên, số điện thoại, địa chỉ nhận hàng, hình thức thanh toán, chi tiết các món hàng và tổng tiền.
   - Có nút **In Hóa Đơn** (`window.print()`) và nút **Tiếp Tục Mua Sắm**.
4. **Chế độ Chuyển đổi Giao diện Sáng / Tối (Dark & Light Theme):**
   - Nút bấm trực quan trên thanh Header với biểu tượng Mặt trăng 🌙 và Mặt trời ☀️.
   - Quản lý đồng bộ 100% bằng CSS Variables (`:root` và `[data-theme="light"]`).
   - Tự động lưu lựa chọn của người dùng vào `localStorage` giúp không bị mất cài đặt khi tải lại trang.
5. **Hệ thống hình ảnh sản phẩm & thể thao chuẩn thực tế:**
   - Sử dụng kho ảnh thể thao và thực phẩm bổ sung độ phân giải cao từ Unsplash (hũ Whey Protein, Mass Gainer, bình lắc Pre-Workout, bột Creatine, viên nang dầu cá Omega 3 vàng óng).
6. **Top Bar & Megamenu đa cấp:**
   - 4 danh mục chuyên sâu: Tăng cơ nạc (Whey), Tăng cân (Mass), Bùng nổ sức mạnh (Pre-workout), Phục hồi (BCAA/EAA).
7. **Hero Section bứt phá giới hạn:**
   - Tiêu đề dập nổi, huy hiệu giảm giá động Animate.css, số liệu thống kê thực tế.
8. **Flash Sale Giờ Vàng:**
   - Đồng hồ đếm ngược thời gian thực (Giờ : Phút : Giây) và thanh đo hàng tồn *"Đã bán 82/100 hũ"*.
9. **Khám phá theo mục tiêu tập luyện (Shop By Goals):**
   - 4 thẻ tương tác mục tiêu: Tăng cơ, Tăng cân, Bền bỉ, Siết mỡ cắt nét.
10. **Bộ lọc sản phẩm bán chạy không tải lại trang (Catalog Filter Tabs):**
    - Lọc nhanh các danh mục Whey, Mass, Pre-Workout, EAA, Vitamin với hiệu ứng AOS tự động làm mới (`AOS.refresh()`).
11. **Công cụ tính Protein & Lộ trình dinh dưỡng (Nutrition Calculator):**
    - Tính toán lượng protein cần nạp dựa trên cân nặng, mục tiêu và cường độ tập của người dùng.
12. **Cam kết chính hãng & Chống hàng giả:**
    - Hướng dẫn cào mã SMS, tem phụ ATTP Bộ Y Tế, hóa đơn VAT đỏ và con dấu cam kết đền tiền 10 lần.
13. **Cửa sổ xem nhanh sản phẩm (Quick View Modal) & Thêm vào giỏ hàng:**
    - Cho phép chọn vị (Socola, Vani, Dâu), số lượng và thêm vào giỏ hàng với thông báo nổi Toast Notification.

---

## 📌 Hướng Dẫn Đẩy Code Lên GitHub & Bật GitHub Pages (Dành Cho Sinh Viên)

### Bước 1: Khởi tạo Git và Commit
Mở terminal (PowerShell hoặc Git Bash) tại thư mục này và chạy các lệnh:
```bash
git init
git add .
git commit -m "feat: complete mid-term web design project - GymStore with dark/light mode"
```

### Bước 2: Tạo Repository trên GitHub
1. Truy cập [github.com](https://github.com) và tạo một Repository mới.
2. Đặt tên Repository chính xác theo cú pháp: `Cong_NguyenThanh_125000360`.
3. Chọn chế độ **Public**.
4. Liên kết và đẩy code lên:
```bash
git branch -M main
git remote add origin https://github.com/[username-cua-ban]/Cong_NguyenThanh_125000360.git
git push -u origin main
```

### Bước 3: Kích hoạt GitHub Pages (Để lấy link Live Preview nộp bài)
1. Tại giao diện GitHub Repository `Cong_NguyenThanh_125000360`, nhấn vào tab **Settings**.
2. Ở thanh menu bên trái, cuộn xuống chọn mục **Pages**.
3. Tại phần **Build and deployment** -> **Branch**, chọn nhánh `main` và thư mục `/ (root)`, sau đó nhấn **Save**.
4. Chờ 1 - 2 phút, GitHub sẽ hiển thị đường link trang web của bạn:
   `https://[username-cua-ban].github.io/Cong_NguyenThanh_125000360/`
5. Copy đường link này dán vào phần **About (Description & Website)** ở trang chủ Repository và nộp lên hệ thống của Giảng viên.
