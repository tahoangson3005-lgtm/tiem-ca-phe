# Hồ sơ sử dụng AI - v2

**Dự án:** Tiệm Cà Phê & Sách Góc Nhỏ
**Sinh viên:** Tạ Hoàng Sơn - 2071020164
**Học phần:** FIT4014 - Thiết kế Web và Triển khai hệ thống phần mềm, Đại học Đại Nam
**Giảng viên hướng dẫn:** ThS. Lê Thái Bảo
**Phiên bản:** `v2`

## 1. Mục đích sử dụng AI

Trong quá trình thực hiện và hoàn thiện bài tập, sinh viên sử dụng:

- **Gemini:** gợi ý khung cấu trúc HTML5/CSS3 và hỗ trợ đối chiếu rubric A3.
- **GitHub Copilot:** hỗ trợ hoàn thiện mã nguồn, kiểm tra lỗi cú pháp và soạn các tệp tài liệu dự án.

AI là công cụ hỗ trợ. Sinh viên Tạ Hoàng Sơn chịu trách nhiệm kiểm tra mã, nội dung, kết quả chạy thử và quyết định cuối cùng trước khi đưa vào sản phẩm.

## 2. Nhận định và chuẩn bị trước khi dùng AI

Trước khi yêu cầu hỗ trợ, phạm vi sản phẩm được xác định là website tĩnh gồm hai trang HTML (`index.html`, `ket-qua.html`), một tệp CSS (`css/style.css`) và các ảnh trong `assets/images/`. Form chỉ mô phỏng kiểm tra hợp lệ bằng HTML5 và điều hướng tới trang kết quả; không có backend.

Lưới thẻ cần đáp ứng chiều rộng tối thiểu khoảng `280px` mỗi thẻ. Với khoảng cách giữa thẻ `20px` và phần đệm hai bên nội dung `32px`, ước lượng:

- Hai cột: `2 × 280px + 20px + 32px = 612px`; chọn breakpoint `640px`.
- Ba cột: `3 × 280px + 2 × 20px + 32px = 912px`; chọn breakpoint `960px`.

Các mốc được làm tròn lên để có khoảng đệm cho bố cục và khớp với breakpoint trong `css/style.css`. Bố cục mặc định trên màn hình nhỏ vẫn là một cột.

## 3. Phần nội dung AI gợi ý và quyết định của sinh viên

AI hỗ trợ đề xuất cấu trúc HTML semantic, cách sắp xếp nội dung responsive, các điểm cần rà soát theo rubric và cách diễn đạt tài liệu bàn giao. Sinh viên trực tiếp đối chiếu các gợi ý với hai trang HTML, CSS và tài nguyên thực tế trong repository.

Tạ Hoàng Sơn chấp nhận hoặc chỉnh sửa các gợi ý để nội dung phản ánh đúng đề tài Tiệm Cà Phê & Sách Góc Nhỏ, thông tin sinh viên, chức năng hiện có và giới hạn của một website tĩnh. Các khẳng định về khả năng gửi form, bố cục, trạng thái focus và HTTP được đưa vào hồ sơ sau khi kiểm tra trên bản GitHub Pages. AI không thay thế quyết định và trách nhiệm kiểm chứng của sinh viên.

## 4. Quá trình tự kiểm chứng

- Rà soát tên tệp mới theo `kebab-case` khi phù hợp; giữ đúng tên `AI_LOG.md` theo yêu cầu bộ hồ sơ.
- Đối chiếu các đường dẫn tương đối trong HTML (`css/style.css`, `assets/images/...`, `ket-qua.html`) để hạn chế lỗi `404` khi chạy dưới đường dẫn con trên GitHub Pages.
- Dùng trình duyệt kiểm tra các mốc `320px`, `640px`, `960px` và `1440px`, xác nhận không cuộn ngang toàn trang và lưới thẻ lần lượt có một, hai, ba cột.
- Dùng phím `Tab` để kiểm tra focus bàn phím và viền `:focus-visible`.
- Thử form ở ba trạng thái: dữ liệu trống, email sai định dạng và dữ liệu hợp lệ chuyển tới `ket-qua.html`.
- Kiểm tra cấu trúc mỗi trang có một `<h1>` và một `<main>`; kiểm tra HTTP `200` cho trang chủ, trang kết quả, CSS và ảnh hero trên GitHub Pages.

Các kết quả chi tiết được ghi trong [`evidence-index.md`](evidence-index.md). Bản `AI_LOG.md` ở thư mục gốc là hồ sơ lịch sử trước đó; tài liệu này là khai báo AI chi tiết cho bộ bàn giao `v2`.
