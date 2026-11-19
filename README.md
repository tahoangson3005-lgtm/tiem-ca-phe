# Tiệm Cà Phê & Sách Góc Nhỏ

## 1. Sản phẩm này là gì?

Website tĩnh giới thiệu Tiệm Cà Phê & Sách Góc Nhỏ, gồm không gian quán, các trải nghiệm cà phê/trà/đọc sách, lịch mở cửa và form đặt bàn mô phỏng. Sản phẩm thuộc Bài tập lớn A3, học phần FIT4014 - Thiết kế Web và Triển khai hệ thống phần mềm, Đại học Đại Nam.

- **Sinh viên thực hiện:** Tạ Hoàng Sơn
- **Mã sinh viên:** 2071020164
- **Lớp / Ngành:** Công nghệ Thông tin (ĐH Đại Nam)
- **Giảng viên hướng dẫn:** ThS. Lê Thái Bảo
- **Phiên bản bàn giao:** `v3`

## 2. Demo

- **GitHub Pages:** <https://tahoangson3005-lgtm.github.io/tiem-ca-phe/>
- **Trang kết quả mô phỏng:** <https://tahoangson3005-lgtm.github.io/tiem-ca-phe/ket-qua.html>

URL được xác định từ remote Git `https://github.com/tahoangson3005-lgtm/tiem-ca-phe.git`. Khi nghiệm thu, nên mở liên kết bằng cửa sổ ẩn danh để kiểm tra bản đã xuất bản, tránh nội dung lưu trong cache.

## 3. Tính năng hiện có

- Điều hướng bằng liên kết neo tới phần giới thiệu, trải nghiệm, giờ mở cửa và đặt bàn.
- Ba thẻ trải nghiệm được bố trí bằng CSS Grid.
- Bảng lịch mở cửa dùng cấu trúc bảng semantic với `thead`, `tbody`, `th` và `scope`.
- Form đặt bàn tĩnh dùng ràng buộc HTML5 (`required`, kiểu email, `minlength`, `maxlength`) và gửi bằng `GET` tới `ket-qua.html`.
- CSS responsive: một cột thẻ ở màn hình hẹp, hai cột từ `640px` và ba cột từ `960px`.
- Trạng thái bàn phím `:focus-visible` cho liên kết, nút và trường nhập.

## 4. Cách mở hoặc chạy thử

1. Mở `index.html` trực tiếp bằng trình duyệt; hoặc mở thư mục dự án trong VS Code và dùng tiện ích Live Server.
2. Thử các liên kết điều hướng, ba thẻ, bảng lịch và form.
3. Dùng phím `Tab` để đi qua các liên kết và trường nhập, quan sát viền focus.
4. Thử gửi form khi để trống, nhập email sai định dạng, rồi nhập dữ liệu hợp lệ để xem `ket-qua.html`.

Form chỉ chạy kiểm tra phía trình duyệt và đưa dữ liệu lên URL bằng `GET`; không nhập thông tin cá nhân thật khi thử trên bản công khai.

## 5. Cấu trúc thư mục

```text
tiem-ca-phe/
├── index.html
├── ket-qua.html
├── css/
│   └── style.css
├── assets/
│   └── images/
│       ├── ca-phe-phin.jpg
│       ├── goc-doc-sach.jpg
│       ├── khong-gian-quan.jpg
│       └── tra-trai-cay.jpg
├── docs/
│   ├── AI_LOG.md
│   └── evidence-index.md
├── CHANGELOG.md
└── README.md
```

Hồ sơ khai báo AI của bản bàn giao `v3` nằm tại [`docs/AI_LOG.md`](docs/AI_LOG.md).

## 6. Đã kiểm tra

Kiểm tra trực tiếp trên GitHub Pages:

- Không có cuộn ngang toàn trang ở các chiều rộng `320px`, `640px`, `960px` và `1440px`.
- Lưới thẻ lần lượt có một, hai và ba cột tại `320px`, `640px` và `960px` (ba cột tiếp tục ở `1440px`).
- Dùng `Tab` để lấy focus bàn phím; phần tử đang focus hiển thị viền `:focus-visible`.
- Ba trạng thái form: bỏ trống bị trình duyệt chặn; email sai định dạng bị chặn; dữ liệu hợp lệ chuyển tới trang kết quả bằng `GET`.
- Mỗi trang `index.html` và `ket-qua.html` có đúng một `<h1>` và một `<main>`.
- Network Status `200` đã xác nhận cho trang chủ, trang kết quả, CSS và ảnh hero.

Chi tiết phép thử và kết quả có trong [bảng minh chứng](docs/evidence-index.md).

## 7. Giới hạn / Chưa kiểm tra

- Form tĩnh chỉ mô phỏng kiểm tra HTML5 và chuyển tới `ket-qua.html` bằng phương thức `GET`; chưa gửi email, lưu cơ sở dữ liệu hoặc xác nhận đặt chỗ phía máy chủ.
- Chưa có backend, API, cơ sở dữ liệu, bộ kiểm thử tự động hoặc CI.
- Kiểm tra responsive được thực hiện tại các mốc nêu trên; không phải kiểm thử trên mọi trình duyệt, thiết bị hay mọi chiều rộng trung gian.
- Các ảnh được đóng gói thành tệp cục bộ trong `assets/images/`; mã nguồn hiện không ghi URL nguồn riêng cho từng ảnh.

## 8. Nguồn và khai báo AI

- **Nguồn ảnh miễn phí:** Unsplash.com; các ảnh sử dụng trong website được lưu cục bộ trong `assets/images/`.
- **Gemini:** gợi ý khung cấu trúc HTML5/CSS3 và đối chiếu rubric A3.
- **GitHub Copilot:** hỗ trợ hoàn thiện mã nguồn, kiểm tra lỗi cú pháp và viết các tệp tài liệu dự án.
- Sinh viên Tạ Hoàng Sơn trực tiếp kiểm tra và quyết định nội dung được chấp nhận hoặc chỉnh sửa cho phù hợp đề tài. Chi tiết phạm vi và quá trình tự kiểm chứng được ghi tại [`docs/AI_LOG.md`](docs/AI_LOG.md).
