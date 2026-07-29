---
name: mindmirror-tong-hop-sau-buoi-coaching
description: "Tổng hợp sau buổi coaching từ transcript/audio/note thô: rút nội dung chính, vấn đề cốt lõi, nhận ra của học viên, cam kết, bài tập về nhà, action items, owner, deadline và bước tiếp theo."
---

# MindMirror — Tổng Hợp Sau Buổi Coaching

## Mục tiêu

Từ transcript, audio hoặc note thô sau một buổi coaching, tạo bản tổng hợp rõ ràng để học viên/khách hàng biết mình đã nhận ra gì, đã cam kết gì, cần làm bài tập nào và buổi sau sẽ đi tiếp ra sao.

## Nguồn bắt buộc phải đọc

Trước khi xử lý:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. Nếu liên quan học viên/khách hàng/doanh nghiệp: đọc thêm `6. OPC Company 2Brain/CLAUDE.md`
5. Template gắn với skill: `5. Hộp Công Cụ/Template/Template - Tổng Hợp Sau Buổi Coaching.md`

Nếu input có tên học viên/khách hàng và vault đã có hồ sơ liên quan, đọc thêm hồ sơ đó trước khi kết luận.

## Đầu vào tối thiểu

User có thể đưa:

- transcript;
- audio;
- note thô;
- chat log sau coaching;
- hoặc tên học viên + ghi chú ngắn.

Cần biết tối thiểu:

1. Tên học viên/khách hàng nếu có.
2. Ngày hoặc bối cảnh buổi coaching nếu có.
3. Nội dung thô để phân tích.

## Nếu thiếu dữ liệu

Hỏi tối đa 3 câu:

1. Đây là buổi coaching với ai?
2. Input hiện có là audio, transcript hay note thô?
3. Sếp muốn output chỉ trả trong chat hay lưu thành file trong vault?

Nếu vẫn có đủ dữ liệu để làm preview, cứ làm preview trước và ghi rõ phần còn thiếu.

## Quy trình

### Bước 1 — Xác định nguồn input

- Nếu là transcript/note: đọc và làm sạch vừa đủ.
- Nếu là audio: transcribe trước nếu có công cụ local phù hợp; nếu chưa transcribe được, báo cần transcript hoặc dùng skill phân tích ghi âm liên quan.
- Ghi mức độ tin cậy: cao, vừa hoặc thấp.

### Bước 2 — Nắm bối cảnh

Rút ra:

- học viên/khách hàng là ai;
- buổi coaching xoay quanh chủ đề gì;
- mục tiêu ban đầu là gì;
- trạng thái trước buổi coaching.

### Bước 3 — Nhóm nội dung chính

Gom nội dung thành 3-5 chủ đề chính. Với mỗi chủ đề, tách:

- ý học viên/khách hàng nói;
- điều coach/AI nhận định;
- quote đáng giữ nếu có.

### Bước 4 — Rút vấn đề cốt lõi

Phân tích theo 3 tầng:

| Tầng | Ý nghĩa |
|---|---|
| Bề mặt | Vấn đề họ nói ra |
| Sâu hơn | Hệ quả hoặc pattern đang lặp lại |
| Cốt lõi | Niềm tin, thiếu hệ thống, thiếu kỹ năng, cảm xúc hoặc rào cản chính |

Không kết luận quá chắc nếu không có bằng chứng.

### Bước 5 — Rút nhận ra và cam kết

Ghi lại:

- nhận ra quan trọng;
- thay đổi góc nhìn;
- quyết định nội tâm;
- cam kết cụ thể học viên đã nói hoặc đồng ý.

Nếu không có cam kết rõ, ghi "Chưa có cam kết rõ" và đề xuất câu hỏi follow-up.

### Bước 6 — Tạo bài tập về nhà

Mỗi bài tập cần có:

- tên bài tập;
- lý do bài tập này quan trọng;
- tiêu chí hoàn thành;
- deadline hoặc mốc kiểm tra;
- mức độ ưu tiên.

Bài tập phải bám vào vấn đề cốt lõi, không đưa quá nhiều.

### Bước 7 — Tạo action items

Tách việc của:

- học viên/khách hàng;
- coach;
- team/đối tác nếu có.

Mỗi action item phải có owner, việc cụ thể, deadline nếu có và trạng thái.

### Bước 8 — Đề xuất bước tiếp theo

Đề xuất:

- trọng tâm buổi tiếp theo;
- câu hỏi cần hỏi thêm;
- tài liệu/template/skill nên dùng;
- hồ sơ/note cần cập nhật trong Second Brain.

## Output bắt buộc

Trả về theo cấu trúc:

```markdown
# Tổng hợp sau buổi coaching - [Tên] - YYYY-MM-DD

## 1. Thông tin buổi coaching

## 2. Tóm tắt một câu

## 3. Nội dung chính theo chủ đề

## 4. Vấn đề cốt lõi

## 5. Nhận ra / chuyển hóa của học viên

## 6. Cam kết của học viên

## 7. Bài tập về nhà

## 8. Action items

## 9. Bước tiếp theo

## 10. Cần cập nhật vào Second Brain

## 11. Câu hỏi mở cho buổi sau
```

## Nơi lưu nếu có tạo file

Nếu user yêu cầu lưu, ưu tiên:

```text
4. Kiến Tạo/2. Lĩnh vực/Học Viên/Buổi Học/
```

Tên file:

```text
Tổng hợp coaching — [Tên học viên] — YYYY-MM-DD.md
```

Nếu đây là khách hàng/doanh nghiệp không thuộc nhóm học viên, lưu theo quy ước Business Brain:

- `Meetings/` nếu là buổi tư vấn/sale/discovery có khách thật;
- `People/` hoặc hồ sơ khách hàng nếu cần cập nhật chân dung;
- project/area liên quan nếu buổi coaching phục vụ một dự án cụ thể.

Không tạo file mồ côi: note phải link về người, project, buổi học hoặc MOC liên quan nếu có.

## Sau khi hoàn thành

Trả về ngắn gọn:

```text
Đã tổng hợp sau buổi coaching cho [Tên].

Điểm chính:
- Vấn đề cốt lõi:
- Cam kết:
- Bài tập về nhà:
- Bước tiếp theo:

File đã lưu: [path nếu có]
```

Nếu chưa lưu file, hỏi user có muốn lưu bản tổng hợp vào vault không.
