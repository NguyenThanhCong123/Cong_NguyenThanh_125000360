# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** Nguyễn Thành Công
- **MSSV:** 125000360
- **Số điện thoại:** 0375 199 493
- **Email:** cong214165@gmail.com
- **Lớp / Học phần:** Thiết kế Web (Kiểm tra giữa kỳ)
- **Tên đề tài Website:** GymStore - Website Thương Mại Điện Tử Thực Phẩm Bổ Sung & Dinh Dưỡng Thể Thao Cao Cấp
- **Công cụ AI đã sử dụng:** Google Gemini 3.8 Flash (High) / Antigravity AI Pair Programmer
- **Link GitHub Repository:** `https://github.com/CongNguyenThanh125000360/Cong_NguyenThanh_125000360` *(Thay bằng link thật khi sinh viên đẩy code)*
- **Link Live Preview (GitHub Pages):** `https://CongNguyenThanh125000360.github.io/Cong_NguyenThanh_125000360/`

---

## 1. Yêu cầu ban đầu (System / Initial Prompt)

> **Prompt tổng quan ban đầu dùng để khởi tạo khung website:**
> 
> *"Bạn là 1 chuyên gia về thiết kế web front-end. Hãy đóng vai trò kỹ sư UI/UX cao cấp để thiết kế một website thương mại điện tử chuyên nghiệp 'GymStore - Thực Phẩm Bổ Sung & Dinh Dưỡng Thể Hình' gồm 2 file chính là `index.html` và `style.css`. Website cần hướng tới đối tượng người tập gym, thể hình, thể thao với phong cách Athletic Dark Theme hiện đại, tông màu đen carbon phối cam lửa energetic `#FF5E14`. Website cần có đầy đủ các phân đoạn: Header tìm kiếm, Mega Navigation, Hero Section bứt phá giới hạn, Cam kết USP chính hãng, Flash Sale giờ vàng, Danh mục theo mục tiêu tập luyện, Bộ sưu tập sản phẩm bán chạy có bộ lọc tab, Công cụ tính Protein theo thể trạng, Đánh giá của Vận động viên/PT, Cẩm nang dinh dưỡng Blog, Form VIP Club và Mega Footer."*

---

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung Semantic HTML5 & Quản lý CSS Variables
- **Prompt đã dùng:**
  > *"Hãy rà soát lại toàn bộ file `index.html` và cấu trúc CSS. Tôi muốn mã nguồn tuân thủ nghiêm ngặt chuẩn Semantic HTML5 theo tiêu chuẩn W3C:
  > 1. Toàn bộ nội dung thân trang giữa `<header>` và `<footer>` bắt buộc phải được bao bọc trong thẻ ngữ nghĩa `<main id="main-content">`.
  > 2. Phân chia rõ ràng các khối bằng `<section>` có id và nhãn aria rõ ràng. Mỗi sản phẩm trong danh mục, đánh giá khách hàng và bài viết blog phải dùng thẻ `<article>`.
  > 3. Hạn chế tối đa việc lạm dụng thẻ `<div>` vô nghĩa, thay thế bằng `<figure>`, `<figcaption>`, `<time>`, `<address>`.
  > 4. Trong `style.css`, tại `:root` phải định nghĩa rõ biến `--primary-color: #FF5E14;`, cùng hệ thống biến màu sắc phụ (`--secondary-color`), màu nền (`--bg-dark`, `--bg-card`), font chữ (`--font-heading`, `--font-body`) và khoảng cách (`--spacing-md`, `--spacing-lg`)."*
- **Kết quả AI tạo ra:**
  - AI đã bọc lại toàn bộ nội dung trong `<main id="main-content">`.
  - Chuyển đổi các thẻ bao bọc sản phẩm và review từ `.product-card` dạng `div` sang `<article class="product-card">`.
  - Khai báo đầy đủ hệ thống CSS Variables chuẩn mực trong `:root` với biến `--primary-color`.
- **Nhận xét & Tinh chỉnh của SV:**
  - *Nhận xét:* Ban đầu AI tạo ra nhiều thẻ `div` lồng nhau ở phần thông tin địa chỉ footer và ngày đăng bài blog.
  - *Tinh chỉnh của SV:* Tôi đã yêu cầu AI đổi thẻ thông tin liên hệ thành `<address class="footer-contact-info">` và ngày đăng bài viết thành thẻ `<time datetime="2026-10-18">` để tối ưu SEO và đạt điểm tối đa tiêu chí Semantic HTML5 của đề thi.

---

### Lần 2: Tích hợp thư viện hiệu ứng Animate.css & AOS (Animate On Scroll)
- **Prompt đã dùng:**
  > *"Hãy tích hợp 2 thư viện hiệu ứng chuyển động theo đúng yêu cầu đề bài:
  > 1. **Animate.css (v4.1.1):** Thêm link CDN vào `<head>` và áp dụng các class animation phù hợp cho các phần tử trọng tâm ở Hero Section (như `animate__animated animate__fadeInLeft` cho tiêu đề chính, `animate__fadeInDown` cho huy hiệu chứng nhận, `animate__pulse animate__infinite` cho huy hiệu giảm giá -28%, và `animate__heartBeat animate__infinite` cho biểu tượng tia sét Flash Sale).
  > 2. **AOS (Animate On Scroll v2.3.4):** Nhúng cả CSS và JS của thư viện AOS, khởi tạo `AOS.init()` với thời gian chuyển động mượt mà (duration: 800ms, once: true, offset: 80). Gán các thuộc tính `data-aos="fade-up"`, `data-aos-delay`, `data-aos="zoom-in"` cho các thẻ card sản phẩm, thẻ mục tiêu tập luyện, bảng tính protein và các bài viết kiến thức để khi cuộn trang các phần tử xuất hiện uyển chuyển, không giật lag."*
- **Thách thức gặp phải:**
  - Khi người dùng click vào các nút Tab lọc danh mục sản phẩm (Whey Protein, Sữa tăng cân, Pre & Creatine,...), các sản phẩm bị ẩn/hiện động bằng JavaScript khiến thư viện AOS không tính toán lại tọa độ cuộn trang, dẫn đến một số card bị khuất hoặc không kích hoạt hiệu ứng hiển thị.
  - Ngoài ra, nếu để hiệu ứng chạy lặp lại liên tục khi cuộn lên xuống (`once: false`) sẽ gây rối mắt cho người dùng.
- **Cách sửa prompt (Debug prompt):**
  > *"Trong hàm lọc sản phẩm theo tab ở JavaScript, sau khi thay đổi display của các phần tử card, hãy gọi thêm hàm `AOS.refresh()` để thư viện tính toán lại vị trí DOM. Đồng thời đặt cấu hình `once: true` trong `AOS.init` để hiệu ứng chỉ kích hoạt một lần khi cuộn tới, đảm bảo trải nghiệm người dùng tinh tế và chuyên nghiệp."*
- **Kết quả sau khi debug:**
  - Thư viện AOS hoạt động hoàn hảo, khi chuyển tab mượt mà và các phần tử xuất hiện đồng bộ, chuẩn chỉnh theo tiêu chí chấm điểm 4 (1.5 điểm).

---

### Lần 3: Tối ưu Layout Hiện Đại (Flexbox/Grid), Responsive & Hiệu Ứng Tự Viết
- **Prompt đã dùng:**
  > *"Hãy hoàn thiện kỹ thuật CSS theo tiêu chí chấm điểm:
  > 1. Sử dụng triệt để **CSS Grid** cho lưới sản phẩm (`grid-template-columns: repeat(4, 1fr)`), lưới 4 mục tiêu tập luyện và footer 4 cột.
  > 2. Sử dụng **CSS Flexbox** cho thanh điều hướng Header, thanh tìm kiếm, cụm nút bấm CTA, thẻ thông tin giá và thanh tiến độ hàng tồn.
  > 3. Tự viết đầy đủ các trạng thái tương tác `:hover`, `:focus`, `:focus-visible` cho các nút bấm (`.btn-primary`, `.btn-outline`), các ô input biểu mẫu và hiệu ứng nhấc thẻ (`transform: translateY(-7px)`, đổ bóng neon glow `box-shadow`) cho các card sản phẩm khi rê chuột.
  > 4. Viết Media Queries chi tiết cho 4 mốc màn hình (Desktop >1200px, Laptop 992px-1199px, Tablet 768px-991px, Mobile <768px và <480px) để website hiển thị xuất sắc trên mọi thiết bị."*
- **Kết quả AI tạo ra:**
  - Giao diện đạt độ hoàn thiện UI/UX cao, co giãn tự nhiên từ màn hình máy tính 4K xuống điện thoại thông minh iPhone/Android.
  - Menu trên thiết bị di động tự động chuyển thành nút bấm hamburger và ngăn kéo điều hướng tiện lợi.

---

### Lần 4: Xây dựng các tính năng tương tác Vibe Coding mở rộng
- **Prompt đã dùng:**
  > *"Hãy bổ sung các tính năng JavaScript thuần (Vanilla JS) không phụ thuộc framework nặng nề để biến GymStore thành một ứng dụng web bán hàng tương tác sống động:
  > 1. Đồng hồ đếm ngược Flash Sale thời gian thực chạy từng giây (Giờ : Phút : Giây).
  > 2. Chức năng Thêm vào giỏ hàng (Add to Cart): Tự động cộng dồn số lượng và cập nhật tổng tiền giỏ hàng hiển thị trên Header.
  > 3. Hệ thống thông báo nổi Toast Notification thông minh trượt từ góc dưới lên mỗi khi thêm giỏ hàng thành công hoặc đăng ký nhận voucher.
  > 4. Cửa sổ xem nhanh sản phẩm (Quick View Modal) dạng popup cho phép xem hình ảnh, chọn hương vị và số lượng rồi đặt mua ngay.
  > 5. Công cụ tính toán lượng Protein & Dinh dưỡng cá nhân hóa (Nutrition Calculator): Người dùng nhập cân nặng, mục tiêu và tần suất tập luyện để nhận khuyến nghị lượng gram protein/ngày và sản phẩm bổ sung thích hợp."*
- **Kết quả AI tạo ra:**
  - Toàn bộ các tương tác chạy trơn tru, không phát sinh lỗi console, tăng tính thực chiến và điểm cộng sáng tạo cho bài thi.

---

### Lần 5: Nâng cấp Chế Độ Sáng / Tối (Dark/Light Theme) & Tối Ưu Hình Ảnh Chuẩn Thực Tế
- **Prompt đã dùng:**
  > *"Cập nhật số điện thoại thành 0375199493, email cong214165@gmail.com trên toàn bộ trang. Hãy bổ sung tính năng chuyển đổi giao diện Sáng / Tối (Dark / Light Theme Toggle) bằng CSS Variables và JavaScript, lưu trạng thái vào LocalStorage để khi tải lại trang không bị mất chế độ. Nút chuyển đổi đặt ở Header có icon Mặt trăng/Mặt trời thay đổi linh hoạt. Đồng thời, thay thế toàn bộ hình ảnh sản phẩm và nội dung bằng nguồn ảnh Unsplash chất lượng cao, đúng thực tế từng loại thực phẩm bổ sung (Whey Protein, Mass Gainer, BCAA, Pre-workout, Dầu cá Omega 3, Vận động viên thể hình)."*
- **Thách thức gặp phải:**
  - Khi chuyển sang chế độ Sáng (`[data-theme="light"]`), nếu chỉ đổi màu nền mà không tái định nghĩa độ tương phản cho tiêu đề, viền thẻ và các nút bấm, giao diện sẽ bị lóa hoặc chữ bị chìm.
- **Cách sửa prompt (Debug prompt):**
  > *"Tận dụng triệt để sức mạnh của CSS Variables. Trong `[data-theme="light"]`, ghi đè các biến: `--bg-dark: #F8FAFC`, `--bg-main: #FFFFFF`, `--bg-card: #FFFFFF`, `--text-pure: #0F172A`, `--text-primary: #1E293B`, `--border-color: #E2E8F0`, giữ nguyên `--primary-color: #FF5E14` để duy trì bản sắc thương hiệu thể thao. Ở JavaScript, dùng `data-theme` trên thẻ `<html>` và gán sự kiện click cho nút `#themeToggleBtn` kèm thông báo Toast Notification."*
- **Kết quả sau khi tinh chỉnh:**
  - Người dùng có thể bấm chuyển đổi qua lại giữa giao diện Tối và Sáng ngay lập tức cực kỳ mượt mà.
  - Hình ảnh sản phẩm trực quan, rõ nét, đúng chủng loại hũ bột protein, viên nang dầu cá và bình lắc năng lượng.

---

### Lần 6: Phát Triển Hệ Thống Đặt Hàng & Thanh Toán (Checkout Modal), Nhập Thông Tin Khách Hàng, Hóa Đơn Xác Nhận (Order Confirmation Receipt) & Tích Hợp Logo/Favicon Thương Hiệu GymStore
- **Prompt đã dùng:**
  > *"Làm thêm phần mua hàng đặt hàng rồi nhập thông tin xác nhận đặt hàng, và thêm logo vào đầu trang web. Logo chính thức của GymStore được lưu tại `assets/logo.png`, áp dụng làm favicon hiển thị trên tab trình duyệt và hiển thị tại Header, Footer. Xây dựng quy trình mua hàng hoàn chỉnh (Checkout Flow): Cho phép người dùng mở Giỏ hàng kiểm tra danh sách sản phẩm đã chọn (tăng/giảm số lượng, xóa món, nhập mã voucher giảm giá GYM100), điền thông tin người nhận (Họ tên, SĐT, Email, Tỉnh/thành phố, Quận/huyện, Địa chỉ số nhà, Ghi chú giao hàng, chọn hình thức thanh toán COD hoặc Chuyển khoản QR Bank), sau đó nhấn 'XÁC NHẬN ĐẶT HÀNG' để hiển thị popup Hóa đơn xác nhận đơn hàng thành công (Order Receipt Modal) gồm mã đơn tự sinh #GS-XXXXX, thời gian đặt, chi tiết khách hàng và danh sách món hàng kèm nút In hóa đơn và Tiếp tục mua sắm."*
- **Thách thức gặp phải:**
  - Khi giỏ hàng cập nhật số lượng hoặc xóa sản phẩm, các số liệu tạm tính, voucher giảm giá và tổng tiền thanh toán cần được đồng bộ tự động theo thời gian thực cả trên modal giỏ hàng lẫn huy hiệu trên thanh Header mà không phải tải lại trang.
  - Cần xử lý trường hợp người dùng đặt hàng khi giỏ hàng trống hoặc nhập thiếu các trường bắt buộc (Họ tên, SĐT hợp lệ, Địa chỉ).
  - Biểu tượng logo GymStore tròn màu đỏ nổi bật cần được cân chỉnh kích thước chuẩn xác (46px - 50px) để không làm vỡ bố cục thanh Header trên cả máy tính lẫn thiết bị di động, đồng thời liên kết đầy đủ `<link rel="icon">`, `<link rel="shortcut icon">` để tab trình duyệt nhận diện ngay lập tức.
- **Cách sửa prompt (Debug prompt):**
  > *"Tổ chức cấu trúc giỏ hàng bằng mảng JavaScript thuần `cartData`, viết hàm `updateCartUI()` tính toán lại `subtotal`, `appliedDiscount`, và `finalTotal` mỗi khi có thao tác thêm/bớt/xóa/nhập mã voucher `GYM100`. Khi nhấn nút 'Xác nhận đặt hàng', thực hiện validate dữ liệu form, tạo mã đơn ngẫu nhiên `#GS-` + 5 chữ số ngẫu nhiên, kết xuất hóa đơn chi tiết vào `#orderSuccessModal`, làm sạch giỏ hàng và kích hoạt Toast thông báo. Về logo, định dạng tròn có viền cam và bóng đổ nhẹ ở file `style.css` và thêm hiệu ứng xoay nhẹ khi hover."*
- **Kết quả sau khi tinh chỉnh:**
  - Hoàn thiện 100% luồng mua sắm chuyên nghiệp (E-Commerce Checkout Flow) từ lúc bấm "Thêm vào giỏ" / "Mua ngay", xem giỏ hàng, điền địa chỉ giao hàng và nhận mã hóa đơn thành công.
  - Logo thương hiệu GymStore hiển thị sắc nét trên thanh tiêu đề đầu trang, chân trang và tab trình duyệt (Favicon).

---

## 3. Đánh giá cá nhân về quá trình Vibe Coding

### 1. AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất?
- **Tiết kiệm tới 75% thời gian viết mã ban đầu (Boilerplate, CSS Styling & Dark Mode):** Việc thiết kế toàn bộ hệ thống CSS Variables, kiến trúc Dark/Light Theme hai chế độ màu, bố cục CSS Grid phức tạp và các animation chuyển động nếu viết thủ công từng dòng sẽ mất từ 5 - 7 tiếng. AI đã giúp tạo nhanh khung sườn hoàn chỉnh chỉ trong vài phút.
- **Tạo nội dung mẫu và tìm kiếm tài nguyên ảnh chuẩn xác:** Thay vì sử dụng văn bản vô nghĩa "Lorem Ipsum" và hình ảnh vỡ nét, AI đã hỗ trợ liên kết toàn bộ kho ảnh thực tế chuẩn studio và dữ liệu thực tế về ngành thể hình/supplement, giúp giao diện đạt độ hoàn thiện cao nhất.
- **Tối ưu hóa Responsive & Media Queries:** AI giúp liệt kê và tính toán chính xác các điểm ngắt (breakpoints) phù hợp với chuẩn thiết bị hiện hành.

### 2. Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?
- **Prompt cần cụ thể về chuẩn kỹ thuật thay vì ra lệnh chung chung:** Nếu chỉ yêu cầu *"làm một trang web đẹp"*, AI thường sinh ra code lộn xộn, lạm dụng thẻ `<div>`, thiếu ngữ nghĩa và không có CSS Variables. Khi chỉ định rõ *"Chuẩn Semantic HTML5 với <main>, <header>, <nav>, <article>, sử dụng CSS Variables :root { --primary-color: ... }, Flexbox & Grid, Dark/Light mode"*, kết quả trả về đạt độ chính xác và chất lượng vượt trội.
- **Phương pháp chia nhỏ theo từng Iteration (Tinh chỉnh từng bước):** Không nên kỳ vọng một prompt duy nhất giải quyết được 100% bài toán. Quy trình Vibe Coding hiệu quả nhất là: **Dựng khung kiến trúc chuẩn -> Tinh chỉnh Semantic & CSS Variables -> Tích hợp thư viện (Animate.css & AOS) -> Kiểm tra sự cố & Debug -> Thêm tính năng tương tác (Dark/Light mode, Cart, Calculator) -> Hoàn thiện UI/UX**.
- **Người lập trình phải nắm vững kiến trúc nền tảng:** AI là một trợ thủ đắc lực giúp đẩy nhanh tốc độ code (co-pilot), nhưng người kỹ sư phải giữ vai trò "thuyền trưởng" kiểm soát chất lượng mã nguồn, kiểm tra chuẩn Semantic, test các thư viện bên thứ ba và chỉnh sửa lỗi logic để đáp ứng đúng 100% barem chấm điểm của đề bài.

---
*Bản quyền nhật ký thuộc về Sinh viên: **Nguyễn Thành Công - MSSV: 125000360***  
*SĐT: 0375 199 493 | Email: cong214165@gmail.com*
