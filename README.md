# E-commerce UI Improvement – Đồng Hồ Hải Triều

## 1. Giới thiệu
Dự án này là bài tập cá nhân Chương 1 môn Phát triển ứng dụng WEB/TMĐT tại Trường Đại học Kinh tế TP.HCM (UEH). Dự án thực hiện khảo sát thực tế website thương mại điện tử Đồng Hồ Hải Triều và xây dựng phiên bản cải tiến cho Khu vực Tìm kiếm & Thẻ sản phẩm (Product Card) bằng HTML5 và CSS3.

## 2. Website tham khảo
- Tên website: Đồng Hồ Hải Triều
- URL: https://donghohaitrieu.com/
- Khu vực đã khảo sát: Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng.

## 3. Chức năng
- Hiển thị thanh tìm kiếm kèm từ khóa xu hướng và tóm tắt giỏ hàng.
- Hiển thị bộ lọc nhanh và danh sách 4 mẫu đồng hồ tiêu biểu.
- Tách bạch tên sản phẩm, mã SKU và các tag thông số kỹ thuật (Loại máy, Mặt kính, Kích thước, Chống nước).
- Hiển thị trạng thái tồn kho tại hệ thống Showroom, giá niêm yết, mức trả góp tạm tính và gói bảo hành đi kèm.
- Bố cục Responsive hỗ trợ tốt trên cả máy tính (4 cột), máy tính bảng (2 cột) và điện thoại di động.

## 4. Công nghệ
- HTML5 (Semantic Elements: header, main, section, article, figure)
- CSS3 (CSS Variables, Flexbox, CSS Grid, Media Queries)

## 5. Cách chạy
Tải thư mục dự án về máy và mở trực tiếp file index.html bằng trình duyệt web (Chrome, Edge, Safari, Firefox), hoặc sử dụng tiện ích Live Server trên VS Code.

## 6. Cải tiến đã thực hiện
- Vấn đề ban đầu trên website gốc: Tên sản phẩm trên lưới danh mục quá dài do ghép nối toàn bộ thông số kỹ thuật bằng dấu gạch ngang, khiến người dùng khó đọc lướt và khó so sánh nhanh các mẫu đồng hồ; thiếu nút thao tác nhanh và thông tin trả góp/tồn kho ngay trên thẻ.
- Thay đổi đã thực hiện:
  1. Giới hạn tên sản phẩm trong 2 dòng và tách các thông số cốt lõi (Automatic, Kính Sapphire, Mặt 40mm) thành các nhãn (Tag) trực quan.
  2. Bổ sung nhãn trạng thái (Swiss Made, Bán chạy, Mẫu mới 2026) và số lượng Showroom còn hàng ngay trên khung ảnh.
  3. Hiển thị mức trả góp 0% ước tính mỗi tháng và quyền lợi bảo hành Red Guarantee để tăng tỷ lệ chuyển đổi.

## 7. Hỗ trợ từ AI
- Phần AI hỗ trợ: Gợi ý khung phân tích UX cho 5 khu vực và dựng cấu trúc khung HTML/CSS ban đầu.
- Phần sinh viên tự kiểm tra, điều chỉnh và bổ sung: Đối chiếu thực tế với chính sách "không bán giảm giá" của Đồng Hồ Hải Triều để loại bỏ các nhãn giảm giá ảo; bổ sung thông tin trả góp + tồn kho showroom; tự điều chỉnh CSS Flexbox (margin-top: auto) và Media Queries (@media max-width: 600px) qua Chrome DevTools để các thẻ sản phẩm luôn thẳng hàng và dễ bấm trên điện thoại.
