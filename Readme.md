# Hướng dẫn cài đặt

## Thông tin phiên bản

- Odoo 17
- Đã thêm thư viện Odoo 17 Accounting

## Chuẩn bị

- (Docker Desktop)[https://www.docker.com/products/docker-desktop/]
- Cài đặt (Docker Desktop)[https://www.docker.com/products/docker-desktop/]
  Hoặc
- Mở CMD bằng cách nhấn nút Windows (Trên bàn phím có hình logo Windows, gần nút ctrl trái) + R gõ CMD hoặc tham khảo (tại đây)[https://quantrimang.com/cong-nghe/thu-thuat-khoi-chay-command-prompt-nhanh-chong-tren-windows-10-118680]
- Gõ lệnh hoặc copy dán vào

```
winget install -e --id Docker.DockerDesktop
```

- Done

## Cài đặt

- Tải về ngay mục Release
- Giải nén thư mục
- Truy cập vào thư mục vừa giải nén
- Rê chuột vào chổ trống trong thư mục, giữ nút Shift và chuột phải, chọn Open with Terminal hoặc Open with comment Promtp
- Sau đó hiển thị cửa sổ màu đen, gõ lệnh sau:

```
docker-compose up -d
```

- Lệnh đó sẽ chạy cài đặt odoo, tốc độ phụ thuộc vào mạng và máy
- Sau khi chạy và cài đặt xong, sẽ xuất hiện kết quả là Created màu xanh là chạy thành công
- Truy cập odoo bằng cách truy cập trên trình duyệt và gõ http://localhost:8069
