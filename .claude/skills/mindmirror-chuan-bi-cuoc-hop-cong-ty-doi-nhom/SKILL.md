---
name: mindmirror-chuan-bi-cuoc-hop-cong-ty-doi-nhom
description: "Chuẩn bị cuộc họp công ty/đội nhóm: làm rõ mục tiêu, người tham gia, agenda, câu hỏi, quyết định cần chốt, tài liệu đọc trước và checklist follow-up."
---

# MindMirror — Chuẩn Bị Cuộc Họp Công Ty, Đội Nhóm

## Mục tiêu

Giúp user chuẩn bị một cuộc họp công ty hoặc đội nhóm sao cho trước khi họp đã rõ:

- cuộc họp tồn tại để tạo output gì;
- ai cần tham gia và vai trò của từng người;
- agenda cần đi theo thứ tự nào;
- câu hỏi nào cần hỏi;
- quyết định nào cần chốt;
- tài liệu/ngữ cảnh nào cần đọc trước;
- sau họp cần có biên bản, action item và follow-up gì.

AI được hỗ trợ phân tích và đề xuất, nhưng không được tự quyết định thay user về mục tiêu chiến lược, người quyết định cuối cùng hoặc quyết định quan trọng.

## Nguồn bắt buộc phải đọc

Trước khi tư vấn hoặc tạo file:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `6. OPC Company 2Brain/CLAUDE.md` nếu cuộc họp liên quan công ty, đội nhóm, sản phẩm, sale/marketing hoặc MindMirror Template
5. `3. Chuyển Hoá/Tri Thức/Framework/Framework - Chuẩn Bị Cho Một Cuộc Họp Công Ty, Đội Nhóm.md`
6. `5. Hộp Công Cụ/Template/Template - Chuẩn Bị Cho Một Cuộc Họp Công Ty, Đội Nhóm.md`

Nếu user đưa project/note/person/company liên quan, đọc thêm các file đó trước khi lập Meeting Brief.

## Đầu vào tối thiểu

User chỉ cần đưa một trong các dạng:

```text
Chuẩn bị cho anh cuộc họp về [chủ đề].
```

Hoặc:

```text
Tên cuộc họp:
Mục tiêu:
Người tham gia:
Bối cảnh:
```

Nếu thiếu dữ liệu nhưng vẫn suy luận được, ghi rõ:

```text
Giả định của em:
- ...
```

## Nếu thiếu dữ liệu

Hỏi tối đa 6 câu, ưu tiên theo thứ tự:

1. Cuộc họp này bàn về việc gì?
2. Sau họp, điều gì phải được chốt/rõ/xong?
3. Ai sẽ tham gia và ai là người quyết định cuối cùng?
4. Có quyết định hoặc câu hỏi nào bắt buộc phải xử lý không?
5. Có note, tài liệu, project hoặc cuộc họp cũ nào cần em đọc trước không?
6. Sếp muốn em chỉ trả lời trong chat hay lưu thành một note chuẩn bị họp trong vault?

Nếu user muốn làm nhanh, có thể dùng dữ liệu hiện có và đánh dấu các phần còn thiếu là `Cần bổ sung`.

## Quy trình

### Bước 1. Xác định loại họp

Phân loại cuộc họp thành một loại chính:

- cập nhật tiến độ;
- ra quyết định;
- lập kế hoạch;
- review/retro;
- xử lý vấn đề;
- 1:1;
- brainstorming có đầu ra;
- kickoff.

Nếu cuộc họp có nhiều loại, chọn loại chi phối output chính và ghi loại phụ.

### Bước 2. Làm rõ output sau họp

Viết lại mục tiêu cuộc họp theo cấu trúc:

```text
Sau cuộc họp này, chúng ta cần có [output cụ thể] để [lý do/ảnh hưởng].
```

Nếu mục tiêu còn mơ hồ, đề xuất phiên bản rõ hơn và hỏi user xác nhận nếu đây là quyết định quan trọng.

### Bước 3. Gom ngữ cảnh từ Second Brain nếu có

Khi có quyền đọc vault hoặc user chỉ tới file liên quan, tìm/nghiên cứu:

- project liên quan trong `4. Kiến Tạo/` hoặc `4. Kiến Tạo/1. Đang Làm/`;
- meeting note cũ trong `Meetings/` nếu là não bộ doanh nghiệp;
- quyết định cũ trong `Decisions/`;
- People/Companies liên quan nếu có;
- tài liệu sản phẩm/chiến lược trong `00. Business Context/`;
- các template/framework liên quan trong project template của bạn.

Không bịa dữ liệu nếu không tìm thấy. Ghi rõ `Chưa tìm thấy trong vault` hoặc `Cần sếp cung cấp thêm`.

### Bước 4. Xác định người tham gia và vai trò

Với từng người, xác định:

- vai trò trong cuộc họp;
- họ cần chuẩn bị gì trước;
- họ có cần dự toàn bộ cuộc họp không;
- họ là người quyết định, người cung cấp dữ liệu, owner hay người bị ảnh hưởng.

Nếu danh sách người tham gia quá rộng, đề xuất rút gọn.

### Bước 5. Tách bối cảnh, câu hỏi, quyết định và hành động

Tạo bốn khối riêng:

1. Bối cảnh cần nắm.
2. Câu hỏi cần hỏi.
3. Quyết định cần chốt.
4. Action items dự kiến sau họp.

Không trộn câu hỏi với quyết định. Không biến action item thành quyết định nếu chưa có người chốt.

### Bước 6. Thiết kế agenda có timebox

Agenda phải có:

- thứ tự thảo luận;
- thời lượng từng phần;
- output của từng phần;
- phần chốt quyết định;
- phần chốt action items.

Nếu thời lượng user đưa quá ngắn hoặc quá dài, đề xuất điều chỉnh.

### Bước 7. Chuẩn bị talking points và pre-read

Tạo:

- 3-7 talking points chủ cuộc họp cần nói;
- danh sách tài liệu/note/link cần gửi trước;
- câu mở đầu cuộc họp trong 1-3 câu.

### Bước 8. Chốt rủi ro và follow-up

Chỉ ra:

- điều dễ khiến cuộc họp lệch hướng;
- quyết định dễ bị bỏ qua;
- người cần follow-up;
- cách ghi biên bản/action items ngay sau họp.

## Output bắt buộc

Trả về bằng tiếng Việt, rõ ràng, dùng được ngay:

```markdown
# Chuẩn bị cuộc họp - [Tên cuộc họp]

## 1. Mục tiêu cuộc họp

## 2. Loại họp

## 3. Bối cảnh cần nắm

## 4. Người tham gia và vai trò

| Người | Vai trò | Cần chuẩn bị |
|---|---|---|

## 5. Agenda có timebox

| Thời lượng | Nội dung | Output cần có |
|---:|---|---|

## 6. Câu hỏi cần hỏi

| Câu hỏi | Người trả lời | Lý do |
|---|---|---|

## 7. Quyết định cần chốt

| Quyết định | Người quyết định | Tiêu chí chốt |
|---|---|---|

## 8. Tài liệu/ngữ cảnh cần đọc trước

## 9. Rủi ro cần tránh

## 10. Output sau họp

## 11. Checklist follow-up
```

Nếu thông tin chưa đủ, vẫn trả bản nháp và thêm section:

```markdown
## Cần sếp bổ sung
```

## Nơi lưu nếu có tạo file

Nếu user yêu cầu lưu bản chuẩn bị họp:

- Với cuộc họp thuộc não bộ doanh nghiệp: lưu vào `Meetings/` hoặc project liên quan nếu user chỉ rõ.
- Tên file gợi ý:

```text
YYYY-MM-DD — Chuẩn bị — [Tên cuộc họp].md
```

File phải có frontmatter tối thiểu:

```yaml
---
created: YYYY-MM-DD
type: meeting-prep
status: draft
tags: [meeting, meeting-prep]
---
```

Nếu cuộc họp liên quan người/công ty/project cụ thể, thêm wikilink tới các note đó để không tạo note mồ côi.

## Sau khi hoàn thành

Sau khi trả Meeting Brief:

1. Nhắc user câu gọi lại skill:

```text
Gọi skill mindmirror-chuan-bi-cuoc-hop-cong-ty-doi-nhom để chuẩn bị cuộc họp: [tên cuộc họp]
```

2. Nếu cuộc họp sắp diễn ra, gợi ý sau họp dùng workflow biên bản cuộc họp hoặc phân tích ghi âm nếu có transcript/recording.
3. Nếu có tạo file, báo đường dẫn đã lưu.
