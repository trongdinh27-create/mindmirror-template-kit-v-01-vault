---
name: mindmirror-rut-bai-hoc-tu-chuyen-vua-xay-ra
description: "Rút bài học từ một chuyện vừa xảy ra: tách sự thật khỏi diễn giải, gọi tên cảm xúc, tìm mô thức, chốt hành động lần sau và gợi ý tài sản nên tạo trong Second Brain."
---

# MindMirror - Rút Bài Học Từ Một Chuyện Vừa Xảy Ra

## Mục tiêu

Giúp sếp biến một sự kiện vừa xảy ra trong công việc hoặc cuộc sống thành:

- bài học cốt lõi;
- hành động lần sau;
- nhận diện mô thức cá nhân;
- gợi ý nơi lưu hoặc tài sản nên tạo tiếp trong MindMirror.

AI được quyền phỏng vấn và phản chiếu, nhưng không được kết luận thay sếp rằng bài học nào là "chân lý cuối cùng".

## Nguồn bắt buộc phải đọc

Trước khi thực hiện:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `5. Hộp Công Cụ/Template/Template - Rút Bài Học Từ Một Chuyện Vừa Xảy Ra.md`
5. `3. Chuyển Hoá/Tri Thức/Framework/Framework - Rút Bài Học Từ Một Chuyện Vừa Xảy Ra.md`

Nếu chuyện liên quan sprint template của bạn, đọc thêm:

- `5. Hộp Công Cụ/Danh Mục Kỹ Năng AI/MOC — Bộ Template Và Skill MindMirror.md`

## Đầu vào tối thiểu

Sếp chỉ cần đưa:

```text
Chuyện vừa xảy ra: [mô tả tự nhiên]
```

Nếu có thêm thông tin thì càng tốt:

- bối cảnh;
- người liên quan;
- cảm xúc;
- kết quả;
- điều sếp đang băn khoăn;
- sếp muốn lưu vào nhật ký, note riêng hay chỉ trả lời trong chat.

## Nếu thiếu dữ liệu

Nếu sếp chỉ nói "rút bài học từ một chuyện vừa xảy ra" mà chưa kể chuyện, hỏi tối đa 5 câu:

1. Chuyện gì vừa xảy ra?
2. Điều gì trong chuyện đó làm anh thấy cần dừng lại để rút bài học?
3. Cảm xúc nổi bật nhất của anh lúc đó là gì?
4. Anh nghĩ mình đã làm đúng/chưa đúng ở điểm nào?
5. Lần sau anh muốn khác đi điều gì?

Nếu sếp đã kể đủ để xử lý, không hỏi thêm quá nhiều. Có thể ghi rõ:

```text
Giả định của em:
- ...
```

## Quy trình

### Bước 1. Tóm tắt sự kiện

Tóm tắt chuyện vừa xảy ra trong 3-5 dòng, giữ trung lập, không phán xét.

### Bước 2. Tách sự thật khỏi diễn giải

Tạo bảng:

| Sự thật quan sát được | Diễn giải / giả định |
|---|---|

Chỉ đưa vào cột sự thật những điều có thể quan sát, đọc, nghe hoặc xác nhận.

### Bước 3. Gọi tên cảm xúc và tín hiệu

Nêu cảm xúc nổi bật và tín hiệu hành vi/cơ thể nếu có:

- cảm xúc;
- phản ứng;
- điều bị kích hoạt;
- nhu cầu hoặc giá trị có thể đang bị chạm vào.

Không chẩn đoán tâm lý. Chỉ phản chiếu như một giả thuyết mềm.

### Bước 4. Tìm mô thức

Xem chuyện này có thể thuộc mô thức nào:

- vội vàng tối ưu trước khi xác nhận chiến lược;
- nói "có" quá nhanh;
- né việc khó;
- thiếu ranh giới;
- cầu toàn;
- không làm rõ input;
- để cảm xúc quyết định nhịp hành động;
- hoặc một mô thức khác rút ra từ dữ liệu sếp cung cấp.

### Bước 5. Rút bài học cốt lõi

Viết bài học bằng 1 câu theo mẫu:

```text
Khi [tình huống], anh cần nhớ [nguyên tắc], để [kết quả mong muốn].
```

Nếu có nhiều bài học, chọn 1 bài học chính và tối đa 2 bài học phụ.

### Bước 6. Chốt hành động lần sau

Đưa ra 1-3 hành động cụ thể:

- việc làm ngay;
- câu hỏi cần hỏi lần sau;
- checklist nhỏ;
- ranh giới cần đặt;
- nhắc nhở cần đưa vào template/quy trình.

### Bước 7. Gợi ý tài sản nên tạo

Phân loại:

- `Nhật ký ngày`: nếu đây chủ yếu là cảm xúc/trải nghiệm trong ngày.
- `Note bài học`: nếu bài học có thể dùng lại.
- `Kiến Thức Cốt Lõi`: nếu bài học là nguyên tắc sống/làm việc có tính bền.
- `Content`: nếu câu chuyện có thể dạy người khác.
- `Quy trình/Template/Skill`: nếu đây là việc lặp lại và có thể hệ thống hóa.

Không tự tạo file phụ nếu sếp chưa yêu cầu lưu, trừ khi yêu cầu hiện tại nói rõ "lưu vào vault".

## Output bắt buộc

Trả về đúng cấu trúc:

```markdown
## Bài học rút ra

[1 câu súc tích]

## Chuyện vừa xảy ra

[Tóm tắt 3-5 dòng]

## Sự thật vs diễn giải

| Sự thật | Diễn giải/giả định |
|---|---|
|  |  |

## Cảm xúc / tín hiệu

- 

## Mô thức

- 

## Hành động lần sau

1. 
2. 
3. 

## Nên lưu thành gì?

- 

## Link liên quan

- 
```

Nếu dữ liệu quá ít, output vẫn được phép có mục `Câu hỏi cần hỏi thêm` ở cuối.

## Nơi lưu nếu có tạo file

Nếu sếp yêu cầu lưu:

- Nếu là ghi nhận trong ngày: cập nhật daily note theo quy ước vault.
- Nếu là bài học riêng: tạo note trong `2. Tinh Lọc/Kiến Thức Nguồn/` với tên:

```text
Bài học từ [tên chuyện ngắn] — YYYY-MM-DD.md
```

- Nếu bài học dẫn tới một template/framework mới: lưu hoặc link về:

```text
5. Hộp Công Cụ/Template/
3. Chuyển Hoá/Tri Thức/Framework/
```

- Nếu bài học đủ mạnh để thành nguyên tắc, đề xuất nâng cấp thành Kiến Thức Cốt Lõi thay vì tự động tạo khi chưa được xác nhận.

## Sau khi hoàn thành

Kết thúc bằng 3 dòng ngắn:

1. Bài học quan trọng nhất.
2. Hành động lần sau.
3. Đề xuất lưu/tái dùng tiếp theo.
