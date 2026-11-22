# TEAM — Ngày 12

Mã bộ ảnh: **G07** · Hình thức: **Cá nhân, có review chéo**

| Họ tên | MSSV | Đã gán đủ 22 ảnh? | Review chéo với (peer diff) | Số dòng disagreement đã xử lý |
|---|---|---|---|---|
| Doãn Thị Phương Thảo | 2A202603255 | Có | Vũ Đức Quang | 3 |

Các trường hợp chưa thống nhất và đã hỏi coach:

- Đã đối chiếu 22 ảnh với Vũ Đức Quang, phát hiện 3 bất đồng về thuộc tính child_seat.occupied.
- S01_rgb.png: Thảo sửa occupied từ unknown thành no trong bản v2; chờ Quang xác nhận kết luận.
- S02_ir.png và S02_rgb.png: đề xuất Quang sửa occupied từ unknown thành no; chờ xác nhận.
- D01 và D06: cần làm rõ cách sử dụng unknown và cờ occluded/outside đối với các điểm mắt.

## Cá nhân

### DoanThiPhuongThao-2A202603255

- **Phần mình làm:** Gán nhãn 16 ảnh OMS và 6 ảnh DMS thuộc bộ G07; xuất nhãn CVAT; kiểm tra chất lượng bằng cabin_check.py; tổng hợp kết quả kiểm tra và báo cáo cá nhân.
- **Điều mình học được hôm nay:** Hiểu cách gán nhãn người, khuôn mặt, ghế trẻ em và các thuộc tính DMS/OMS; phân biệt ảnh RGB và IR; sử dụng công cụ QC để phát hiện lỗi và cảnh báo trong dữ liệu gán nhãn.

