---
name: mindmirror-ghi-bien-ban-tong-hop-sau-cuoc-hop
description: "Ghi biên bản và tổng hợp sau cuộc họp từ transcript/audio/note thô/chat log: tóm tắt nội dung chính, quyết định đã chốt, điểm chưa chốt, action items, owner, deadline, insight và follow-up."
---

# MindMirror — Ghi Biên Bản Và Tổng Hợp Sau Cuộc Họp

## Mục tiêu

Biến transcript, audio, note thô hoặc chat log sau một cuộc họp thành **biên bản có thể hành động**:

- cuộc họp bàn gì;
- điều gì quan trọng nhất;
- quyết định nào đã chốt;
- điểm nào chưa chốt;
- ai cần làm gì;
- deadline nào cần giữ;
- insight nào đáng lưu;
- bước follow-up tiếp theo là gì.

Skill này là lớp template phổ thông cho người dùng mới. Nếu input là file audio và cần transcribe sâu, dùng hoặc tham chiếu workflow `mindmirror-phan-tich-file-ghi-am`.

## Nguồn bắt buộc phải đọc

Trước khi tạo output hoặc lưu file:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `6. OPC Company 2Brain/CLAUDE.md` nếu cuộc họp liên quan công ty, đội nhóm, sản phẩm, sale/marketing hoặc MindMirror Template
5. `3. Chuyển Hoá/Tri Thức/Framework/Framework - Ghi Biên Bản Và Tổng Hợp Sau Cuộc Họp.md`
6. `5. Hộp Công Cụ/Template/Template - Ghi Biên Bản Và Tổng Hợp Sau Cuộc Họp.md`

Nếu user đưa meeting brief, project, people, company hoặc note liên quan, đọc thêm trước khi tổng hợp.

## Đầu vào tối thiểu

User chỉ cần đưa một trong các dạng:

```text
Ghi biên bản cuộc họp này cho anh:
[transcript/note thô]
```

Hoặc:

```text
File audio/transcript:
Tên cuộc họp:
Ngày:
Người tham gia:
```

Nếu thiếu tên/ngày/người tham gia nhưng nội dung vẫn xử lý được, dùng `Chưa rõ` và hỏi bổ sung sau output.

## Nếu thiếu dữ liệu

Hỏi tối đa 5 câu:

1. Input là audio, transcript, note thô hay chat log?
2. Tên cuộc họp là gì?
3. Ngày họp và người tham gia là ai?
4. Cuộc họp thuộc project/bối cảnh nào?
5. Sếp muốn em chỉ trả trong chat hay lưu thành file trong vault?

Nếu user cần nhanh, không hỏi vòng dài; tạo bản biên bản nháp và đánh dấu các trường thiếu.

## Quy trình

### Bước 1. Xác định nguồn vào

Phân loại input:

- **Audio:** cần transcribe trước. Nếu có thể, dùng logic/pipeline trong `mindmirror-phan-tich-file-ghi-am`.
- **Transcript:** phân tích trực tiếp.
- **Note thô:** chuẩn hóa và suy luận thận trọng.
- **Chat log:** giữ người nói nếu có, gom ý theo chủ đề.

Không dựng transcript giả nếu audio chưa được transcribe.

### Bước 2. Làm sạch nguồn vừa đủ

- Giữ đúng ý gốc.
- Không viết lại cho hay đến mức đổi nghĩa.
- Đánh dấu đoạn không chắc: `[không nghe rõ]`, `[chưa chắc tên]`, `[deadline chưa rõ]`.
- Nếu nguồn quá dài, chia theo cụm chủ đề rồi tổng hợp.

### Bước 3. Tạo kết quả chính

Viết 2-5 câu:

- cuộc họp xoay quanh vấn đề gì;
- kết quả lớn nhất là gì;
- điều gì ảnh hưởng tới bước tiếp theo.

### Bước 4. Nhóm nội dung chính

Tạo các chủ đề:

- tên chủ đề;
- ý chính;
- mức độ rõ: `đã rõ / còn mơ hồ / cần hỏi thêm`;
- trích dẫn đáng chú ý nếu có.

### Bước 5. Rút quyết định đã chốt

Chỉ đưa vào `Quyết định đã chốt` khi có căn cứ rõ trong nguồn.

Nếu chưa rõ, đưa vào:

```text
Chưa chốt / cần làm rõ
```

Phân biệt:

- quyết định;
- đề xuất;
- ý tưởng;
- câu hỏi mở.

### Bước 6. Rút action items

Mỗi action item phải có:

- owner;
- việc cần làm;
- deadline;
- phụ thuộc;
- trạng thái.

Nếu thiếu owner/deadline, ghi `Chưa rõ owner` hoặc `Chưa rõ deadline`, không tự gán.

### Bước 7. Rút insight và follow-up

Tách:

- insight đáng giữ;
- câu nói/trích dẫn có giá trị;
- rủi ro;
- cơ hội tạo content/offer/framework/SOP;
- follow-up cần gửi, cần nhắc, cần hẹn.

### Bước 8. Đề xuất lưu hoặc nâng cấp

Nếu nội dung liên quan vận hành công ty, đề xuất lưu vào `Meetings/` theo quy ước Business Brain hoặc `2. Tinh Lọc/Kiến Thức Nguồn/` nếu là biên bản tri thức.

Nếu có insight bền vững, gợi ý dùng:

- `mindmirror-chuyen-suy-nghi-thanh-kien-thuc-cot-loi`
- `mindmirror-rut-bai-hoc-tu-chuyen-vua-xay-ra`
- `mindmirror-tao-phuong-phap-template-skill`
- `mindmirror-cap-nhat-daily-note`

## Output bắt buộc

Trả về bằng tiếng Việt:

```markdown
# Biên bản - [Tên cuộc họp]

## 1. Thông tin cuộc họp

| Trường | Nội dung |
|---|---|
| Ngày/giờ |  |
| Người tham gia |  |
| Bối cảnh/project |  |
| Nguồn input |  |
| Mức độ tin cậy | Cao / vừa / thấp |

## 2. Kết quả chính

## 3. Nội dung chính theo chủ đề

### [Chủ đề 1]
- Ý chính:
- Mức độ rõ:
- Trích dẫn đáng chú ý nếu có:

## 4. Quyết định đã chốt

| Quyết định | Người/nhóm đồng thuận | Lý do/điều kiện |
|---|---|---|

## 5. Chưa chốt / cần làm rõ

| Vấn đề | Cần ai xác nhận? | Ghi chú |
|---|---|---|

## 6. Action items

| Owner | Việc cần làm | Deadline | Phụ thuộc | Trạng thái |
|---|---|---|---|---|

## 7. Insight đáng giữ

## 8. Follow-up

## 9. Đề xuất lưu vào MindMirror
```

Nếu input không đủ tin cậy, thêm:

```markdown
## 10. Giới hạn của biên bản này
```

## Nơi lưu nếu có tạo file

Nếu user yêu cầu lưu:

- Với cuộc họp doanh nghiệp: ưu tiên `Meetings/`.
- Với biên bản tri thức/call cần tinh lọc: dùng `2. Tinh Lọc/Kiến Thức Nguồn/`.
- Nếu thuộc project cụ thể, lưu trong project đó hoặc link về project.

Tên file gợi ý:

```text
YYYY-MM-DD — Biên bản — [Tên cuộc họp].md
```

Frontmatter tối thiểu:

```yaml
---
created: YYYY-MM-DD
type: meeting-note
status: processed
tags: [meeting-note, action-items]
source:
---
```

Không lưu toàn bộ transcript thô vào biên bản trừ khi user yêu cầu.

## Sau khi hoàn thành

Sau khi trả biên bản:

1. Nhắc câu gọi lại skill:

```text
Gọi skill mindmirror-ghi-bien-ban-tong-hop-sau-cuoc-hop để ghi biên bản cuộc họp: [tên cuộc họp]
```

2. Nếu có action items thiếu owner/deadline, nhắc user chốt.
3. Nếu có insight mạnh, đề xuất skill/note nên tạo tiếp.
4. Nếu có tạo file, báo đường dẫn đã lưu.
