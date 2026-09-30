# Chương 4: Triển khai Hệ thống và Đánh giá

## 4.1. Môi trường triển khai
*(Phần này mô tả các nền tảng và công cụ được sử dụng để đưa hệ thống lên trực tuyến)*

### 4.1.1. Triển khai Frontend
- **Nền tảng**: Vercel (hoặc Netlify)
- **Công nghệ**: ReactJS / Vite
- **Quá trình triển khai**:
  - Tích hợp Git (GitHub/GitLab) để thiết lập CI/CD.
  - Cấu hình Build Command (`npm run build`) và Output Directory (`dist`).
  - Cấu hình routing (`vercel.json`) để hỗ trợ Single Page Application (SPA).

### 4.1.2. Triển khai Backend
- **Nền tảng**: Render / Vercel / VPS
- **Công nghệ**: Node.js / Express (hoặc công nghệ tương ứng của dự án)
- **Quá trình triển khai**:
  - Thiết lập các biến môi trường (Environment Variables) như Database URI, JWT Secret, v.v.
  - Khởi chạy server thông qua script `npm start`.

### 4.1.3. Cơ sở dữ liệu
- **Nền tảng**: MongoDB Atlas / Supabase / PlanetScale
- **Quá trình triển khai**:
  - Thiết lập cluster và cấu hình IP whitelist.
  - Lấy chuỗi kết nối an toàn tích hợp vào Backend.

---

## 4.2. Cấu hình hệ thống trực tuyến
*(Mô tả sơ đồ các thành phần kết nối với nhau trên cloud)*

- **Frontend URL**: `https://<tên-miền-frontend>.vercel.app`
- **Backend API URL**: `https://<tên-miền-backend>.onrender.com/api`

---

## 4.3. Đánh giá và Kiểm thử trên môi trường thực tế
*(Các bài test sau khi ứng dụng đã online)*

1. **Kiểm thử chức năng**: 
   - Đăng nhập/Đăng ký.
   - Các nghiệp vụ chính của hệ thống hoạt động ổn định, gửi nhận API tốt.
2. **Kiểm thử hiệu năng (Performance)**:
   - Tốc độ tải trang frontend ổn định nhờ CDN của Vercel.
3. **Kiểm thử bảo mật cơ bản**:
   - Giao tiếp hoàn toàn qua HTTPS.
   - API được bảo vệ bằng token.

---

## 4.4. Tài liệu hướng dẫn sử dụng (User Manual)
*(Hướng dẫn người dùng các thao tác cơ bản trên hệ thống mới triển khai)*

1. Truy cập vào đường dẫn trang chủ.
2. Thực hiện đăng nhập hoặc đăng ký tài khoản.
3. Khám phá các tính năng của ứng dụng.
