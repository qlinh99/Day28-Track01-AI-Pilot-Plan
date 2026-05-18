---
artifact: 4 — Problem Framing (bản nộp phase Frame)
bai-tap: Frame — đóng khung vấn đề thật
phase: Double Diamond vòng 1 · ◆ output (chốt — owner xác nhận)
time: ~13 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 2-quick-win.md · prompts/03-problem-framing-challenge.md
nop-cuoi: Có — đây là bản nộp của phase Frame (Part A · A3 Working Canvas mục Problem Framing)
---

# 3 — FINAL: Problem Framing

Mục tiêu: đóng khung Quick Win đã chọn cho thật cụ thể. Đây **không phải** bản đề xuất giải pháp — là tài liệu trả lời đúng 1 câu: *"nhóm đã hiểu đúng vấn đề chưa?"*. Đây là output chốt của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1, và là một mục trong A3 Working Canvas nộp cuối buổi.

Lý do làm bước này: một AI Pilot Plan cho vấn đề SAI — dù viết hay — vẫn sai. Đa số nhóm trượt Gate 3 vì khung chung chung ("học viên cần học tốt hơn", "coach quá tải") — câu đó không đo được, không ai chịu trách nhiệm, không biết khi nào thành công.

Quy tắc: **pain phải có số.** "Nhiều người phàn nàn" không phải evidence. "200 câu hỏi/tuần × 20 phút = 67 giờ/tuần" mới là evidence. Trong lab dùng số giả định cũng được, nhưng phải nói rõ số đến từ đâu.

## Quy trình 13 phút

```text
9 phút  — Điền 9 mục Problem Framing
3 phút  — Tự phản biện
1 phút  — Chốt: owner (giả định) có xác nhận đúng vấn đề không
```

---

## 9 mục Problem Framing

Câu hỏi phụ (tự trả lời trước khi điền):

- Một người ngoài đọc khung này có biết CHÍNH XÁC ai đau, đau cái gì không?
- Nếu KHÔNG có baseline thì nhóm đo "tốt hơn" bằng cách nào?
- Mục Open Questions trống = nguy hiểm (chưa nghĩ đủ). Nhóm còn chưa biết gì?

### Trả lời

1. **Original Ask** (stakeholder nói gì, nguyên văn):
   > "Biến tài liệu LMS thành tutor tương tác, hỏi-đáp có nguồn, mini practice. VD: Học viên hỏi 'Pilot Plan khác project plan thế nào?' — Tutor trả lời dựa trên handbook."

2. **Reframed problem** (vấn đề thật sau khi tách):
   Học viên đang làm worksheet/lab gặp khái niệm chưa rõ nhưng không có cách tra Handbook nhanh ngay trong LMS — phải thoát ra, tìm file dài, Ctrl+F, đọc không đủ context, hoặc đăng lên Discord đợi coach. Kết quả: tắc tiến độ giữa chừng, câu hỏi lặp dồn lên coach, coach mất thời gian trả lời câu đáng ra học viên tự tìm được.

3. **Current workflow** (hiện tại đang xử lý thế nào):
   - Học viên gặp thuật ngữ/câu hỏi nội dung → thoát LMS → mở Handbook PDF/Markdown → Ctrl+F từ khóa → đọc đoạn xung quanh → nhiều khi vẫn không đủ context → bỏ qua hoặc đoán
   - Hoặc: post câu hỏi lên Discord/nhắn coach → đợi reply (15 phút đến vài giờ trong giờ lab)
   - Coach nhận cùng câu hỏi từ nhiều học viên khác nhau trong 1 buổi, trả lời thủ công từng người

4. **Pain evidence — bằng SỐ** (số giả định — ghi rõ nguồn):

```text
Quy mô ước tính (giả định, dựa trên bối cảnh 80 học viên track Product):
  • 80 học viên × 2 câu hỏi nội dung/buổi lab = ~160 câu/buổi
  • Coach trả lời ~5 phút/câu = 800 phút (~13 giờ coach time/buổi) — không khả thi với 1–2 coach
  • Thực tế chỉ ~20–30% câu được trả lời trong giờ lab
    → 70–80% học viên tự xử (bỏ qua / đoán / chờ buổi sau)

Khoảnh khắc đau: giữa buổi lab khi học viên đang điền worksheet, gặp khái niệm
chưa rõ (VD: "What is a Problem Statement?", "Double Diamond là gì?") — cần tra ngay
trong 1–2 phút, không muốn thoát khỏi LMS.

Nguồn số: ước tính từ quy mô khóa (80 học viên / track) + bối cảnh Discord AI20k.
Cần validate bằng khảo sát 10 học viên trước pilot thật.
```

5. **Affected people**:
   - **Dùng trực tiếp**: Học viên track Product (~80 người) đang làm worksheet trong buổi lab
   - **Quyết duyệt pilot**: Instructor / PM AI20k (xét duyệt scope + chi phí)
   - **Review/Expert**: Coach (calibrate chất lượng câu trả lời, xác nhận citation đúng trước khi mở rộng)

6. **Constraints** (từ `00-context.md`):
   - **Citation bắt buộc**: mọi câu trả lời phải có nguồn (tên tài liệu + section/trang); thiếu nguồn = nói "không biết", không bịa
   - **Human review**: coach review sample câu trả lời (50 câu đầu) trước khi mở rộng — AI không tự quyết chất lượng
   - **Privacy**: chỉ index tài liệu khóa đã public (Handbook, Slide); không dùng data bài nộp/hành vi học viên
   - **Budget nhỏ**: dùng LLM API có sẵn (Claude/OpenAI) + RAG đơn giản, không xây platform lớn
   - **Formative only**: AI không chấm điểm, không đưa ra đánh giá năng lực học viên
   - **Adoption**: pilot 10–20 học viên trước, đo tỷ lệ dùng thật trước khi mở rộng

7. **Quick Win đã chọn** (từ `2-quick-win.md`):
   AI trả lời câu hỏi nội dung Handbook/Slide **kèm dẫn nguồn** (tên tài liệu + section), trong chatbox trên LMS, cho học viên track Product (~80 người) trong buổi lab.

8. **Open questions** (còn chưa biết):
   - Handbook/Slide trên LMS hiện ở định dạng gì (PDF, Markdown, DOCX)? → ảnh hưởng trực tiếp đến pipeline RAG
   - Citation granularity cần đến mức nào: "Handbook §A1" hay "Handbook §A1 tr.3"?
   - LMS hiện tại có cho phép embed chatbox không, hay phải build standalone URL?
   - Khi AI không biết câu trả lời (nội dung không có trong tài liệu), trả về gì để học viên không bị lạc?
   - Coach có bandwidth review ~50 câu/tuần đầu không?

9. **Validation** (đóng vai instructor/PM AI20k):

```text
Vấn đề: "Học viên làm lab không tra được Handbook nhanh — hỏi coach câu lặp, coach mất
13 giờ/buổi trả lời thủ công, 70–80% câu hỏi không được giải đáp trong giờ."

→ XÁC NHẬN: Đây là vấn đề thật và đáng giải.
   Giải quyết được 30% câu hỏi lặp (câu về định nghĩa / quy trình đã có trong Handbook)
   = tiết kiệm ~4 giờ coach/buổi = đủ để xin pilot.
   Điều kiện pass: citation accuracy ≥ 80% sau coach review 50 câu đầu.
```

---

## Tự phản biện

- Còn câu chung chung không? → "Coach quá tải" đã được cụ thể hóa bằng số: 160 câu × 5 phút = 800 phút/buổi. Không còn câu chung chung kiểu "học tốt hơn".
- **Số/giả định lấy ở đâu?** → Ước tính từ 80 học viên × 2 câu/buổi. Cần validate bằng khảo sát 10 học viên trước pilot thật — ghi rõ trong Open Questions.
- **Giả định chính sai thì sao?** → Nếu học viên thực ra ít hỏi (tự dùng Google), adoption sẽ thấp. Pilot cần đo tỷ lệ dùng thật (số câu hỏi/học viên/tuần) song song với citation accuracy.
- **Khi nào dừng?** → Citation accuracy < 80% sau review 50 câu đầu → dừng, sửa pipeline trước khi mở rộng. Đã ghi ở mục 9.

---

## Tổng kiểm tra trước khi sang `02-solution/`

| Hạng mục | Xong? |
|---|---|
| Chỉ rõ 1 nhóm người + 1 khoảnh khắc cụ thể (không "user nói chung") | ✓ — Học viên track Product, giữa buổi lab khi điền worksheet |
| Pain có số (hoặc kế hoạch lấy số), nói rõ số từ đâu | ✓ — 160 câu/buổi × 5 phút = 800 phút; nguồn giả định ghi rõ |
| Có baseline (hoặc cách đo baseline) + ≥1 chỉ số có ngưỡng | ✓ — Baseline: 70–80% câu không được giải đáp trong giờ. Ngưỡng pass: citation accuracy ≥ 80% / 50 câu đầu |
| Mục 9: owner (giả định) xác nhận đúng vấn đề = qua cổng phase Frame | ✓ — XÁC NHẬN, điều kiện pass rõ ràng |

⚑ Coach kiểm tra ở Mốc 2: *"Ai đau? Baseline là gì? Không có baseline thì đo thế nào?"*

Owner chưa xác nhận → quay lại file `1`/`2`, đừng sang Solution. Owner xác nhận → mở `../02-solution/1-find-existing-solutions.md`.

*Liên quan: handbook §A4 · `prompts/03-problem-framing-challenge.md`*
