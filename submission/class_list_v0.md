# Danh sách lớp v0 — Doãn Thị Phương Thảo · G07

## DMS (Hệ thống giám sát người lái)

| # | Lớp / thuộc tính | Giá trị | Để làm gì (chức năng DMS) | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | person | Có / không | Xác định sự hiện diện và vị trí người lái | Có |
| 2 | face | Có / không | Xác định khuôn mặt để phân tích trạng thái người lái | Có, nếu không bị che |
| 3 | eye_left / eye_right | open / closed / unknown | Phát hiện dấu hiệu buồn ngủ thông qua trạng thái mắt | Có, trừ khi bị che hoặc kính phản xạ |
| 4 | gaze_zone | road / mirror_l / mirror_r / mirror_c / cluster / center / lap / other | Phát hiện người lái mất tập trung hoặc nhìn khỏi đường | Có thể ước lượng từ hướng mặt và mắt |
| 5 | hand / on_wheel | yes / no / unknown | Xác định người lái có đặt tay trên vô lăng hay không | Có, nếu tay không bị che |
| 6 | seatbelt | worn_correct / worn_incorrect / not_worn / unknown | Phát hiện người lái không thắt dây an toàn đúng cách | Có, nếu dây an toàn nhìn rõ |

## OMS (Hệ thống giám sát người ngồi trong xe)

| # | Lớp / thuộc tính | Giá trị | Để làm gì (chức năng OMS) | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | person | Có / không | Phát hiện người ngồi trên các ghế trong xe | Có |
| 2 | seat | driver / front_passenger / rear_left / rear_middle / rear_right | Xác định vị trí người hoặc vật thể trong khoang xe | Có thể xác định từ vị trí |
| 3 | face | Có / không | Xác định khuôn mặt người ngồi trong xe | Có, nếu không bị che |
| 4 | child_seat | occupied: no / unknown | Nhận diện ghế an toàn trẻ em để hỗ trợ giám sát khoang xe | Có, dựa trên hình dạng |
| 5 | infant_seat | facing: rear / front | Nhận diện ghế trẻ sơ sinh và hướng đặt ghế | Có, nếu hình dạng đủ rõ |
| 6 | object | bag / box / cup / other | Phát hiện vật thể trên ghế để phân biệt với người ngồi | Có, nếu không bị che |

## 2 câu hỏi leo thang

### Câu hỏi 1

**Câu hỏi:** Khi ánh sáng IR phản xạ trên kính khiến không thể xác định trạng thái mắt, có cần đánh dấu các điểm mắt trong face13 là occluded hay chỉ đặt eye_left / eye_right = unknown?

**Khung ví dụ:** D01.png

**Cách gán tạm:** Giữ eye_left = unknown khi không xác định được trạng thái mắt. Cần hỏi coach để thống nhất cách đánh dấu occluded cho các điểm face13.

### Câu hỏi 2

**Câu hỏi:** Khi người lái quay đầu hoặc cúi xuống khiến một phần khuôn mặt không nhìn thấy, các điểm face13 không xác định được nên dùng occluded hay outside?

**Khung ví dụ:** D06.png

**Cách gán tạm:** Giữ trạng thái mắt là unknown khi không quan sát rõ. Các điểm face13 cần được kiểm tra và đánh dấu occluded hoặc outside theo khả năng xác định vị trí thực tế.
