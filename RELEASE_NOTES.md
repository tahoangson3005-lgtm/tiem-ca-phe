# RELEASE_NOTES - Bản v7

## Thông tin phát hành

- **Tên phiên bản:** Tiệm Cà Phê Hoàng Sơn v7
- **Mã phiên bản:** `v7`
- **Ngày cập nhật:** 19/11/2026
- **Nhánh:** `main`
- **Repository:** <https://github.com/tahoangson3005-lgtm/tiem-ca-phe>
- **GitHub Pages:** <https://tahoangson3005-lgtm.github.io/tiem-ca-phe/>

## Thay đổi chính

- Xác nhận website gồm trang chủ và trang kết quả đặt bàn.
- Hoàn thiện README bằng cấu trúc thư mục, hướng dẫn chạy local, hướng dẫn kiểm tra và liên kết minh chứng.
- Thêm `AI_LOG.md` ghi quá trình quyết định khi sử dụng AI.
- Thêm tài liệu phát hành `RELEASE_NOTES.md` cho bản v7.
- Giữ nguyên giao diện, CSS, ảnh và luồng form của mã sản phẩm.

## Lỗi đã sửa

- Bản tài liệu cũ thiếu hướng dẫn kiểm tra phù hợp với sản phẩm thực tế; đã bổ sung các bước theo trang, form và responsive hiện có.
- Chưa có tài liệu hồ sơ quyết định AI; đã tạo `AI_LOG.md` với dữ kiện và phạm vi minh bạch.
- Chưa có ghi chú bàn giao riêng; đã tạo tài liệu tóm tắt thay đổi, mã nguồn, hạn chế và cách kiểm tra.

Không có thay đổi logic trong mã nguồn HTML/CSS của bản này.

## Commit liên quan

- Commit mã nguồn mới nhất: `e8b528ec155d9f5c28ea8c5e6a441505e0eac3da`
- Nội dung: “Add files via upload”
- Liên kết commit: <https://github.com/tahoangson3005-lgtm/tiem-ca-phe/commit/e8b528ec155d9f5c28ea8c5e6a441505e0eac3da>
- Commit trước đó: `9a35608503ce36d20b56c095bb75b3905e71566a`
- Liên kết commit trước: <https://github.com/tahoangson3005-lgtm/tiem-ca-phe/commit/9a35608503ce36d20b56c095bb75b3905e71566a>

Tài liệu này dẫn tới cây mã nguồn hiện có; commit mới của chính tài liệu bàn giao (nếu người nộp tạo thêm commit) cần được cập nhật vào mục này trước lúc nộp cuối.

## Kiểm tra đã thực hiện

- Git tree xác nhận có `index.html`, `ket-qua.html`, `css/style.css`, thư mục ảnh và `README.md`.
- GitHub Pages root đã được truy vấn và trả về HTTP 200.
- Thử `py -m http.server 4173`, `python -m http.server 4173` và `node -e ...`; các lệnh này không khả dụng trong PATH của máy kiểm tra.
- Kiểm tra cục bộ bằng `System.Net.HttpListener` có sẵn trong Windows PowerShell trên cổng 4173.
- `http://127.0.0.1:4173/`, `/ket-qua.html`, `/css/style.css` và `/assets/images/khong-gian-quan.jpg` đều trả về HTTP 200.

## Hạn chế còn lại

- Form đặt bàn chỉ mô phỏng kiểm tra HTML5; không gửi email, không lưu dữ liệu và không xác nhận đặt chỗ phía server.
- Tên/địa chỉ/giờ mở cửa của tiệm trong nội dung là dữ liệu giao diện, chưa có nguồn dữ liệu kinh doanh độc lập.
- Chưa có bộ kiểm thử tự động hoặc quy trình CI.
- Website chưa dùng backend, cơ sở dữ liệu hoặc API.
- Các ảnh là tài nguyên trong repo; tác quyền/nguồn gốc từng ảnh chưa được ghi trong mã nguồn.

## Cách tiếp tục kiểm tra và bàn giao

1. Từ thư mục repo, chạy `py -m http.server 4173`.
2. Kiểm tra trang chủ, điều hướng, bảng lịch, ba thẻ trải nghiệm và form đặt bàn.
3. Kiểm tra form khi dữ liệu trống/sai định dạng và khi dữ liệu hợp lệ.
4. Kiểm tra trang kết quả và xác nhận thông báo không gửi/lưu dữ liệu.
5. Thử giao diện ở 375 px, 640 px và 960 px trở lên.
6. Kiểm tra bản công khai qua <https://tahoangson3005-lgtm.github.io/tiem-ca-phe/>.
7. Trước khi nộp, commit toàn bộ tài liệu và mã nguồn, ghi rõ commit cuối vào mục **Commit liên quan**, sau đó đẩy lên nhánh `main`.
8. Kiểm tra lại GitHub Pages sau khi GitHub hoàn thành triển khai.
