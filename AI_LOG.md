# AI_LOG - Ghi nhận quyết định sử dụng AI

## Thông tin phiên ghi nhận

- **Sản phẩm:** Tiệm Cà Phê &amp; Sách Góc Nhỏ
- **Tác giả:** Tạ Hoàng Sơn
- **Mốc ghi nhận:** 19/11/2026
- **AI được sử dụng:** Có, dùng Copilot SDK trong VS Code để hỗ trợ kiểm tra repo và soạn tài liệu bàn giao.
- **Công cụ:** VS Code/Copilot SDK, PowerShell, Git.
- **Phạm vi:** Chỉ soạn và cập nhật README, AI_LOG, RELEASE_NOTES; không sửa HTML, CSS, ảnh hoặc logic của sản phẩm.

## Hiện tượng và dữ kiện ban đầu

- Repository đã có `index.html`, `ket-qua.html`, `css/style.css` và bốn ảnh.
- README cũ chỉ ghi tên repository, mô tả ngắn và thông tin học phần.
- Chưa có `AI_LOG.md` hoặc `RELEASE_NOTES.md`.
- Git đang ở nhánh `main`, làm việc sạch, với commit sản phẩm mới nhất:
  `e8b528ec155d9f5c28ea8c5e6a441505e0eac3da` (“Add files via upload”).
- URL Pages dự kiến là `https://tahoangson3005-lgtm.github.io/tiem-ca-phe/`.
- Form đặt bàn dùng `method="get"` tới `ket-qua.html`; trang kết quả nêu rõ website tĩnh chưa gửi email hoặc lưu cơ sở dữ liệu.
- Không tìm thấy tài liệu hoặc lịch sử trong repository chứng minh AI đã tham gia xây dựng mã gốc trước phiên này.

## Nhận định trước AI

Sinh viên cần tài liệu bàn giao phải mô tả đúng trạng thái thật, không nên suy đoán về backend, chức năng lưu dữ liệu hoặc tác giả khác với thông tin repo. URL Pages cần được kiểm tra thay vì chỉ ghi theo quy tắc đặt tên. Các commit và tên cấu hình Git có thể dùng làm minh chứng cho phiên bản/mã nguồn.

## Công cụ, prompt và phản hồi

Prompt yêu cầu: tạo/sửa `README.md`, `AI_LOG.md`, `RELEASE_NOTES.md` theo nội dung bàn giao, cập nhật mọi liên kết đúng tên tệp và không tạo kết quả kiểm chứng chưa thực hiện.

Copilot đã đề xuất quy trình:

1. Quét cấu trúc repo, trang HTML, CSS và Git history.
2. Xác nhận GitHub Pages bằng truy vấn HTTP.
3. Viết tài liệu dựa trên dữ kiện đã đọc.
4. Chạy server local và kiểm tra phản hồi hai trang.

Lưu ý: AI không tự ý khẳng định mọi chức năng đã thử; các mục thử lại trong tài liệu chỉ ghi sau khi truy cập server/thực hiện kiểm tra.

## Gợi ý và quyết định

- **Gợi ý:** README cần ghi tên sản phẩm, tác giả, cách chạy, cấu trúc, kiểm tra, nguồn xuất bản và hồ sơ minh chứng.
- **Quyết định:** Chấp nhận cấu trúc này vì đúng với yêu cầu và phù hợp website tĩnh hiện có.
- **Gợi ý:** Dùng commit mới nhất làm “commit liên quan”, nhưng không ghi là commit tài liệu nếu tài liệu chưa được commit.
- **Quyết định:** Ghi commit `e8b528ec` làm mã nguồn đã nộp và mô tả tài liệu bàn giao là thay đổi của bộ file hiện tại; không tạo commit giả hoặc số commit chưa có.
- **Gợi ý:** Xác nhận Pages qua HTTP thay vì ghi URL dựa suy luận.
- **Quyết định:** Chấp nhận URL chỉ sau khi kiểm tra trả về HTTP 200.
- **Gợi ý:** Kể AI đã tạo toàn bộ sản phẩm.
- **Quyết định:** Không chấp nhận. Ghi rõ AI chỉ hỗ trợ tài liệu trong phiên này; không tìm thấy bằng chứng AI tham gia xây dựng mã gốc.

## Phần đã sửa

- `README.md`: thay mô tả ngắn cũ bằng hướng dẫn mở, cấu trúc, kiểm tra trang và liên kết minh chứng.
- `AI_LOG.md`: tạo bản ghi quyết định theo dữ kiện/nhận định/gợi ý/quyết định/kết quả thử lại.
- `RELEASE_NOTES.md`: tạo ghi chú cho bản v7, gồm commit liên quan, thay đổi, hạn chế và cách bàn giao.

## Cách thử lại và kết quả

1. Kiểm tra Git remote và commit bằng `git remote -v`, `git log`, `git ls-tree`, `git show`.
2. Kết quả: remote trùng repository trong README; commit mới nhất là `e8b528ec...`; cây commit chứa đúng hai HTML, CSS, ảnh và README.
3. Kiểm tra Pages bằng `Invoke-WebRequest`: URL root trả về HTTP 200.
4. Chạy local bằng `py -m http.server 4173`, sau đó truy cập root và `ket-qua.html`.
5. Kết quả lần đầu: `py` không có trong PATH; `python` và `node` cũng không có trong PATH.
6. Thay thế không thay đổi sản phẩm: dùng `System.Net.HttpListener` có sẵn trong Windows PowerShell để phục vụ thư mục repo.
7. Kết quả: root, `ket-qua.html`, `css/style.css` và một ảnh đại diện đều phản hồi HTTP 200 trên `http://127.0.0.1:4173/`.

## Ranh giới minh bạch

Hồ sơ này ghi lại quá trình hỗ trợ tài liệu. Các quyết định về nội dung sản phẩm, dữ liệu hiển thị và phạm vi form đặt bàn được xác định theo mã và tài liệu có trong repository, không theo một kết quả kiểm thử giả định.
