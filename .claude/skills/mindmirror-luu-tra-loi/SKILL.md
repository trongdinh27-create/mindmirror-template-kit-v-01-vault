---
name: mindmirror-luu-tra-loi
description: "Lưu một câu trả lời AI vào Second Brain: capture câu trả lời, giữ câu hỏi gốc/bối cảnh, tạo note trong Thu Thập và gợi ý bước xử lý tiếp theo."
---

# MindMirror - Lưu Một Câu Trả Lời AI Vào Second Brain

## Mục tiêu

Chuyển một câu trả lời AI có giá trị thành note trong MindMirror Vault mà không cần copy-paste thủ công.

Mặc định đây là bước Thu Thập: capture trước, xử lý sâu sau. Skill phải giữ được câu hỏi gốc hoặc bối cảnh để câu trả lời không trở thành một mẩu thông tin rời rạc.

## Nguồn bắt buộc phải đọc

Trước khi thực hiện:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `5. Hộp Công Cụ/Template/Template - Lưu Một Câu Trả Lời AI Vào Second Brain.md`
5. `3. Chuyển Hoá/Tri Thức/Framework/Framework - Lưu Một Câu Trả Lời AI Vào Second Brain.md`

## Đầu vào tối thiểu

Sếp chỉ cần nói:

```text
Lưu câu trả lời này vào Second Brain.
```

Nếu có thêm dữ liệu, nhận:

- câu trả lời AI cần lưu;
- câu hỏi/prompt gốc;
- lý do đáng lưu;
- chủ đề chính;
- tầng lưu mong muốn;
- bước xử lý tiếp theo.

## Nếu thiếu dữ liệu

Nếu sếp chỉ nói "lưu câu trả lời này" mà không paste nội dung, tự suy ra nội dung từ câu trả lời AI ngay trước đó trong conversation hiện tại.

Nếu không thể xác định câu trả lời cần lưu, hỏi đúng 1 câu:

```text
Sếp muốn em lưu câu trả lời nào? Sếp dán lại nội dung cần lưu giúp em nhé.
```

## Quy trình

### Bước 1. Xác định nội dung cần lưu

Nếu sếp paste nội dung cụ thể, dùng nội dung đó. Nếu sếp nói "câu trả lời ngay phía trên", dùng câu trả lời ngay trước đó.

### Bước 2. Xác định bối cảnh

Ghi lại:

- câu hỏi gốc nếu có;
- chủ đề chính;
- lý do đáng lưu nếu có thể suy luận.

Không bịa câu hỏi gốc nếu không có dữ liệu. Nếu thiếu, ghi là `Chưa rõ trong conversation`.

### Bước 3. Tóm gọn nội dung

Tóm gọn câu trả lời thành bản lưu trữ dễ đọc:

- giữ insight chính;
- giữ framework/quy trình nếu có;
- bỏ ví dụ thừa;
- không làm sai nghĩa gốc.

### Bước 4. Tạo slug

Tạo slug tiếng Việt 4-8 từ mô tả chủ đề chính.

Ví dụ:

```text
AI và vai trò trong Second Brain
```

### Bước 5. Tạo file Thu Thập

Tạo file tại:

```text
1. Thu Thập/FN — {slug} — {YYYY-MM-DD}.md
```

Nếu file đã tồn tại, thêm hậu tố ngắn hoặc đọc trước để tránh ghi đè.

### Bước 6. Viết note

```markdown
---
created: {YYYY-MM-DD}
tags: [raw, fleeting, ai-answer]
status: unprocessed
source: "{câu hỏi gốc hoặc bối cảnh}"
---

# FN — {slug} — {YYYY-MM-DD}

## Câu hỏi gốc

{câu hỏi/prompt gốc nếu có}

## Câu trả lời AI đã lưu

{nội dung câu trả lời được tóm gọn, giữ ý chính}

## Vì sao đáng lưu

{1-3 câu nếu suy luận được}

## Gợi ý xử lý tiếp

{skill hoặc hành động phù hợp}

#process-later
```

### Bước 7. Gợi ý bước xử lý tiếp

Chọn một gợi ý:

- `mindmirror-xu-ly`: nếu muốn đi qua Thu Thập → Tinh Lọc → Chuyển Hoá → Kiến Tạo.
- `mindmirror-chuyen-suy-nghi-thanh-kien-thuc-cot-loi`: nếu câu trả lời chứa luận điểm mạnh.
- `mindmirror-tao-phuong-phap-template-skill`: nếu câu trả lời ẩn một quy trình có thể đóng gói.
- Giữ `#process-later`: nếu chỉ cần capture.

## Output bắt buộc

Sau khi lưu, trả về:

```markdown
Đã lưu vào:
[đường dẫn file]

Tóm tắt nội dung đã lưu:
[3-5 dòng]

Gợi ý xử lý tiếp:
[skill/hành động]
```

## Nơi lưu nếu có tạo file

Mặc định:

```text
1. Thu Thập/
```

Framework/template của workflow nằm trong:

```text
5. Hộp Công Cụ/Template/
3. Chuyển Hoá/Tri Thức/Framework/
```

## Sau khi hoàn thành

Kết thúc bằng:

1. file đã lưu;
2. nội dung chính đã capture;
3. bước xử lý tiếp theo.
