---
name: mindmirror-tao-phuong-phap-template-skill
description: Tạo trọn bộ phương pháp luận, template và skill vận hành từ một tiêu đề duy nhất trong MindMirror Vault. Dùng khi user nói "tạo phương pháp luận + template + skill", "đóng gói quy trình thành template và skill", "chỉ đưa tiêu đề rồi tự tạo bộ framework/template/skill", hoặc muốn biến một ý tưởng/quy trình thành tài sản tái dùng có skill đính kèm trong template.
---

# MindMirror — Tạo Phương Pháp + Template + Skill

## Mục tiêu

Từ một **tiêu đề** do user đưa, tạo trọn bộ tài sản tái dùng trong MindMirror:

```text
Tiêu đề
→ Phương pháp luận / Framework
→ Template tương ứng
→ Skill vận hành template
→ Gắn skill ngược vào template
```

Kết quả cuối cùng phải được lưu vào vault. Final response chỉ cần báo đường dẫn template và skill đã tạo.

## Nguồn bắt buộc phải đọc

Trước khi tạo file:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. Nếu chủ đề liên quan business, sales, marketing, sản phẩm hoặc MindMirror Template: đọc `6. OPC Company 2Brain/CLAUDE.md`

## Đầu vào tối thiểu

User chỉ cần đưa:

```text
Tiêu đề: [Tên phương pháp / quy trình / template muốn tạo]
```

Nếu tiêu đề quá mơ hồ, hỏi tối đa 3 câu:

1. Bộ này dùng cho ai?
2. Kết quả cuối cùng người dùng cần nhận là gì?
3. Dùng hằng ngày, hằng tuần, theo dự án hay theo buổi phỏng vấn?

Nếu có thể suy luận an toàn từ bối cảnh, không hỏi; ghi rõ `Giả định của em:`.

## Quy tắc đặt tên

Từ tiêu đề gốc, tạo:

```text
Tên framework: Framework - [Tiêu đề].md
Tên template: Template - [Tiêu đề].md
Tên skill: mindmirror-[slug-tieu-de]
```

Slug skill:

- lowercase ASCII
- bỏ dấu tiếng Việt
- chỉ dùng chữ, số, dấu gạch ngang
- tối đa 64 ký tự
- ưu tiên động từ hoặc cụm rõ hành động

Ví dụ:

```text
Tiêu đề: Khởi Động Ngày Theo La Bàn 365
Skill: mindmirror-khoi-dong-ngay-la-ban-365
```

## Nơi lưu mặc định

Nếu chủ đề thuộc project hiện hành hoặc user đưa đường dẫn, lưu cùng project đó.

Nếu không có project rõ:

```text
Framework: 3. Chuyển Hoá/Tri Thức/Framework/
Template: 5. Hộp Công Cụ/Template/
Canonical skill: .claude/skills/[skill-name]/SKILL.md
Adapter Codex: .agents/skills/[skill-name]/SKILL.md
```

Template và framework sinh ra từ skill này lưu tại:

```text
5. Hộp Công Cụ/Template/
3. Chuyển Hoá/Tri Thức/Framework/
```

## Cấu trúc Framework cần tạo

Framework note phải có:

```yaml
---
up:
  - "[[Tên MOC hoặc Project MOC liên quan]]"
created: YYYY-MM-DD
loai: framework
tags: [chuyen-hoa, framework]
source:
---
```

Nội dung:

```text
# Framework - [Tiêu đề]

## Mục đích
## Khi nào dùng
## Nguyên tắc lõi
## Thành phần
## Quy trình từng bước
## Output chuẩn
## Ví dụ
## Giới hạn
## Liên kết
```

Framework phải giải thích được **phương pháp luận**, không chỉ là checklist.

## Cấu trúc Template cần tạo

Template note phải có:

```yaml
---
loai: template
framework: "[[Framework - [Tiêu đề]]]"
skill: [skill-name]
created: YYYY-MM-DD
tags: [template, skill-ready]
up:
  - "[[Tên MOC hoặc Project MOC liên quan]]"
---
```

Ngay đầu template phải có callout:

```markdown
> [!important] Skill đi kèm
> Template này được đóng gói với skill `[skill-name]`.
```

Template phải có:

```text
## 0. Skill vận hành
## 1. Cách dùng với AI
## 2. Dữ liệu đầu vào
## 3. AI xử lý / phân tích
## 4. Output chính
## 5. Checklist hoàn thành
## 6. Review / cải tiến
## 7. Output chuẩn AI phải trả về
```

Nếu template là cho lập kế hoạch/phỏng vấn/ngày/tuần, bổ sung bảng câu hỏi. Nếu là cho content/sales/delivery, bổ sung các trường đầu vào, tiêu chí chất lượng và CTA/handoff phù hợp.

## Cấu trúc Skill vận hành cần tạo

Canonical skill:

```text
.claude/skills/[skill-name]/SKILL.md
```

Adapter:

```text
.agents/skills/[skill-name]/SKILL.md
```

Canonical `SKILL.md` chỉ dùng frontmatter `name` và `description`.

Nội dung canonical phải có:

```text
# [Tên Skill]

## Mục tiêu
## Nguồn bắt buộc phải đọc
## Đầu vào tối thiểu
## Nếu thiếu dữ liệu
## Quy trình
## Output bắt buộc
## Nơi lưu nếu có tạo file
## Sau khi hoàn thành
```

Adapter chỉ trỏ về canonical, không duplicate logic:

```text
Workflow chuẩn nằm tại:
../../../.claude/skills/[skill-name]/SKILL.md
```

Nếu tạo `.agents/skills/[skill-name]` bị sandbox chặn, dùng escalation đúng chính sách để tạo folder adapter.

## Quy trình thực hiện

1. Chuẩn hóa tiêu đề và skill slug.
2. Xác định nơi lưu framework/template theo bối cảnh.
3. Tạo framework note.
4. Tạo template note, gắn `skill:` trong frontmatter và callout "Skill đi kèm".
5. Tạo canonical skill trong `.claude/skills/[skill-name]/SKILL.md`.
6. Tạo adapter trong `.agents/skills/[skill-name]/SKILL.md`.
7. Nếu có MOC/project hub liên quan, cập nhật thêm link tới framework/template/skill.
8. Chạy validate nếu có thể:

```text
python3 scripts/quick_validate.py .claude/skills/[skill-name]
```

9. Final response chỉ báo:
   - Template đã tạo
   - Skill đã tạo
   - Câu gọi skill

## Tiêu chuẩn chất lượng

- Template phải tự mô tả đủ để AI đọc vào biết dùng skill nào.
- Skill phải dùng được ngay chỉ từ tiêu đề hoặc dữ liệu tối thiểu.
- Không tạo file mồ côi: framework/template phải link MOC/project nếu có.
- Không tạo README hoặc tài liệu phụ ngoài `SKILL.md` trừ khi thật sự cần.
- Không ghi đè file có sẵn nếu chưa đọc nội dung trước.
