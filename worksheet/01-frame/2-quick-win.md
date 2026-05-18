---
artifact: 3 — Quick Win Selection
bai-tap: Frame — chọn lát cắt làm trước
phase: Double Diamond vòng 1 · ◆ siết (hội tụ về 1 lựa chọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-intake-breakdown.md · prompts/02-quick-win-challenge.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 2 — Quick Win: chọn lát cắt làm trước

Mục tiêu: từ 5–8 use case ở file `1`, chấm điểm nhanh và chốt **1 Quick Win** để pilot đầu tiên — kèm lý do chọn và lý do *không* chọn các phần khác. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1.

Lý do làm bước này: đây là quyết định quan trọng nhất của phase Frame. Quick Win **không phải** phần dễ nhất hay nghe hay nhất — là phần *chứng minh được giá trị nhanh và có người ủng hộ*. Chọn sai → pilot fail → mất uy tín → khó xin pilot tiếp. Nhóm phải chọn được *và bảo vệ được bằng lý do*, không bằng cảm tính.

Quy tắc: **điểm số chỉ là gợi ý, không phải đáp án.** Đừng để con số quyết thay nhóm — nó chỉ giúp so sánh.

## Bước 0 — Lấy 4–6 use case mạnh nhất từ file `1` (1 phút)

Loại ngay khỏi bảng chấm:
- **#5 Gợi ý tài liệu liên quan** — phụ thuộc #1, không độc lập
- **#6 Feedback bài nộp** — rủi ro cao nhất, vi phạm ràng buộc Human review

Còn lại 5 ứng viên đưa vào bảng: #1 · #2 · #3 · #4 · #7

## Quy trình 10 phút

```text
1 phút  — Bước 0: chọn 4–6 ứng viên
5 phút  — Phần A: chấm điểm 4 trục
3 phút  — Phần B: 1 lý do nên / 1 lý do không cho top 2
1 phút  — Phần C: chốt + ai ủng hộ + cái KHÔNG chọn
```

---

## Phần A — Chấm điểm 4 trục (1–5 mỗi trục)

Câu hỏi phụ (tự trả lời):

- "Risk" ở đây là *sai thì mất gì* — chọn đúng việc chính của user (task centrality) thì sai cũng đỡ đau; chọn việc lớn nhất thì sai rất đắt. Use case nào risk thấp thật?
- Use case nào có sẵn data + có người trong AI20k thật sự muốn dùng?

| Use case | Impact (×.30) | Feasibility (×.25) | Evidence nhanh (×.25) | Risk an toàn (×.20) | Tổng | Hạng |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| #1 — Q&A có dẫn nguồn (Handbook/Slide) | 5 | 4 | 5 | 4 | **4.55** | **2** |
| #2 — Tóm tắt bài giảng theo yêu cầu | 3 | 4 | 4 | 5 | 3.90 | 3 |
| #3 — Giải thích thuật ngữ/khái niệm (Glossary) | 4 | 5 | 5 | 5 | **4.70** | **1** |
| #4 — Mini quiz luyện tập | 3 | 2 | 2 | 2 | 2.30 | 5 |
| #7 — Onboarding học viên mới | 3 | 4 | 3 | 4 | 3.45 | 4 |

**Ghi chú chấm điểm:**
- #1 Impact=5: 500 học viên, coach không đủ trả lời, câu hỏi lặp liên tục. Feasibility=4 (không phải 5) vì RAG over toàn bộ Handbook cần xử lý chunking + embedding — phức tạp hơn Glossary.
- #3 Feasibility=5 + Evidence=5: glossary.md có sẵn dạng Markdown, demo trong 1 ngày. Nhưng **tác động hẹp hơn #1** — chỉ phủ thuật ngữ, không phủ câu hỏi về quy trình, bài tập, bối cảnh.
- #4 điểm thấp: phụ thuộc #1, tạo câu hỏi chất lượng khó đảm bảo, fail = confuse học viên (Risk=2).

(Thang điểm chi tiết: `templates/quick-win-scoring.md`.)

## Phần B — 1 lý do nên / 1 lý do không, cho top 2

**Ứng viên A — #3 Giải thích thuật ngữ/khái niệm từ Glossary** *(điểm cao nhất: 4.70)*

```text
Nên chọn vì: Demo được trong 1 ngày với glossary.md có sẵn — bằng chứng nhanh nhất,
             không có dependency, không rủi ro nếu sai.

Không nên vì: Phạm vi quá hẹp — chỉ phủ ~thuật ngữ trong glossary, không chứng minh
             được giá trị cốt lõi của track (Q&A bất kỳ câu hỏi nội dung bài giảng
             từ Handbook). Stakeholder hỏi "so với Ctrl+F trong PDF thì khác gì?" → khó bảo vệ.
```

**Ứng viên B — #1 Q&A có dẫn nguồn từ Handbook/Slide** *(điểm nhì: 4.55)*

```text
Nên chọn vì: Chứng minh đúng core value của track — học viên hỏi bất kỳ câu nội dung
             bài học, AI trả lời kèm "nguồn: Handbook §A1 tr.3". Demo bằng 5 câu hỏi
             thật từ Day 28 là đủ thuyết phục stakeholder và coach.

Không nên vì: Feasibility thấp hơn #3 một chút — cần index Handbook (~50–100 trang),
             xử lý chunking, test citation accuracy trước khi demo. Mất ~3–5 ngày setup
             so với 1 ngày của Glossary.
```

## Phần C — Chốt Quick Win

- **Quick Win nhóm chọn**: **#1 — Q&A có dẫn nguồn từ Handbook/Slide LMS**

- **Vì sao chọn cái này trước**: Mặc dù #3 (Glossary) chấm điểm cao hơn 0.15 điểm, nhưng nó chỉ là tập con của #1 — chọn #3 trước sẽ cần build lại khi mở rộng sang Handbook. #1 chứng minh đúng core value của track ("tutor tương tác hỏi-đáp có nguồn") và trả lời được câu của stakeholder: *"Học viên hỏi 'Pilot Plan khác Project Plan thế nào?' — Tutor trả lời từ Handbook"*. Evidence cũng nhanh: 5 câu hỏi thật từ Day 28, demo live trong 1 tuần với Handbook dạng Markdown đã có sẵn. Sai thì học viên tự đọc tài liệu gốc — Risk thấp.

- **Ai trong AI20k sẽ ủng hộ pilot này**:
  - **Coach/Instructor**: giảm tải câu hỏi lặp ("Pilot Plan là gì?", "Double Diamond dùng thế nào?") — tiết kiệm thời gian coaching cho câu hỏi sâu hơn.
  - **Học viên track Product**: đang làm worksheet ngay lúc này, cần tra Handbook nhanh mà không muốn rời LMS. Đây là người dùng đầu tiên thật sự, ủng hộ ngay nếu demo trúng pain.

- **Nhóm KHÔNG chọn gì + vì sao**:
  1. **#4 Mini quiz** — Red Flag track card, phụ thuộc #1, tạo câu hỏi sai → confuse học viên. Làm sau khi #1 ổn định.
  2. **#6 Feedback bài nộp** — Rủi ro nhất: cần human calibrate rubric, output sai ảnh hưởng trực tiếp đến đánh giá học viên, vi phạm ràng buộc "Formative ≠ summative".
  3. **#3 Glossary** — Demo được ngay nhưng scope quá hẹp, không đủ để xin pilot riêng; sẽ tích hợp vào #1 như một quick lookup mode.

---

## Phát hiện ban đầu

- Điểm số cao nhất (#3 Glossary) và lựa chọn thực tế (#1 Q&A) không trùng nhau — đúng như cảnh báo của template: *điểm chỉ là gợi ý, không phải đáp án*. Impact và "ai ủng hộ" mới là yếu tố quyết định.
- #1 và #3 thực ra là 1 hệ thống, chỉ khác scope data đầu vào. Chọn #1 = chọn đúng, bao luôn #3.
- #4 (Mini quiz) bị loại hoàn toàn — đây là Red Flag của track nhưng cũng là thứ nhóm dễ bị cám dỗ nhất khi "brainstorm sáng tạo".

## Câu hỏi mở (mang sang Problem Framing)

- Handbook/Slide trên LMS hiện ở định dạng gì (PDF, Markdown, DOCX)? → ảnh hưởng đến pipeline RAG.
- Citation cần granular đến mức nào: tên section là đủ, hay cần số trang cụ thể?
- Pilot scope: 10–20 học viên track Product, hay mở rộng cả ~80 học viên track Product ngay?

---

## Tổng kiểm tra trước khi sang `3-FINAL-problem-framing.md`

| Hạng mục | Xong? |
|---|---|
| Có bảng chấm 4 trục cho ≥4 use case | ✓ — 5 use case |
| Chốt 1 Quick Win, lý do bám số/impact (không "nghe hay") | ✓ — #1 Q&A có nguồn, lý do rõ |
| Nêu rõ ai ủng hộ pilot này | ✓ — Coach + Học viên track Product |
| Ghi rõ ≥2 phần KHÔNG chọn + lý do | ✓ — 3 phần bị loại với lý do cụ thể |

⚑ Đây là phần coach kiểm tra ở Mốc 1: *"Vì sao không làm full tool? Vì sao chọn lát cắt này trước?"*

Sau bước này, mở `3-FINAL-problem-framing.md` — đóng khung vấn đề thật (bản nộp của phase Frame).

*Liên quan: handbook §A3 · `templates/quick-win-scoring.md` · `prompts/02-quick-win-challenge.md`*
