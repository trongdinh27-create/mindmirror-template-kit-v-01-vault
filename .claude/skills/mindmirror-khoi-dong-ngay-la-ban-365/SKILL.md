---
name: mindmirror-khoi-dong-ngay-la-ban-365
description: Thiết lập mục tiêu đầu ngày theo Template Khởi Động Ngày Theo La Bàn 365. Dùng khi user muốn lập kế hoạch hôm nay, chọn MIT, bám sát mục tiêu năm/tháng/tuần, hoặc gọi "khởi động ngày", "thiết lập mục tiêu đầu ngày", "lập kế hoạch ngày theo La Bàn 365".
---

# MindMirror — Khởi Động Ngày Theo La Bàn 365

## Mục tiêu

Skill này đọc bối cảnh mục tiêu lớn và thiết lập kế hoạch **trong ngày** theo chuỗi:

```text
Mục tiêu năm → Kết quả tháng → Cam kết tuần → Kết quả ngày → MIT hôm nay
```

Đầu ra phải giúp người dùng biết hôm nay cần làm gì để bám sát mục tiêu lớn, không tạo danh sách việc rời rạc.

## Nguồn bắt buộc phải đọc

Trước khi thiết lập mục tiêu ngày, đọc các file sau nếu tồn tại:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `6. OPC Company 2Brain/CLAUDE.md` nếu ngày hôm nay liên quan doanh thu, sản phẩm, marketing, sale hoặc MindMirror business.
5. Template nguồn:
   `5. Hộp Công Cụ/Template/Template - Khởi Động Ngày Theo La Bàn 365.md`
6. Framework nguồn:
   `3. Chuyển Hoá/Tri Thức/Framework/Framework - Khởi Động Ngày Theo La Bàn 365.md`

Nếu template hoặc framework không tồn tại, tìm bản gần nhất bằng tên file.

## Khi bắt đầu

Bắt đầu bằng một câu ngắn:

```text
Em sẽ khởi động ngày cho anh theo La Bàn 365: nối việc hôm nay ngược lên mục tiêu năm, rồi chọn 1 MIT thật đáng làm.
```

Nếu thiếu dữ liệu, hỏi tối đa 5 câu. Không hỏi dài. Ưu tiên các câu sau:

1. Mục tiêu năm hoặc mục tiêu lớn hiện tại là gì?
2. Kết quả tháng này cần đạt là gì?
3. Cam kết quan trọng nhất tuần này là gì?
4. Hôm nay anh có bao nhiêu giờ làm sâu thật sự?
5. Năng lượng hôm nay là cao, vừa hay thấp? Có lịch cố định/deadline nào không?

Nếu người dùng đã cung cấp đủ dữ liệu, không hỏi lại; tự lập kế hoạch.

## Quy trình

### Bước 1 — Xác định la bàn hôm nay

Điền rõ:

```text
Mục tiêu năm:
Kết quả tháng:
Cam kết tuần:
Kết quả ngày:
```

Kết quả ngày phải là một đầu ra cụ thể, có thể kiểm tra trong hôm nay.

### Bước 2 — Kiểm tra bối cảnh thực tế

Luôn xét:

- Năng lượng hôm nay: cao / vừa / thấp.
- Giờ làm sâu thật sự.
- Lịch cố định.
- Deadline gần nhất.
- Việc tồn từ hôm qua.
- Ràng buộc sức khỏe/cảm xúc nếu có.

Nếu năng lượng thấp, giảm phạm vi MIT nhưng vẫn giữ kết quả thật.

### Bước 3 — Chọn 1 MIT

Chỉ chọn **1 MIT — Most Important Task**.

Công thức MIT:

```text
[Động từ cụ thể] + [đầu ra] + [phạm vi] + [thời lượng] + [khung giờ]
```

MIT phải nối được lên cam kết tuần và mục tiêu lớn.

### Bước 4 — Chọn việc phụ

Chỉ chọn 2-5 việc phụ. Mỗi việc phụ phải có:

- Động từ cụ thể.
- Đầu ra rõ.
- Nhóm việc: Deep Work / Admin / Giao tiếp / Review.
- Thời lượng dự kiến.

Không để việc phụ ăn mất MIT.

### Bước 5 — Tạo block thời gian

Phân bổ theo năng lượng:

- Việc quan trọng/Deep Work vào block năng lượng cao.
- Admin/giao tiếp vào block năng lượng thấp hơn.
- Review cuối ngày 10-15 phút.

### Bước 6 — Chặn lệch hướng

Luôn có mục:

```text
Điều cần tránh hôm nay:
```

Gợi ý tránh:

- Làm việc dễ trước để né MIT.
- Thêm tính năng mới khi việc cần là bán/ra mắt.
- Nhảy sang ý tưởng mới chưa liên quan mục tiêu năm.
- Chat/họp làm vỡ block làm sâu.
- Học thêm thay vì xuất bản/gửi/bán.

### Bước 7 — Review và handoff

Cuối output phải có câu hỏi review:

- Kết quả thật hôm nay là gì?
- MIT có hoàn thành không?
- Mục tiêu năm tiến thêm ở điểm nào?
- Điều gì làm tôi lệch hướng?
- Việc đầu tiên ngày mai là gì?

## Output bắt buộc

Trả về theo format:

```text
## La bàn hôm nay
- Mục tiêu năm:
- Kết quả tháng:
- Cam kết tuần:
- Kết quả ngày:

## MIT
- [ ] [Việc quan trọng nhất] — [đầu ra] — [thời lượng] — [khung giờ]

## Việc phụ
- [ ] [Việc phụ 1] — [nhóm việc] — [đầu ra] — [thời lượng]
- [ ] [Việc phụ 2] — [nhóm việc] — [đầu ra] — [thời lượng]
- [ ] [Việc phụ 3] — [nhóm việc] — [đầu ra] — [thời lượng]

## Block thời gian
- [Giờ] — [Việc]
- [Giờ] — [Việc]
- [Giờ] — Review cuối ngày

## Điều cần tránh
- 

## Review cuối ngày
- Kết quả thật hôm nay là gì?
- MIT có hoàn thành không?
- Mục tiêu năm tiến thêm ở điểm nào?
- Việc đầu tiên ngày mai là gì?
```

## Lưu vào Daily Note nếu được yêu cầu

Nếu user yêu cầu lưu, cập nhật daily note tương ứng trong:

```text
2. Tinh Lọc/Nhật Ký Ngày/
```

hoặc vị trí Daily Note hiện hành trong vault. Không tạo note mồ côi; link về mục tiêu/kế hoạch liên quan nếu có.
