# MyanShop Project (PentaDevs)

Dự án web + mobile bán phụ kiện & thức ăn cho mèo.  
Gồm 3 phần chính: **Backend (API)**, **Web** và **Android App**.

---

## Giới thiệu tổng quan
**MyanShop** là hệ thống thương mại điện tử mini dành cho mèo,  
gồm website và ứng dụng Android kết nối chung qua một backend API (PostgreSQL).

---

## Các repository con

| 🧩 Backend (API) | Xử lý dữ liệu, kết nối PostgreSQL, cung cấp API REST | [myanshop-backend](https://github.com/Munbetis/myanshop-backend) |
| 🌐 Web (Frontend) | Giao diện website bán hàng (React / Next.js) | [myanshop-web](https://github.com/Munbetis/myanshop-web) |
| 📱 Android | Ứng dụng di động viết bằng Android Studio (Kotlin/Java) | [myanshop-android](https://github.com/Munbetis/myanshop-android) |

---

## Nhóm thực hiện: **PentaDevs**

| Thành viên | Vai trò | Nhiệm vụ chính |
|-------------|----------|----------------|
| **Lương Quốc Khánh** | Leader | Quản lý tổng thể dự án, hỗ trợ mọi mảng (backend, web, mobile, database). |
| **Lê Minh Trâm Anh** | Co-Leader | Phụ trách phần **Web** (giao diện, chức năng, test API), **kết nối Web ↔ Mobile** |
| **Lâm Bảo Ngọc** | Database & Report | Thiết kế **CSDL**, viết **SQL**, quản lý dữ liệu và thực hiện **báo cáo** tổng hợp. |
| **Nguyễn Quang Trường** | Database | Phụ trách **tạo và seed dữ liệu**, kiểm tra liên kết giữa các bảng trong CSDL.|
| **Nguyễn Hà Đăng Khoa** | Database | Xây dựng, tối ưu và kiểm thử các **truy vấn SQL**, hỗ trợ thiết kế bảng. |


## Tiến độ
- [x] Tạo cấu trúc backend (src, sql, env)
- [x] Thiết kế cơ sở dữ liệu PostgreSQL
- [ ] Kết nối API → Web
- [ ] Kết nối API → Android
- [ ] Hoàn thiện giao diện & chức năng

---

## Cách chạy demo (sau khi hoàn thiện)

### 1. Backend
```bash
cd myanshop-backend
npm install
npm run dev
```
- Server sẽ chạy tại: `http://localhost:3001/api`  
- Kết nối với cơ sở dữ liệu PostgreSQL trong thư mục `sql/`.  
- Kiểm tra API mẫu: `http://localhost:3001/api/products`
---

### 2️. Web
```bash
cd myanshop-web
npm install
npm run dev
```
- Website hiển thị tại: `http://localhost:3000`  
- Gọi dữ liệu từ backend thông qua biến môi trường:  
  `NEXT_PUBLIC_API_BASE=http://localhost:3001/api`
---

### 3️. Android
- Mở project **`myanshop-android`** bằng **Android Studio**  
- Chạy trên **emulator** hoặc **thiết bị thật**
- Cấu hình **API base URL** trong code Android:
  ```
  http://10.0.2.2:3001/api
  ```
  (Đây là địa chỉ localhost khi truy cập backend từ Android Emulator)

---

*Dự án phục vụ cho môn học **“Phát triển ứng dụng Web & Mobile”***

