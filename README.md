# Thêm danh sách khách hàng MKT

Công cụ chuẩn hoá file khách hàng cho marketing:

- Đổi số điện thoại đầu `0` (hoặc `+84`) thành `84`, ví dụ `0912345678` → `84912345678`. Tự bỏ dấu cách, dấu chấm, dấu gạch.
- Thêm cột ngày theo định dạng `2026-10-11T16:07:00Z`.
- Xuất ra Excel (.xlsx) hoặc CSV với 3 cột: `ten`, `so_dien_thoai`, `ngay`.

## Cách dùng

1. Mở file `index.html` bằng trình duyệt (Chrome, Edge...).
2. Chọn file khách hàng (CSV hoặc Excel) có cột tên và cột số điện thoại. Xem file mẫu `mau_khach_hang.csv`.
3. Chọn cách tạo ngày:
   - **Tất cả cùng một ngày giờ**
   - **Tăng dần theo khoảng cách**: mỗi khách cách nhau N phút / giờ / ngày
   - **Ngẫu nhiên trong khoảng**: rải ngẫu nhiên giữa ngày bắt đầu và kết thúc (đã sắp xếp tăng dần)
4. Bấm **Xử lý danh sách**, rồi tải file kết quả.

Số điện thoại không hợp lệ (sau khi đổi không đủ dạng `84` + 9 số) sẽ được tô đỏ để kiểm tra lại.

### Về múi giờ

Chữ `Z` nghĩa là giờ UTC. Mặc định công cụ giữ nguyên giờ bạn nhập. Nếu bạn nhập theo giờ Việt Nam và muốn đổi sang UTC, tick ô "Giờ tôi chọn là giờ Việt Nam" (tự trừ 7 tiếng, ví dụ 23:07 → `16:07:00Z`).

Dữ liệu được xử lý ngay trên máy, không gửi lên máy chủ nào.
