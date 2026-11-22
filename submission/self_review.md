# Tự đánh giá — Doãn Thị Phương Thảo · G07

## 1. Tự rà soát 4 cảnh

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|
| S01_rgb | person, child_seat | ok | Bộ kiểm tra tự động không phát hiện lỗi ở ảnh này. | Không cần sửa theo kết quả kiểm tra |
| S01_ir | person, child_seat | ok | Bộ kiểm tra tự động không phát hiện lỗi ở ảnh này. | Không cần sửa theo kết quả kiểm tra |
| D01 | face, face13 | flag | eye_left=unknown nhưng các điểm mắt trái chưa có cờ occluded/outside; cần xác minh thủ công. | Chưa sửa |
| D06 | face, face13 | flag | eye_left=unknown nhưng các điểm mắt trái chưa có cờ occluded/outside; cần xác minh thủ công. | Chưa sửa |

Ghi chú: Bảng trên tổng hợp kết quả kiểm tra tự động và quan sát ảnh; chưa thay thế bước tự rà soát đầy đủ trong CVAT.

## 2. Lỗi mình lặp lại nhiều nhất hôm nay

**Lỗi:** Chưa thống nhất cách sử dụng trạng thái unknown và cờ occluded/outside tại các điểm mắt trong face13.

**Vì sao mình mắc:** Khi mắt bị che hoặc khó quan sát trên ảnh hồng ngoại, việc phân biệt trạng thái mắt và khả năng nhìn thấy điểm đặc trưng còn chưa rõ ràng.

**Lần sau tránh bằng cách:** Kiểm tra từng điểm face13, đối chiếu guideline và đánh dấu occluded/outside phù hợp trước khi xuất nhãn.

## 3. Ghi chú về disagreement_log

Chưa có kết quả review chéo để xác định trường hợp bạn cùng nhóm đúng và mình sai.

Sau khi nhận kết quả review chéo, sẽ bổ sung trường hợp cụ thể và bài học rút ra.
