# CHANGELOG

## [v3] - 19/11/2026

- **Thay đổi:** Dọn sạch hai tệp tài liệu trùng lặp (`AI_LOG.md`, `RELEASE_NOTES.md`) ở thư mục gốc; chuẩn hóa bộ 4 tệp hồ sơ bàn giao (`README.md`, `CHANGELOG.md`, `docs/AI_LOG.md`, `docs/evidence-index.md`) theo quy chuẩn Lab 8; đồng bộ toàn bộ thông tin với báo cáo Bài tập lớn A3 của sinh viên Tạ Hoàng Sơn (MSV: 2071020164).
- **Đã kiểm tra:** Xác nhận cây thư mục sạch, toàn bộ đường dẫn tương đối (`css/style.css`, `assets/images/...`) khớp chữ hoa/thường và hoạt động ổn định trên GitHub Pages (<https://tahoangson3005-lgtm.github.io/tiem-ca-phe/>).
- **Hạn chế:** Giữ nguyên giới hạn của website tĩnh (form mô phỏng qua `GET` tới `ket-qua.html`, chưa có backend/cơ sở dữ liệu, chưa kiểm thử trên thiết bị di động vật lý).
- Commit v3 được đối chiếu: `e7e64f8`.

## v2 - Bản bàn giao

- Cập nhật giao diện website giới thiệu Tiệm Cà Phê & Sách Góc Nhỏ.
- Chuẩn hóa cách tổ chức và tham chiếu tài nguyên ảnh cục bộ, CSS và các breakpoint responsive.
- Hoàn thiện bộ hồ sơ bàn giao gồm README, changelog, khai báo sử dụng AI và bảng đối chiếu minh chứng.
- Công khai các công cụ AI đã dùng: Gemini và GitHub Copilot.
- Hoàn thiện bản ghi nhận xét cấu trúc semantic, điều hướng bàn phím và giới hạn của form tĩnh.

### Phạm vi kiểm thử

- Kiểm tra trên GitHub Pages tại các chiều rộng `320px`, `640px`, `960px` và `1440px`: không tràn ngang toàn trang; lưới thẻ chuyển lần lượt một, hai và ba cột tại các mốc breakpoint.
- Kiểm tra một `<h1>` và một `<main>` trên mỗi trang.
- Dùng `Tab` kiểm tra trạng thái `:focus-visible`.
- Kiểm tra form với dữ liệu trống, email sai định dạng và dữ liệu hợp lệ.
- Xác nhận HTTP `200` cho trang chủ, trang kết quả, CSS và ảnh hero trên GitHub Pages.

### Hạn chế hiện tại

- Đây là website tĩnh. Form dùng kiểm tra HTML5 và gửi `GET` tới `ket-qua.html`, không gửi email và không lưu database.
- Chưa có backend, API, kiểm thử tự động, CI hoặc xác nhận tương thích trên mọi thiết bị/trình duyệt.
- Các ảnh được lưu cục bộ; không có URL nguồn riêng cho từng ảnh trong mã nguồn.

## v1 - Bản nền

- Website giới thiệu tiệm cà phê kết hợp không gian đọc sách với trang chủ và trang kết quả mô phỏng đặt bàn.
- Các nội dung nền gồm phần giới thiệu, ba trải nghiệm, bảng giờ mở cửa và form đặt bàn HTML5.
