# Tiệm Cà Phê &amp; Sách Góc Nhỏ

**Tên sản phẩm:** Tiệm Cà Phê Hoàng Sơn  
**Tác giả:** Tạ Hoàng Sơn (tài khoản GitHub: `tahoangson3005-lgtm`)  
**Bài tập:** A3 - Thiết kế Web và Triển khai hệ thống phần mềm (FIT4014), Đại học Đại Nam

Website tĩnh giới thiệu tiệm cà phê kết hợp không gian đọc sách. Sản phẩm dùng HTML5 ngữ nghĩa, CSS3 responsive theo hướng mobile-first, không có backend và không lưu dữ liệu đặt bàn.

## Liên kết sản phẩm

- **Repository:** <https://github.com/tahoangson3005-lgtm/tiem-ca-phe>
- **GitHub Pages:** <https://tahoangson3005-lgtm.github.io/tiem-ca-phe/>
- **Trang kết quả:** <https://tahoangson3005-lgtm.github.io/tiem-ca-phe/ket-qua.html>
- **Hồ sơ GitHub:** <https://github.com/tahoangson3005-lgtm>
- **Hoạt động bàn giao:** [AI_LOG.md](AI_LOG.md) và [RELEASE_NOTES.md](RELEASE_NOTES.md)

## Cấu trúc thư mục

```text
tiem-ca-phe/
├── index.html              # Trang chủ, giới thiệu, thực đơn, giờ mở cửa và form đặt bàn
├── ket-qua.html            # Trang mô phỏng kết quả sau khi form hợp lệ
├── css/
│   └── style.css           # Bố cục, breakpoint và trạng thái tương tác
├── assets/
│   └── images/             # Ảnh không gian, cà phê, trà và góc đọc sách
├── README.md               # Hướng dẫn mở và kiểm tra sản phẩm
├── AI_LOG.md               # Ghi nhận quyết định sử dụng AI
└── RELEASE_NOTES.md        # Ghi chú bàn giao bản v7
```

## Chạy website local

Mở trực tiếp `index.html` bằng trình duyệt cũng có thể tải được CSS và ảnh. Cách kiểm tra ổn định hơn là chạy server tĩnh:

### Python (nếu máy đã cài Python)

```powershell
cd D:\tiem-ca-phe
py -m http.server 4173
```

Hoặc dùng `python -m http.server 4173` nếu máy không hỗ trợ lệnh `py`.

Trong môi trường chưa cài Python/Node.js, có thể dùng tiện ích Live Server của VS Code để mở thư mục rồi truy cập địa chỉ do tiện ích cung cấp.

Sau khi server đã chạy, mở:

- Trang chủ: <http://localhost:4173/>
- Trang kết quả: <http://localhost:4173/ket-qua.html>

Nhấn `Ctrl+C` trong terminal để dừng server.

## Hướng dẫn kiểm tra

1. Mở trang chủ và kiểm tra các liên kết điều hướng: **Giới thiệu**, **Trải nghiệm**, **Giờ mở cửa**, **Đặt bàn**.
2. Cuộn tới phần “Trải nghiệm nổi bật”; kiểm tra ba thẻ cà phê, trà/bánh và tủ sách cùng ảnh tương ứng.
3. Kiểm tra bảng lịch mở cửa có thể cuộn ngang trên màn hình nhỏ.
4. Kéo tới form “Đặt bàn trước”.
5. Gửi form khi để trống hoặc nhập email sai định dạng để xác nhận trình duyệt từ chối dữ liệu không hợp lệ.
6. Nhập dữ liệu hợp lệ: họ tên từ 2 ký tự, email hợp lệ và yêu cầu chỗ ngồi từ 10 đến 500 ký tự, rồi nhấn **Xác nhận đặt bàn**.
7. Kiểm tra [ket-qua.html](ket-qua.html): trang xác nhận nội dung đã qua kiểm tra HTML5 và nêu rõ dữ liệu chưa được gửi hoặc lưu.
8. Thử ở các bề rộng khoảng 375 px, 640 px và 960 px trở lên. Mỗi cấp đặt từ 1 đến 2 và 3 cột thẻ; thanh điều hướng cũng chuyển sang bố cục hàng khi đủ rộng.

## Phạm vi và nguồn xuất bản

- Mã nguồn và tài liệu: <https://github.com/tahoangson3005-lgtm/tiem-ca-phe>
- Mã nguồn trang được nộp tại commit `e8b528ec155d9f5c28ea8c5e6a441505e0eac3da`: <https://github.com/tahoangson3005-lgtm/tiem-ca-phe/commit/e8b528ec155d9f5c28ea8c5e6a441505e0eac3da>
- Sản phẩm công khai bởi GitHub Pages; URL đã được kiểm tra trả về HTTP 200.
- Đây là website tĩnh. Việc đặt bàn chỉ mô phỏng; không gửi email, không gọi API và không lưu vào cơ sở dữ liệu.

## Hồ sơ và minh chứng

- [GitHub repository](https://github.com/tahoangson3005-lgtm/tiem-ca-phe)
- [GitHub profile](https://github.com/tahoangson3005-lgtm)
- [GitHub Pages bản công khai](https://tahoangson3005-lgtm.github.io/tiem-ca-phe/)
- [Ghi nhận quyết định AI](AI_LOG.md)
- [Ghi chú phát hành v7](RELEASE_NOTES.md)
