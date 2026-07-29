---
name: mindmirror-theo-doi-nang-luong-va-thoi-quen
description: "Theo dõi năng lượng và thói quen hằng ngày: check-in năng lượng, ghi thói quen lõi, tìm tác nhân tăng/tụt năng lượng và chốt điều chỉnh ngày mai."
---

# MindMirror - Theo Dõi Năng Lượng Và Thói Quen

## Mục tiêu

Giúp sếp theo dõi năng lượng và thói quen hằng ngày theo cách nhẹ, rõ và có hành động:

- check-in năng lượng;
- theo dõi 3-5 thói quen lõi;
- ghi tác nhân tăng/tụt năng lượng;
- tìm pattern theo ngày/tuần;
- chốt một điều chỉnh nhỏ cho ngày mai.

Không dùng skill này để chẩn đoán sức khỏe hoặc thay thế tư vấn y tế.

## Nguồn bắt buộc phải đọc

Trước khi thực hiện:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `5. Hộp Công Cụ/Template/Template - Theo Dõi Năng Lượng Và Thói Quen.md`
5. `3. Chuyển Hoá/Tri Thức/Framework/Framework - Theo Dõi Năng Lượng Và Thói Quen.md`

Nếu đang nối với mục tiêu/ngày, đọc thêm khi có:

- `5. Hộp Công Cụ/Template/Template - Khởi Động Ngày Theo La Bàn 365.md`
- `5. Hộp Công Cụ/Template/Template - Review Cuối Ngày.md`

## Đầu vào tối thiểu

Sếp chỉ cần nói:

```text
Theo dõi năng lượng và thói quen hôm nay cho anh.
```

Nếu có dữ liệu thì nhận thêm:

- năng lượng sáng/trưa/tối theo thang 1-10;
- chất lượng ngủ và số giờ ngủ;
- thói quen muốn theo dõi;
- deep work;
- vận động;
- thiền/tĩnh tâm;
- tác nhân tăng/tụt năng lượng;
- mục tiêu chính trong ngày.

## Nếu thiếu dữ liệu

Nếu chưa có dữ liệu, hỏi tối đa 6 câu:

1. Năng lượng hiện tại của anh từ 1-10 là mấy?
2. Đêm qua anh ngủ khoảng bao lâu và chất lượng ngủ 1-10?
3. Hôm nay anh muốn theo dõi 3-5 thói quen nào?
4. Mục tiêu chính hoặc MIT hôm nay là gì?
5. Có điều gì dễ làm anh tụt năng lượng hôm nay không?
6. Anh muốn chỉ setup bảng theo dõi hay lưu vào daily note luôn?

Nếu sếp chỉ muốn setup nhanh, tạo bảng mặc định mà không hỏi quá sâu.

## Quy trình

### Bước 1. Check-in đầu ngày

Ghi:

- năng lượng hiện tại;
- chất lượng ngủ;
- cảm xúc nền;
- mục tiêu chính;
- thói quen không được bỏ;
- điều cần tránh.

### Bước 2. Chọn thói quen lõi

Nếu sếp chưa chọn, đề xuất tối đa 5 thói quen:

- ngủ đúng nhịp;
- vận động;
- thiền/tĩnh tâm;
- deep work;
- ghi chú/review ngày.

Mỗi thói quen phải có bản tối thiểu đủ nhỏ để làm trong ngày bận.

### Bước 3. Tạo bảng theo dõi

Trả về bảng:

- chỉ số năng lượng;
- bảng thói quen;
- log năng lượng theo thời điểm;
- ghi chú tăng/tụt năng lượng.

### Bước 4. Review cuối ngày nếu có dữ liệu

Nếu sếp cung cấp dữ liệu cuối ngày, phân tích:

- năng lượng trung bình;
- thói quen hoàn thành/chưa hoàn thành;
- tác nhân tăng năng lượng;
- tác nhân tụt năng lượng;
- pattern đáng chú ý.

### Bước 5. Chốt điều chỉnh ngày mai

Chỉ chọn một điều chỉnh nhỏ, cụ thể và làm được trong 24 giờ tới.

### Bước 6. Tổng hợp tuần nếu có nhiều ngày

Nếu có dữ liệu 5-7 ngày, tổng hợp:

- ngày năng lượng cao nhất/thấp nhất;
- khung giờ tốt nhất;
- thói quen ảnh hưởng mạnh nhất;
- một thử nghiệm tuần tới.

## Output bắt buộc

Khi setup đầu ngày:

```markdown
## Check-in năng lượng hôm nay

| Chỉ số | Giá trị |
|---|---|
| Năng lượng hiện tại |  |
| Chất lượng ngủ |  |
| Cảm xúc nền |  |
| MIT hôm nay |  |

## Thói quen lõi

| Thói quen | Bản tối thiểu | Trạng thái |
|---|---|---|

## Điều cần giữ năng lượng

- 

## Điều cần tránh

- 
```

Khi review cuối ngày:

```markdown
## Pattern năng lượng

- Tăng năng lượng:
- Tụt năng lượng:
- Mô thức đáng chú ý:

## Thói quen

| Thói quen | Trạng thái | Nhận xét |
|---|---|---|

## Điều chỉnh ngày mai

1. 
```

## Nơi lưu nếu có tạo file

Nếu sếp yêu cầu lưu ngày:

```text
2. Tinh Lọc/Nhật Ký Ngày/
```

Nếu tạo tracker hoặc template mới, lưu tại:

```text
5. Hộp Công Cụ/Template/
```

Nếu tổng hợp tuần:

```text
2. Tinh Lọc/Tổng Kết Tuần/
```

## Sau khi hoàn thành

Kết thúc bằng:

1. mức năng lượng chính hôm nay;
2. pattern đáng chú ý;
3. một điều chỉnh nhỏ cho ngày mai.
