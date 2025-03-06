# Hướng Dẫn Cài Đặt Odoo (Có Video Hướng Dẫn Phía Dưới)  
**(Đọc Hướng Dẫn Thật Kỹ Trước Khi Cài Đặt)**

---

## 🔹 Thông Tin Phiên Bản

- **Odoo 17 & Odoo 18**
- Đã tích hợp thư viện **Odoo Accounting**

---

## ✅ Ưu & Nhược Điểm

### 🔥 Ưu Điểm
- **Dễ triển khai** hơn so với cách cài đặt thủ công.
- **Dễ khắc phục lỗi** nếu có sự cố xảy ra.
- **Dễ gỡ bỏ** mà không lo mất dữ liệu như cách cài đặt truyền thống.
- **Tích hợp sẵn module cần thiết**, không cần cài đặt thêm.
- **Tối ưu tài nguyên**, chỉ chạy khi cần, không tốn tài nguyên khi tắt.
- **Hỗ trợ đa nền tảng** (Windows, MacOS, Linux).

### ⚠️ Nhược Điểm
- Cần **một ít kiến thức kỹ thuật**.
- **Dung lượng lớn hơn một chút** (~50MB, nhưng không đáng kể so với lợi ích mang lại).

---

## 📌 Yêu Cầu Thiết Bị (Windows & MacOS)

### 🔹 Cấu Hình Tối Thiểu
#### Windows:
- **Hệ điều hành**: Windows 10 64-bit trở lên
- **CPU**: Hỗ trợ ảo hóa (VT-x hoặc AMD-V)
- **RAM**: Tối thiểu 4GB (khuyến nghị 8GB trở lên)
- **Ổ cứng**: Tối thiểu 20GB dung lượng trống
- **Mạng**: Kết nối internet ổn định để tải các container Docker

#### MacOS:
- **Hệ điều hành**: macOS 11 (Big Sur) trở lên
- **CPU**: Chip Intel hoặc Apple Silicon (M1, M2,...)
- **RAM**: Tối thiểu 4GB (khuyến nghị 8GB trở lên)
- **Ổ cứng**: Tối thiểu 20GB dung lượng trống
- **Mạng**: Kết nối internet ổn định để tải các container Docker

### 🔹 Cách Kiểm Tra Cấu Hình
#### Windows:
- **Kiểm Tra Ảo Hóa CPU**
  1. Mở **Task Manager** (`Ctrl + Shift + Esc`)
  2. Chuyển sang tab **Performance**
  3. Chọn mục **CPU**
  4. Tìm mục **Virtualization**
     - Nếu hiển thị **Enabled**, máy bạn hỗ trợ ảo hóa.
     - Nếu hiển thị **Disabled**, cần bật ảo hóa trong BIOS.

#### MacOS:
- **Kiểm Tra Dung Lượng Ổ Cứng**
  1. Nhấn **Cmd + Space**, gõ "About This Mac" rồi nhấn **Enter**.
  2. Chọn tab **Storage** để kiểm tra dung lượng trống.

---

## 📌 Chuẩn Bị (Dành Cho Windows & MacOS)

### 🔹 Windows:
#### Cách 1: Cài Đặt Docker Desktop
1. Tải và cài đặt **[Docker Desktop](https://www.docker.com/products/docker-desktop/)**.

#### Cách 2: Cài Đặt Docker Qua Command Prompt
1. Mở **CMD** (`Windows + R`, nhập `cmd`, nhấn **Enter**).
2. Chạy lệnh sau để cài đặt Docker Desktop:
   ```sh
   winget install -e --id Docker.DockerDesktop
   ```
3. Hoàn tất quá trình cài đặt.

### 🔹 MacOS:
1. Tải **[Docker Desktop for Mac](https://www.docker.com/products/docker-desktop/)** và chọn đúng phiên bản (**Intel Chip** là dành cho các máy chạy chip Intel. **Apple Silicon** là dành cho các máy chạy chip M1,M2,...).
2. Mở file `.dmg`, kéo ứng dụng **Docker** vào thư mục **Applications**.
3. Mở Docker, chấp nhận điều khoản sử dụng.

---

## 🚀 Cài Đặt Odoo 17 / Odoo 18

1. Tải về phiên bản mới nhất tại **[Release](https://github.com/PhucChiVas161/odoo-erp-docker/releases)**.
2. Giải nén thư mục vừa tải xuống.
3. Truy cập vào thư mục đã giải nén.
4. Nhấp chuột phải vào vùng trống trong thư mục, giữ **Shift**, chọn **Open with Terminal** hoặc **Open with Command Prompt**.
5. Nhập lệnh sau để khởi chạy Odoo:
   ```sh
   docker-compose up -d
   ```
6. Quá trình cài đặt sẽ diễn ra, tốc độ phụ thuộc vào tốc độ mạng và cấu hình máy.
7. Khi xuất hiện dòng **Created (màu xanh)**, quá trình cài đặt đã hoàn tất.
8. Truy cập Odoo bằng cách mở trình duyệt và nhập:
   ```
   http://localhost:8069
   ```
9. Những lần sau chạy, chỉ cần bật **Docker Desktop** tìm dòng **odoo_erp_docker** và bấm ⏯️ là chạy được

---

## 🔄 Cách Restart Lại Odoo Nếu Gặp Lỗi (Windows & MacOS)
1. Mở **Command Prompt (Windows)** hoặc **Terminal (MacOS)** trong thư mục chứa file `docker-compose.yml`.
2. Dừng container:
   ```sh
   docker-compose down -v
   ```
3. Khởi động lại container:
   ```sh
   docker-compose up -d
   ```
4. Đợi một lúc và kiểm tra lại bằng cách truy cập:
   ```
   http://localhost:8069
   ```

---

## 🎥 Video Hướng Dẫn

- **Windows**: [Xem video hướng dẫn](https://www.youtube.com/watch?v=FjjfyuB0In0)
- **MacOS (Macbook, MacPro, iMac, v.v.)**: [Xem video hướng dẫn](https://www.youtube.com/watch?v=ZMmPEiG77Sg)

---

## ❌ Những Lỗi Phổ Biến (Windows) & Cách Khắc Phục

### 🔹 Lỗi "Docker Engine Stopped" Khi Chạy Lần Đầu
📌 **Giải pháp:**
1. Mở **Command Prompt** (CMD) dưới quyền **Administrator**.
2. Chạy lệnh sau:
   ```sh
   wsl --install --no-distribution
   ```
3. Đợi quá trình cập nhật hoàn tất (**100%**).
4. Mở lại **Docker Desktop**, nếu thấy "Docker Engine starting..." thì chờ một chút để nó khởi động.

---

💡 **Chúc bạn cài đặt thành công!** 🚀

<h3 align="center">Liên hệ:</h3>
<p align="center">
<a href="https://fb.com/phucchivas1601" target="_blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/facebook.svg" alt="phucchivas1601" height="30" width="40" /></a>
<a href="https://www.youtube.com/@phucchivas1601" target="_blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/youtube.svg" alt="@phucchivas1601" height="30" width="40" /></a>
<a href="https://zalo.me/0931323078" target="_blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/9/91/Icon_of_Zalo.svg" alt="@phucchivas1601" height="30" width="40" /></a>
<a href="https://t.me/phuchivas" target="_blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/8/83/Telegram_2019_Logo.svg" alt="@phucchivas1601" height="30" width="40" /></a>
<a href="https://m.me/phucchivas1601" target="_blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/b/be/Facebook_Messenger_logo_2020.svg" alt="@phucchivas1601" height="30" width="40" /></a>
</p>

