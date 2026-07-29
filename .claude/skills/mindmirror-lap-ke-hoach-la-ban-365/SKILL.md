---
name: mindmirror-lap-ke-hoach-la-ban-365
description: Phỏng vấn người dùng theo phương pháp La Bàn 365 để lập kế hoạch mục tiêu năm/tháng/tuần/ngày từ template có sẵn. Dùng khi user muốn lập kế hoạch mục tiêu, bóc mục tiêu lớn thành hành động, hoặc gọi "lập kế hoạch La Bàn 365", "phỏng vấn lập kế hoạch", "tạo kế hoạch năm/tháng/tuần/ngày".
---

# MindMirror — Lập Kế Hoạch La Bàn 365

## Mục tiêu

Skill này biến `Template - La Bàn 365 - Kế Hoạch Mục Tiêu` thành một buổi phỏng vấn có cấu trúc. Sau phỏng vấn, tạo một kế hoạch hoàn chỉnh theo chuỗi:

```text
Mục tiêu năm → Kết quả bàn giao → Quý/Tháng → Sprint tuần → Hành động ngày → Review
```

## Nguồn bắt buộc phải đọc

Trước khi phỏng vấn hoặc lập kế hoạch, đọc các file sau nếu tồn tại:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `6. OPC Company 2Brain/CLAUDE.md` nếu mục tiêu liên quan doanh thu, sản phẩm, marketing, sale hoặc MindMirror business.
5. Template nguồn:
   `5. Hộp Công Cụ/Template/Template - La Bàn 365 - Kế Hoạch Mục Tiêu.md`

Nếu template nguồn không tồn tại, tìm bản gần nhất bằng:

```text
Template - La Bàn 365 - Kế Hoạch Mục Tiêu.md
```

## Khi bắt đầu

Không lập kế hoạch ngay nếu mục tiêu còn mơ hồ. Bắt đầu bằng một câu ngắn:

```text
Em sẽ phỏng vấn anh theo La Bàn 365. Mình đi từ mục tiêu lớn xuống kết quả đo được, rồi mới bóc thành tháng, tuần và ngày.
```

Sau đó hỏi theo từng vòng. Mỗi lượt chỉ hỏi tối đa 5 câu để người dùng dễ trả lời. Nếu người dùng đã cung cấp đủ dữ liệu ở vòng nào, tự đi tiếp vòng sau.

## Vòng phỏng vấn

### Vòng 1 — Làm rõ đích đến

Hỏi:

1. Mục tiêu lớn anh muốn đạt là gì?
2. Thời hạn cụ thể là ngày/tháng/năm nào?
3. Con số hoặc bằng chứng nào chứng minh là đã đạt?
4. Vì sao mục tiêu này quan trọng với anh lúc này?
5. Nếu không làm, cái giá phải trả là gì?

Chuẩn hóa đầu ra:

```text
Mục tiêu:
Thời hạn:
Kết quả đo được:
Ý nghĩa:
Cái giá nếu không làm:
```

### Vòng 2 — Bóc kết quả bàn giao

Hỏi:

1. Cuối kỳ phải có những tài sản/kết quả cụ thể nào?
2. Ai là người nhận hoặc hưởng lợi từ kết quả đó?
3. Kết quả nào tạo doanh thu/chuyển hóa lớn nhất?
4. Kết quả nào phải có trước để các kết quả khác xảy ra?
5. Tiêu chí hoàn thành của từng kết quả là gì?

Phân loại kết quả thành:

- Tài sản: template, framework, landing page, video, tài liệu, dashboard.
- Năng lực: kỹ năng, thói quen, số lần thực chiến.
- Kinh doanh: doanh thu, lead, khách hàng, offer, funnel, case study.
- Đời sống: sức khỏe, năng lượng, quan hệ, tài chính cá nhân.

### Vòng 3 — Chia chặng quý/tháng

Hỏi:

1. Từ nay đến deadline còn bao nhiêu tháng?
2. Giai đoạn đầu tiên cần validate điều gì?
3. Giai đoạn giữa cần scale hoặc chuẩn hóa điều gì?
4. Giai đoạn cuối cần chốt mục tiêu bằng chiến dịch nào?
5. Mỗi tháng chỉ nên có 1-3 kết quả nào?

Nếu mục tiêu là doanh thu, luôn bóc ngược:

```text
Doanh thu cần đạt → Giá bán → Số khách/gói → Lead cần có → Kênh tạo lead → Hoạt động tháng/tuần/ngày
```

### Vòng 4 — Sprint tuần

Hỏi:

1. Tuần đầu tiên cần tạo ra kết quả gì để kế hoạch bắt đầu chạy thật?
2. 3 cam kết tuần là gì?
3. Việc nào nếu hoàn thành sẽ làm tuần này đáng giá?
4. Tuần này có bao nhiêu giờ làm sâu thực tế?
5. Điều gì cần nói không để bảo vệ mục tiêu?

### Vòng 5 — Hành động ngày đầu tiên

Hỏi:

1. Hôm nay hoặc ngày bắt đầu có bao nhiêu giờ làm sâu?
2. Năng lượng hiện tại là cao, vừa hay thấp?
3. Lịch cố định nào không thể dời?
4. Việc tồn nào đang kéo từ hôm trước sang?
5. Nếu chỉ làm một việc hôm nay, việc nào làm mục tiêu tiến thêm thật?

Chọn đúng 1 MIT và 2-5 việc phụ.

## Quy tắc tư vấn

- Không để kế hoạch thành danh sách việc quá dài.
- Mỗi hành động phải có động từ cụ thể, đầu ra rõ, thời lượng dự kiến.
- Luôn có mục "Điều cần nói không".
- Với mục tiêu doanh thu, phải có công thức doanh thu và chỉ số ngược.
- Với mục tiêu lớn hơn 6 tháng, phải chia theo chặng.
- Nếu người dùng trả lời bằng cảm giác hoặc câu chung chung, phản chiếu lại và hỏi thêm để đo được.
- Khi cần đưa giả định, ghi rõ `Giả định của em:`.

## Output cuối cùng

Sau khi đủ dữ liệu, tạo kế hoạch theo cấu trúc:

```text
# Kế hoạch La Bàn 365 — [Tên mục tiêu]

## 0. Định nghĩa mục tiêu
## 1. La bàn năm / đích đến
## 2. Kết quả bàn giao
## 3. Bản đồ quý hoặc chặng
## 4. Bản đồ tháng đầu tiên
## 5. Sprint tuần đầu tiên
## 6. Kế hoạch ngày đầu tiên
## 7. Điều cần nói không
## 8. Dashboard tiến độ
## 9. Prompt vận hành hằng tuần
## 10. Bước tiếp theo ngay bây giờ
```

## Nơi lưu file

Nếu kế hoạch sinh ra template hoặc framework mới, lưu vào:

```text
5. Hộp Công Cụ/Template/
3. Chuyển Hoá/Tri Thức/Framework/
```

Tên file:

```text
Kế hoạch La Bàn 365 — [Tên mục tiêu ngắn] — YYYY-MM-DD.md
```

Bản kế hoạch chính lưu vào:

```text
4. Kiến Tạo/1. Đang Làm/
```

hoặc hỏi người dùng nếu vị trí lưu chưa rõ.

## Sau khi lưu

1. Báo đường dẫn file.
2. Tóm tắt 3 quyết định chiến lược quan trọng nhất.
3. Nêu 1 MIT đầu tiên để bắt đầu.
4. Nhắc người dùng có thể mở `5. Hộp Công Cụ/Danh Mục Kỹ Năng AI/MOC — Bộ Template Và Skill MindMirror.md` để chọn template/skill dùng tiếp.
