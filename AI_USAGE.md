# AI Usage Log

## 1. Công cụ AI
- Tên công cụ: Google Gemini
## 2. Mục đích sử dụng
- Hỗ trợ lập bảng khung phân tích nghiệp vụ và trải nghiệm người dùng (UI/UX) cho 5 khu vực của website donghohaitrieu.com.
- Đề xuất phương án bố cục HTML5/CSS3 cho khu vực danh sách sản phẩm và thẻ sản phẩm cải tiến.
- Hỗ trợ sinh mã nguồn mẫu và giải thích các thuộc tính CSS Grid, Flexbox, Line Clamp.
## 3. Prompt đã sử dụng
- Prompt 1 (Phân tích website): "Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng cho website thương mại điện tử. Tôi đang khảo sát website: Đồng Hồ Hải Triều (https://donghohaitrieu.com/). Hãy giúp tôi lập bảng phân tích các khu vực: 1. Trang chủ, 2. Danh mục sản phẩm, 3. Chi tiết sản phẩm, 4. Tìm kiếm, 5. Giỏ hàng..."
- Prompt 2 (Đề xuất & Tạo giao diện cải tiến): "Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện thương mại điện tử bằng HTML5 và CSS3 cải tiến khu vực thẻ sản phẩm của Đồng Hồ Hải Triều. Yêu cầu: có tiêu đề, khu vực sản phẩm tối thiểu 4 mẫu thực tế, mỗi sản phẩm có hình ảnh, tên, tag thông số, giá và nút thao tác, tách file CSS riêng, hỗ trợ máy tính và điện thoại."
## 4. Kết quả AI đề xuất
- AI cung cấp bảng phân tích chi tiết 5 khu vực với mục đích, thành phần giao diện, điểm thuận tiện và hướng cải tiến.
- AI đề xuất cấu trúc tách các thông số kỹ thuật ra khỏi tên sản phẩm thành danh sách ul.specs-tags và tạo bộ mã nguồn index.html + css/style.css.

## 5. Kiểm tra và điều chỉnh
- Loại bỏ thông tin không phù hợp: Không sử dụng đề xuất hiển thị "giá gốc gạch ngang và % giảm giá" thông thường của các sàn TMĐT vì thực tế Đồng Hồ Hải Triều kinh doanh theo chính sách bán đúng giá niêm yết hãng 100%. Thay vào đó, tôi đổi thành hiển thị "Mức trả góp 0% mỗi tháng" và "Gói bảo hành Red Guarantee" đúng với thực tế website.
- Tự chỉnh sửa mã nguồn CSS:
  + Bổ sung -webkit-line-clamp: 2 và min-height cho .product-title để xử lý lỗi lệch chiều cao khi tên đồng hồ dài/ngắn khác nhau.
  + Điều chỉnh .card-actions ở màn hình mobile (<= 600px) sang bố cục 1 cột (grid-template-columns: 1fr) sau khi kiểm tra bằng Chrome DevTools thấy 2 nút nằm ngang bị hẹp.

## 6. Phần tôi hiểu và có thể giải thích
- HTML5 Semantic: Hiểu rõ vai trò của <header>, <main>, <section>, <article>, <figure> trong việc giúp cấu trúc mã nguồn mạch lạc và tối ưu SEO.
- CSS Grid (grid-template-columns: repeat(4, 1fr)): Cách chia lưới 4 cột đều nhau trên máy tính và tự động thu về 2 cột trên màn hình nhỏ thông qua @media.
- CSS Flexbox (flex-direction: column & margin-top: auto): Cơ chế đẩy khối giá và nút mua hàng luôn bám sát đáy thẻ sản phẩm, giữ bố cục đồng đều.
- Tỷ lệ khung ảnh (padding-top: 100% + position: absolute): Kỹ thuật giữ khung ảnh sản phẩm luôn vuông vức (tỷ lệ 1:1) không bị méo hình với object-fit: cover.
