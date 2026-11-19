# Bảng đối chiếu kiểm thử - v2

Các phép thử dưới đây được thực hiện trên GitHub Pages: <https://tahoangson3005-lgtm.github.io/tiem-ca-phe/>.

| Tiêu chí / Tuyên bố | Phép thử thực hiện | Kết quả thực tế | Minh chứng |
|---|---|---|---|
| Cấu trúc HTML5 có đúng một `<h1>` và một `<main>` trên mỗi trang | Kiểm tra `index.html` và `ket-qua.html` đã xuất bản bằng bộ chọn trình duyệt | Cả hai trang đều có `h1: 1`, `main: 1` | Trang chủ và [trang kết quả](https://tahoangson3005-lgtm.github.io/tiem-ca-phe/ket-qua.html) |
| Không cuộn ngang ở `320px` | Đặt viewport rộng `320px`, so sánh chiều rộng tài liệu với viewport | `scrollWidth` không vượt `clientWidth` | GitHub Pages, viewport `320px`; `noHorizontalOverflow: true` |
| Lưới chuyển cột tại `640px` / `960px` | Đo số cột `.card-grid` tại `320px`, `640px`, `960px` và `1440px` | Tương ứng một, hai, ba và ba cột; không tràn ngang tại các mốc đã thử | GitHub Pages, kiểm tra viewport bằng trình duyệt |
| Có viền `:focus-visible` khi điều hướng bằng bàn phím | Tải lại trang, nhấn `Tab`, kiểm tra phần tử đang nhận focus | Liên kết đầu tiên nhận focus; outline hiển thị kiểu solid | GitHub Pages, thao tác bàn phím `Tab` |
| Form xử lý đúng ba trạng thái cơ bản | Gửi form trống; gửi với email sai; gửi với dữ liệu hợp lệ | Form trống bị chặn; email sai bị chặn; dữ liệu hợp lệ chuyển bằng `GET` tới `ket-qua.html` | GitHub Pages: thông báo ràng buộc HTML5 và trang “Trang kết quả mô phỏng” |
| Tài nguyên xuất bản trả HTTP `200` | Gửi yêu cầu `HEAD` tới trang chủ, trang kết quả, CSS và ảnh hero | Cả bốn URL được kiểm tra đều trả `200` | `https://tahoangson3005-lgtm.github.io/tiem-ca-phe/`; `/ket-qua.html`; `/css/style.css`; `/assets/images/khong-gian-quan.jpg` |

Phạm vi trên là kiểm tra thủ công tại các chiều rộng và URL được liệt kê, không phải kiểm thử tự động toàn diện trên mọi trình duyệt hoặc thiết bị. Form là mô phỏng phía trình duyệt; không gửi email và không lưu dữ liệu.
