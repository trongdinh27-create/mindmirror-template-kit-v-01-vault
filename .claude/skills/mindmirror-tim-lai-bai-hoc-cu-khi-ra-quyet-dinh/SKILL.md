---
name: mindmirror-tim-lai-bai-hoc-cu-khi-ra-quyet-dinh
description: "Tìm lại bài học cũ trong Second Brain khi cần ra quyết định: scan note liên quan, so sánh bối cảnh, rút nguyên tắc và đề xuất bước kiểm chứng nhỏ."
---

# MindMirror - Tìm Lại Bài Học Cũ Khi Cần Ra Quyết Định

## Mục tiêu

Giúp sếp ra quyết định dựa trên bài học đã sống qua và tri thức đã lưu trong MindMirror:

- truy hồi bài học cũ liên quan;
- đối chiếu bối cảnh cũ với hiện tại;
- nhận ra mô thức lặp lại;
- rút nguyên tắc quyết định;
- đề xuất bước kiểm chứng nhỏ.

AI không được quyết định thay sếp.

## Nguồn bắt buộc phải đọc

Trước khi thực hiện:

1. `CLAUDE.md`
2. `QUY ƯỚC MINDMIRROR.md`
3. `Me.md`
4. `5. Hộp Công Cụ/Template/Template - Tìm Lại Bài Học Cũ Khi Cần Ra Quyết Định.md`
5. `3. Chuyển Hoá/Tri Thức/Framework/Framework - Tìm Lại Bài Học Cũ Khi Cần Ra Quyết Định.md`

Khi truy hồi, scan các vùng liên quan:

- `3. Chuyển Hoá/Tri Thức/Kiến Thức Cốt Lõi/`
- `3. Chuyển Hoá/Tri Thức/Framework/`
- `2. Tinh Lọc/Kiến Thức Nguồn/`
- `2. Tinh Lọc/Nhật Ký Ngày/`
- `2. Tinh Lọc/Tổng Kết Tuần/`
- `4. Kiến Tạo/`
- `6. OPC Company 2Brain/`

## Đầu vào tối thiểu

Sếp chỉ cần đưa:

```text
Quyết định hiện tại: [mô tả]
```

Nếu có thêm:

- các phương án;
- deadline;
- điều đang phân vân;
- kết quả mong muốn;
- rủi ro sợ nhất;
- chủ đề hoặc project liên quan;
- muốn lưu kết quả hay chỉ tư vấn trong chat.

## Nếu thiếu dữ liệu

Nếu chưa rõ quyết định, hỏi tối đa 5 câu:

1. Anh đang cần quyết định điều gì?
2. Có những phương án nào?
3. Điều gì khiến anh phân vân nhất?
4. Kết quả anh muốn đạt là gì?
5. Nếu chọn sai, cái giá lớn nhất là gì?

Nếu đủ dữ liệu để truy hồi, không hỏi thêm dài dòng.

## Quy trình

### Bước 1. Làm rõ quyết định

Tóm tắt quyết định hiện tại, phương án, deadline, rủi ro và kết quả mong muốn.

### Bước 2. Tạo từ khóa truy hồi

Tạo 5-10 từ khóa tiếng Việt/tiếng Anh nếu cần:

- chủ đề;
- người/nhóm liên quan;
- cảm xúc hoặc mô thức;
- loại quyết định;
- dự án/area;
- từ đồng nghĩa.

### Bước 3. Scan vault bằng `rg`

Ưu tiên `rg` để tìm trong các thư mục bắt buộc. Không bịa note nếu không tìm thấy.

### Bước 4. Đọc note liên quan nhất

Chọn 3-7 note có liên quan cao nhất. Đọc nội dung đủ để hiểu bối cảnh, không chỉ dựa vào tiêu đề.

### Bước 5. So sánh bối cảnh

Với mỗi bài học:

- cũ giống hiện tại ở đâu;
- cũ khác hiện tại ở đâu;
- bài học còn dùng được không;
- có nguy cơ áp dụng sai không.

### Bước 6. Rút nguyên tắc quyết định

Tổng hợp thành:

- điều nên làm;
- điều nên tránh;
- câu hỏi còn thiếu;
- nguyên tắc ra quyết định.

### Bước 7. Đề xuất hướng và bước kiểm chứng

Đưa khuyến nghị mềm, kèm câu:

```text
Đây là khuyến nghị dựa trên bài học cũ, không phải quyết định thay sếp.
```

Luôn có một bước kiểm chứng nhỏ trong 24-72 giờ.

## Output bắt buộc

```markdown
## Tóm tắt quyết định

## Từ khóa đã dùng để truy hồi

## Bài học cũ liên quan

| Note | Vì sao liên quan | Mức độ | Cảnh báo |
|---|---|---|---|
|  |  |  |  |

## Bài học rút lại cho hiện tại

## Điều nên tránh lặp lại

## Nguyên tắc ra quyết định

## Khuyến nghị của AI

## Bước kiểm chứng 24-72 giờ

## Link liên quan
```

Nếu không tìm thấy đủ note liên quan, nói rõ:

```text
Vault hiện chưa có đủ bài học cũ cho quyết định này. Em sẽ dựa trên dữ liệu hiện có và đề xuất câu hỏi cần capture thêm.
```

## Nơi lưu nếu có tạo file

Nếu sếp yêu cầu lưu kết quả tư vấn quyết định, lưu vào:

```text
4. Kiến Tạo/3. Tham khảo/
```

Hoặc nếu thuộc project đang chạy, lưu vào đúng project liên quan.

Nếu phát sinh bài học mới, đề xuất dùng:

```text
mindmirror-rut-bai-hoc-tu-chuyen-vua-xay-ra
mindmirror-chuyen-suy-nghi-thanh-kien-thuc-cot-loi
```

Framework/template của workflow này nằm trong:

```text
5. Hộp Công Cụ/Template/
3. Chuyển Hoá/Tri Thức/Framework/
```

## Sau khi hoàn thành

Kết thúc bằng:

1. bài học cũ quan trọng nhất;
2. nguyên tắc nên dùng;
3. bước kiểm chứng nhỏ trước khi quyết định.
