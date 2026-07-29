---
name: mindmirror-chuyen-suy-nghi-thanh-kien-thuc-cot-loi
description: "Chuyển một đoạn suy nghĩ thô thành Kiến Thức Cốt Lõi: tìm luận điểm, đặt tiêu đề statement, viết note core, gợi ý MOC và wikilink liên quan."
---

# MindMirror - Chuyển Suy Nghĩ Thành Kiến Thức Cốt Lõi

## Mục tiêu

Giúp sếp chuyển một đoạn suy nghĩ thô thành một hoặc nhiều **Kiến Thức Cốt Lõi** đúng chuẩn MindMirror:

- tiêu đề là câu khẳng định hoàn chỉnh;
- có quan điểm cá nhân;
- có bối cảnh, bằng chứng và ứng dụng;
- có `up:` và wikilink liên quan;
- lưu đúng tầng Chuyển Hoá khi sếp yêu cầu.

## Nguồn bắt buộc phải đọc

Trước khi thực hiện:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `5. Hộp Công Cụ/Template/Template - Chuyển Một Đoạn Suy Nghĩ Thành Kiến Thức Cốt Lõi.md`
5. `3. Chuyển Hoá/Tri Thức/Framework/Framework - Chuyển Một Đoạn Suy Nghĩ Thành Kiến Thức Cốt Lõi.md`

Khi chuẩn bị lưu note core, scan thêm:

- `3. Chuyển Hoá/Bản Đồ/`
- `3. Chuyển Hoá/Tri Thức/Kiến Thức Cốt Lõi/`
- `3. Chuyển Hoá/Tri Thức/Framework/`

## Đầu vào tối thiểu

Sếp chỉ cần đưa:

```text
Đoạn suy nghĩ: [nội dung thô]
```

Nếu có thêm, nhận thêm:

- nguồn/bối cảnh;
- chủ đề;
- mục tiêu dùng lại;
- muốn tạo 1 note hay nhiều note;
- muốn lưu ngay hay chỉ draft.

## Nếu thiếu dữ liệu

Nếu chưa có đoạn suy nghĩ, hỏi:

1. Anh muốn chuyển đoạn suy nghĩ nào thành Kiến Thức Cốt Lõi?
2. Suy nghĩ đó xuất hiện từ trải nghiệm, nhật ký, sách/video hay cuộc trò chuyện?
3. Anh muốn em lưu luôn hay chỉ tạo bản draft để anh duyệt?

Nếu đã có đoạn suy nghĩ nhưng thiếu bối cảnh, vẫn xử lý được. Ghi rõ:

```text
Giả định của em:
- source tạm để là "Suy nghĩ cá nhân";
- MOC sẽ được gợi ý dựa trên nội dung và có thể cần xác nhận lại.
```

## Quy trình

### Bước 1. Đọc và giữ nguyên tinh thần

Không làm mất sắc thái cá nhân trong đoạn suy nghĩ. Không biến thành văn chung chung.

### Bước 2. Tách ý chính

Trả lời:

- Sếp đang thật sự nói điều gì?
- Luận điểm ngầm là gì?
- Có bao nhiêu ý độc lập?
- Ý nào đủ mạnh để thành Kiến Thức Cốt Lõi?

### Bước 3. Đề xuất candidate statement

Đề xuất 1-3 tiêu đề Kiến Thức Cốt Lõi.

Quy tắc bắt buộc:

- là câu khẳng định hoàn chỉnh;
- có chủ ngữ và vị ngữ;
- thể hiện quan điểm;
- không phải tên chủ đề;
- không quá mơ hồ.

### Bước 4. Đánh giá độ chín

Phân loại:

- `Đủ chín`: có thể tạo note core.
- `Cần Tinh Lọc thêm`: cần hỏi thêm hoặc lưu ở Kiến Thức Nguồn trước.
- `Chỉ nên lưu Nhật Ký Ngày`: chủ yếu là cảm xúc/bối cảnh cá nhân nhất thời.

### Bước 5. Viết note core đề xuất

Dùng cấu trúc:

```markdown
---
up:
  - "[[MOC liên quan]]"
created: YYYY-MM-DD
tags: [statement, core]
source: "[[Nguồn hoặc bối cảnh]]"
---

# [Câu khẳng định hoàn chỉnh]

## Luận điểm

## Vì sao điều này quan trọng

## Bối cảnh / nguồn gốc

## Ví dụ / bằng chứng

## Ứng dụng

## Câu hỏi mở

## Liên kết

- 
- 
```

### Bước 6. Gợi ý MOC và link liên quan

Trước khi lưu, dùng `rg` để tìm note liên quan trong:

```text
3. Chuyển Hoá/Bản Đồ/
3. Chuyển Hoá/Tri Thức/Kiến Thức Cốt Lõi/
3. Chuyển Hoá/Tri Thức/Framework/
```

Nếu tìm được link chắc, thêm vào note. Nếu chưa chắc, ghi là `Gợi ý cần xác nhận`, không bịa wikilink.

### Bước 7. Lưu file nếu được yêu cầu

Nếu sếp nói lưu/tạo file/đưa vào vault, tạo file tại:

```text
3. Chuyển Hoá/Tri Thức/Kiến Thức Cốt Lõi/[Câu khẳng định hoàn chỉnh].md
```

Nếu file đã tồn tại, đọc trước rồi hỏi hoặc đề xuất merge; không ghi đè.

### Bước 8. Gợi ý bước tiếp theo

Sau khi tạo note, gợi ý:

- có cần dùng `mindmirror-goi-y-lien-ket` để tăng liên kết không;
- có cần dùng `mindmirror-tinh-chinh-moc` để đưa note vào curated section không;
- có thể biến luận điểm thành content/framework/template/skill không.

## Output bắt buộc

Nếu chưa lưu file:

```markdown
## Đánh giá độ chín

- Trạng thái:
- Lý do:

## Candidate Kiến Thức Cốt Lõi

1. 
2. 
3. 

## Note đề xuất

[Markdown note đầy đủ]

## Cần sếp xác nhận

- 
```

Nếu đã lưu file:

```markdown
✅ Đã tạo Kiến Thức Cốt Lõi

- File:
- Statement:
- MOC:
- Link liên quan:
- Bước tiếp theo:
```

## Nơi lưu nếu có tạo file

Kiến Thức Cốt Lõi:

```text
3. Chuyển Hoá/Tri Thức/Kiến Thức Cốt Lõi/
```

Nếu suy nghĩ chưa đủ chín:

```text
2. Tinh Lọc/Kiến Thức Nguồn/
```

Nếu chỉ là dữ liệu sống trong ngày:

```text
2. Tinh Lọc/Nhật Ký Ngày/
```

Framework/template của workflow này nằm trong:

```text
5. Hộp Công Cụ/Template/
3. Chuyển Hoá/Tri Thức/Framework/
```

## Sau khi hoàn thành

Kết thúc bằng:

1. statement tốt nhất;
2. file đã tạo hoặc lý do chưa tạo;
3. một bước tiếp theo để dùng lại tri thức này.
