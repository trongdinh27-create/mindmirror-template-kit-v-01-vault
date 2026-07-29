---
name: mindmirror-tao-ho-so-khach-hang-theo-vpd
description: "Tạo hồ sơ/chân dung khách hàng theo Value Proposition Design từ bộ câu hỏi có sẵn, transcript/audio/note thô hoặc tự tạo bộ câu hỏi phỏng vấn theo ngành nghề; output 5 file: PV, CD VPD, MOC khách hàng, kế hoạch tư vấn/bước tiếp theo, email cảm ơn/tổng hợp gửi khách."
---

# MindMirror — Tạo Hồ Sơ Khách Hàng Theo VPD

## Mục đích

Dùng skill này khi bạn muốn biến một cuộc trò chuyện, transcript, ghi âm, note thô hoặc bộ câu hỏi phỏng vấn thành một hồ sơ khách hàng rõ ràng theo Value Proposition Design (VPD), rồi dùng hồ sơ đó để tư vấn, thiết kế offer, chăm sóc và viết email gửi lại khách hàng.

Skill này thay thế bản cũ chỉ dành cho "tiếp nhận học viên". Bản mới dùng được cho mọi ngành nghề, mọi loại khách hàng, mọi sản phẩm/dịch vụ, miễn là có mục tiêu hiểu khách hàng sâu hơn để ra quyết định.

## Khi Nào Dùng

- User nói: "tạo hồ sơ khách hàng", "chân dung khách hàng", "phân tích khách hàng theo VPD", "Value Proposition Design", "phỏng vấn khách hàng", "tạo bộ câu hỏi phỏng vấn khách hàng", "phân tích transcript khách hàng".
- User đã có bộ câu hỏi và muốn AI phân tích câu trả lời.
- User chưa có bộ câu hỏi và muốn AI tự phỏng vấn để tạo bộ câu hỏi phù hợp ngành nghề/công việc.
- User có ghi âm/transcript/note thô từ buổi tư vấn, sales call, coaching call, discovery call.

## Nguyên Tắc

- Phân biệt rõ dữ kiện khách hàng nói thật và suy luận của AI.
- Không ép mọi khách hàng phải fit với offer. Nếu fit thấp, đề xuất nuôi dưỡng, hỏi thêm hoặc không bán.
- Không hard-code MindMirror. Luôn bám vào ngành nghề, offer, công việc và bối cảnh của người đang dùng skill.
- Không tạo deadline giả, khan hiếm giả hoặc lời hứa vượt quá bằng chứng.
- Nếu thông tin thiếu, hỏi thêm trước khi kết luận các phần quan trọng như budget, offer, mức độ sẵn sàng trả tiền.

## Input Cần Có

Nhận một trong các dạng sau:

1. Bộ câu hỏi + câu trả lời của khách hàng.
2. Transcript/note thô sau cuộc gọi.
3. File ghi âm/video cần transcribe trước.
4. Chỉ có ngành nghề/công việc/sản phẩm và muốn AI tạo bộ câu hỏi phỏng vấn trước.

Nếu thiếu dữ liệu, hỏi ngắn gọn theo thứ tự:

1. Khách hàng/người được phỏng vấn tên gì?
2. Ngành nghề/công việc/sản phẩm/dịch vụ đang phân tích là gì?
3. Mục tiêu của buổi phỏng vấn là gì: hiểu nhu cầu, thiết kế offer, tư vấn, chốt sale, nghiên cứu thị trường hay chăm sóc sau mua?
4. Đã có bộ câu hỏi/câu trả lời/transcript chưa, hay cần AI tạo bộ câu hỏi trước?

## Quy Trình Chuẩn

### Bước 1 — Chọn Chế Độ Làm Việc

Xác định một trong ba chế độ:

- **Chế độ A — Đã có dữ liệu:** user đưa transcript, note thô hoặc câu trả lời. Chuyển sang phân tích.
- **Chế độ B — Đã có bộ câu hỏi nhưng thiếu câu trả lời:** dùng bộ câu hỏi đó để phỏng vấn từng câu, hỏi tự nhiên, mỗi lần một cụm nhỏ.
- **Chế độ C — Chưa có bộ câu hỏi:** tạo bộ câu hỏi phỏng vấn riêng cho ngành nghề/công việc trước, sau đó dùng bộ câu hỏi này để phỏng vấn.

### Bước 2 — Tạo Hoặc Chuẩn Hóa Bộ Câu Hỏi

Nếu cần tạo bộ câu hỏi, thiết kế theo cấu trúc:

1. **Bối cảnh khách hàng:** vai trò, công việc, tình trạng hiện tại, trách nhiệm chính.
2. **Jobs (Công việc cần hoàn thành):**
   - Functional Job: họ đang cố làm việc gì trong thực tế?
   - Social Job: họ muốn được người khác nhìn nhận thế nào?
   - Emotional Job: họ muốn cảm thấy thế nào?
3. **Pains (Nỗi đau):**
   - Pain bề mặt: vấn đề họ tự nhận ra.
   - Pain sâu hơn: hệ quả đang kéo họ xuống.
   - Pain ẩn nhất: nỗi sợ, mất mát, rủi ro hoặc niềm tin sai chưa nói thẳng.
4. **Gains (Kết quả mong muốn):**
   - Gain phải có.
   - Gain kỳ vọng.
   - Gain WOW.
   - Kết quả 90 ngày.
   - Di sản hoặc giá trị dài hạn.
5. **Hành vi mua và bối cảnh quyết định:** đã thử giải pháp nào, vì sao chưa hiệu quả, tiêu chí chọn, rào cản, ngân sách/lịch sử đầu tư nếu có.
6. **Ngôn ngữ khách hàng:** câu nói nguyên văn, từ khóa, hình ảnh ẩn dụ, cách họ mô tả vấn đề.
7. **Bước tiếp theo mong muốn:** họ muốn được tư vấn gì, muốn nhận gì sau buổi nói chuyện.

Sau khi tạo bộ câu hỏi, hỏi user muốn:

- dùng ngay để phỏng vấn,
- lưu thành template riêng,
- hay chỉnh lại trước.

### Bước 3 — Phân Tích Theo VPD

Từ câu trả lời/transcript, extract thành bảng phân tích nội bộ:

```text
Tên khách hàng:
Ngành nghề / vai trò:
Bối cảnh hiện tại:
Functional Jobs:
Social Jobs:
Emotional Jobs:
Pain bề mặt:
Pain sâu hơn:
Pain ẩn nhất:
Quote nguyên văn quan trọng:
Gain phải có:
Gain kỳ vọng:
Gain WOW:
Kết quả 90 ngày:
Di sản / giá trị dài hạn:
Giải pháp đã thử:
Rào cản mua:
Trigger hiện tại:
Mức độ đau:
Mức độ sẵn sàng trả tiền:
Giai đoạn nhận thức:
Cơ hội fit với offer:
Thông tin còn thiếu:
```

Nếu là transcript dài, ưu tiên giữ lại quote thật. Không bịa quote.

### Bước 4 — Tạo 5 File

Khi user đồng ý lưu, tạo đủ 5 file sau. Nếu user chưa yêu cầu lưu, hiển thị bản preview trước.

Đường dẫn mặc định:

```text
4. Kiến Tạo/2. Lĩnh vực/Khách Hàng/Phỏng Vấn/
4. Kiến Tạo/2. Lĩnh vực/Khách Hàng/Chân Dung/
4. Kiến Tạo/2. Lĩnh vực/Khách Hàng/Hồ Sơ/
4. Kiến Tạo/2. Lĩnh vực/Khách Hàng/Kế Hoạch Chăm Sóc/
4. Kiến Tạo/2. Lĩnh vực/Khách Hàng/Email/
```

Nếu đang làm trong Não Bộ Doanh Nghiệp SME và khách hàng là người thật, link thêm về `People/`, `Companies/`, `Meetings/`, `Projects/` hoặc `03. Areas/Sales Pipeline & CRM/` khi phù hợp.

#### File 1 — PV

Tên file:

```text
PV — Phỏng Vấn Khách Hàng — [Tên] — YYYY-MM-DD.md
```

Nội dung bắt buộc:

- Thông tin buổi phỏng vấn.
- Mục tiêu phỏng vấn.
- Bộ câu hỏi đã dùng.
- Câu trả lời của khách hàng.
- Quote đáng chú ý.
- Trường còn thiếu.

#### File 2 — CD VPD

Tên file:

```text
CD — Chân Dung Khách Hàng Theo VPD — [Tên].md
```

Nội dung bắt buộc:

- Chân dung 1 câu.
- Bối cảnh hiện tại.
- Jobs: Functional / Social / Emotional.
- Pains: bề mặt / sâu hơn / ẩn nhất.
- Gains: phải có / kỳ vọng / WOW / 90 ngày / di sản.
- Pain Relievers: giải pháp giúp giảm từng pain.
- Gain Creators: giải pháp tạo từng gain.
- Fit với giải pháp/offer hiện có.
- Gợi ý offer phù hợp.
- Mức độ phù hợp: mức độ đau, sẵn sàng trả tiền, giai đoạn nhận thức, tier phù hợp, tiềm năng giới thiệu.
- Góc content và thông điệp bán hàng.
- Câu hỏi cần hỏi thêm.

#### File 3 — MOC Khách Hàng

Tên file:

```text
MOC Khách Hàng — [Tên].md
```

Nội dung bắt buộc:

- Link tới PV, CD, kế hoạch chăm sóc, email.
- Timeline tương tác.
- Tóm tắt 1 màn hình.
- Việc cần theo dõi.
- Các buổi họp/cuộc gọi liên quan nếu có.

#### File 4 — Kế Hoạch Chăm Sóc / Tư Vấn / Bước Tiếp Theo

Tên file:

```text
KH — Kế Hoạch Chăm Sóc Tư Vấn Bước Tiếp Theo — [Tên].md
```

Nội dung bắt buộc:

- Mục tiêu chăm sóc/tư vấn.
- 3 ưu tiên cần xử lý.
- Bước tiếp theo đề xuất.
- Owner.
- Deadline nếu có.
- Rủi ro nếu tư vấn/bán sai.
- Nội dung cần chuẩn bị cho lần trao đổi tiếp theo.

#### File 5 — Email Gửi Khách Hàng

Tên file:

```text
Email — Tóm Tắt Tư Vấn Gửi Khách Hàng — [Tên].md
```

Nội dung bắt buộc:

```text
Subject: [Tên khách hàng] — Tóm tắt buổi tư vấn hôm nay

[Tên],

[Cảm ơn ngắn, tự nhiên, có nhắc lại bối cảnh thật của buổi nói chuyện.]

Sau buổi hôm nay, em/anh hiểu rằng:
- Anh/chị đang muốn [kết quả / job chính].
- Điều đang cản trở nhiều nhất là [pain chính].
- Điều quan trọng nhất trong giai đoạn tới là [gain hoặc kết quả 90 ngày].

Một ý em/anh thấy rất đáng chú ý là: "[quote thật nếu có]".

Từ góc nhìn tư vấn, hướng đi phù hợp nhất lúc này là:
[2-4 câu tư vấn rõ ràng, không bán quá tay.]

Nếu mình đi tiếp, bước hợp lý nhất là:
[offer hoặc next step phù hợp với mức độ fit.]

[CTA nhẹ, một hành động cụ thể.]

[Chữ ký]
```

Email phải ấm, rõ, có ích ngay cả khi khách chưa mua. Không dùng áp lực giả, không chốt sale thô.

## Output Cuối Cùng Cho User

Sau khi hoàn thành, trả về ngắn gọn:

```text
Đã tạo hồ sơ khách hàng theo VPD cho [Tên].

5 file đã tạo:
- [PV path]
- [CD path]
- [MOC path]
- [KH path]
- [Email path]

Nhận định nhanh:
- Fit: [cao/trung bình/thấp]
- Offer phù hợp: [tên offer hoặc cần hỏi thêm]
- Bước tiếp theo: [hành động cụ thể]
```

Nếu chưa lưu file, trả về bản phân tích preview và hỏi user có muốn lưu đủ 5 file không.
