# CHANGELOG

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

## Thông tin Git tham chiếu

- Remote `origin`: <https://github.com/tahoangson3005-lgtm/tiem-ca-phe>
- Commit mới nhất được kiểm tra: `f61a724a49c0979dc48a9674313c73a3015daf94` - `feat: update UI, documentation and AI log for v2`.
- Các tài liệu bàn giao trong workspace cần được commit và đẩy lên remote để xuất hiện trong repository và bản bàn giao.
