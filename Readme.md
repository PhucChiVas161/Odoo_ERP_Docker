# Hướng dẫn cài đặt (Có video hướng dẫn phía bên dưới)

## Thông tin phiên bản

- Odoo 17
- Đã thêm thư viện Odoo 17 Accounting
## Ưu và nhược của cách này

### Ưu điểm

- Dễ triển khai hơn so với cách cài đặt thông thường
- Dễ sửa lỗi khi có lỗi xảy ra
- Dễ xóa (Cài theo cách thông thường, nếu cài không cẩn thận thì sẽ bị mất dữ liệu, còn cách này thì không)
- Đã tích hợp các module cần thiệt, không cần phải cài thêm bất cứ thứ gì
- Không tốn nhiểu tài nguyên khi chạy (Bật là chạy, tắt là ngừng :)))). Còn theo cách cài đặt thông thường thì nó luôn luôn chạy, tốn tài nguyên của máy)
- Support đa nền tảng

### Nhược điểm
- Cần có 1 tí kiến thức về technical.
- Dung lượng lớn hơn (Tầm 50mb, không đáng kể)

## Chuẩn bị (Cách này dành cho windowns)

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- Cài đặt [Docker Desktop](https://www.docker.com/products/docker-desktop/)
### Hoặc
- Mở CMD bằng cách nhấn nút Windows (Trên bàn phím có hình logo Windows, gần nút ctrl trái) + R gõ CMD hoặc tham khảo [tại đây](https://quantrimang.com/cong-nghe/thu-thuat-khoi-chay-command-prompt-nhanh-chong-tren-windows-10-118680)
- Gõ lệnh hoặc copy dán vào

```
winget install -e --id Docker.DockerDesktop
```

- Done
## Cài đặt

- Tải về ngay mục [Release](https://github.com/PhucChiVas161/odoo-erp-docker/releases)
- Giải nén thư mục
- Truy cập vào thư mục vừa giải nén
- Rê chuột vào chổ trống trong thư mục, giữ nút Shift và chuột phải, chọn Open with Terminal hoặc Open with Command Prompt
- Sau đó hiển thị cửa sổ màu đen, gõ lệnh sau:

```
docker-compose up -d
```

- Lệnh đó sẽ chạy cài đặt odoo, tốc độ phụ thuộc vào mạng và máy
- Sau khi chạy và cài đặt xong, sẽ xuất hiện kết quả là Created màu xanh là chạy thành công
- Truy cập odoo bằng cách truy cập trên trình duyệt và gõ http://localhost:8069

## Video hướng dẫn
- [Windows](https://www.youtube.com/watch?v=FjjfyuB0In0)
- [MacOS (Macbook, MacPro,... nói chung là của Apple)](https://www.youtube.com/watch?v=ZMmPEiG77Sg)

## Những lỗi phổ biến (Windows)
- Khi cài và chạy lần đầu. Docker có thể hiển thị "Docker Engine stopped". Thì bật Command Prompt lên và gõ lệnh:
```
wsl --update
```
- Sau khi nó chạy xong 100% thì bật lại docker, thấy nó quay quay ghi là "Docker Engine starting..." đợi nó chạy xong là được
