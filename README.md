Dự án : 🌟 Mẹo Vặt & Tài Nguyên - Admin Ẩn + Link Rút Gọn

**Website chia sẻ mẹo vặt và tài nguyên, kiếm tiền từ link rút gọn, với khu vực quản trị ẩn xử lý bằng PHP/MySQL.**

---

## 🎯 Tính Năng Chính

### 1. Frontend (User-facing)
- 🏠 Trang chủ hiển thị bài viết mẹo vặt/tài nguyên
- 🔍 Tìm kiếm & lọc theo danh mục
- 🔗 Link rút gọn tự động (OUO.io/AdLinkFly) trong bài viết

### 2. Backend (Admin Ẩn)
- 🚪 **Đăng nhập ẩn**: 
  - Truy cập qua đường dẫn `/hidden-admin.php` (không hiện link trên trang)
  - Xác thực bằng PHP session + MySQL
- ✍️ **Quản lý bài viết**:
  - Thêm/sửa/xóa bài viết
  - Upload tài nguyên (PDF, hình ảnh)
- 📊 **Thống kê**:
  - Lượt xem bài viết
  - Doanh thu từ link rút gọn

---

## 🛠 Công Nghệ Sử Dụng

### Frontend
- **HTML/CSS/JS thuần**
- **Thư viện**:
  - [AOS](https://michalsnik.github.io/aos/) - Hiệu ứng scroll
  - [Tippy.js](https://atomiks.github.io/tippyjs/) - Tooltip

### Backend
- **PHP 8.x** (Xử lý logic đăng nhập/API)
- **MySQL** (Lưu bài viết, user admin)
- **phpMyAdmin** (Quản lý database)

### Monetization
- 📌 Link rút gọn: [OUO.io](https://ouo.io/) API
- 📌 Quảng cáo: Google AdSense Auto Ads

---



📦 root
├── 📂 public                  
│   ├── 📄 index.html
│   ├── 📄 post.html             
│   ├── 📂 assets
│   │   ├── 📂 css
│   │   ├── 📂 js
│   │   │   ├── 📄 main.js     # Xử lý frontend
│   │   │   ├── 📄 post.js
│   │   └── 📂 images          # Ảnh upload từ bài viết
│   └── 📂 posts               # Thư mục chứa bài viết (tạo động bằng PHP)
│
├── 📂 private                 # Thư mục ẩn (không truy cập trực tiếp từ URL)
│   ├── 📄 hidden-admin.php    # Trang đăng nhập admin 
│   ├── 📄 dashboard.php       # Bảng điều khiển sau đăng nhập
│   ├── 📂 includes
│   │   ├── 📄 config.php      # Kết nối database
│   │   ├── 📄 auth.php        # Xác thực đăng nhập
│   │   └── 📄 functions.php   # Các hàm dùng chung
│   └── 📂 api
│       ├── 📄 add_post.php    # API thêm bài viết
│       └── 📄 delete_post.php # API xóa bài viết
│
├── 📂 database                # Quản lý cơ sở dữ liệu
│   ├── 📄 schema.sql          # Cấu trúc bảng MySQL
│   └── 📄 backup              # Thư mục sao lưu định kỳ
│
├── 📄 .htaccess               # Bảo mật (chặn truy cập thư mục private)
└── 📄 README.md              
