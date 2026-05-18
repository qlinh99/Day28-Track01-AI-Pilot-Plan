---
artifact: 8 — 5-slide Pitch + AI Support Log (bản nộp cuối lab)
bai-tap: Pilot Plan — dồn thành pitch, sẵn sàng phản biện
phase: Double Diamond vòng 2 · ◆ output (bản nộp cuối + present)
time: ~5 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-pilot-plan.md + toàn bộ 01-frame + 02-solution · templates/5-slide-pitch.md
nop-cuoi: Có — bản nộp cuối lab (Part E · 5-slide Pitch + AI Support Log)
---

# 2 — FINAL: 5-slide Pitch + AI Support Log

Mục tiêu: dồn cả A3 Working Canvas thành 5 slide pitch (5 phút), chuẩn bị trả lời 3 câu phản biện, và ghi AI Support Log. Đây là bản nộp cuối cùng của lab.

Lý do làm bước này: nguyên tắc *demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu*. Slide đẹp mà không trả lời được "số này lấy ở đâu" thì hỏng. Pitch không phải kể chuyện — là đưa evidence để stakeholder ra được một quyết định.

Quy tắc: **slide cuối phải là một lời xin rõ ràng** (xin gì · đổi lại hứa gì). Không có lời xin = stakeholder không biết approve cái gì.

## Quy trình 5 phút

```text
3 phút  — Dồn 5 slide (mỗi slide 1 thông điệp)
1 phút  — Chuẩn bị 3 câu phản biện
1 phút  — AI Support Log
```

---

## Phần A — 5 slide (mỗi slide 1 thông điệp)

Kéo nguyên liệu từ các file đã làm, đừng viết mới. Khung đầy đủ: `templates/5-slide-pitch.md`.

| # | Slide | Lấy từ | Nội dung 1–2 gạch đầu dòng | Ai nói |
|---|---|---|---|---|
| 1 | **Problem & user** | 01-frame/3-FINAL | • Học viên tra Handbook mất 5–10 phút/lần → 160 câu/buổi dồn lên coach, 70–80% không được giải đáp trong giờ<br>• User cụ thể: học viên track Product (~80 người) đang làm worksheet giữa buổi lab | **Linh** |
| 2 | **Breakdown & Quick Win** | 01-frame/1,2 | • 7 use case tách ra; chọn Q&A có dẫn nguồn vì: độc lập, feasible, demo được trong 1 tuần, core value của track<br>• Không chọn: mini quiz (Red Flag + phụ thuộc), feedback bài nộp (rủi ro vi phạm human review) | **Linh** |
| 3 | **Solution + bản vẽ flow** | 02-solution/2-FINAL | • Boost: LLM API + RAG đơn giản + prompt citation bắt buộc + fallback "không biết"<br>• Flow: Học viên hỏi → Retriever 3–5 đoạn → LLM answer → Citation check → Trả lời có nguồn hoặc fallback an toàn | **Điềm** |
| 4 | **Pilot Plan** | 03-pilot-plan/1 | • 2 tuần · 15–20 HV volunteer · 2 phase với cổng rõ ràng<br>• Coach review 50 câu đầu; xin: 2h coach/tuần + ~$15 API + phép pilot | **Điềm** |
| 5 | **Metric · Exit · Lời xin** | 03-pilot-plan/1 | • Pass khi: citation accuracy ≥ 80% + ≥ 50% HV dùng ≥1 câu/buổi<br>• **Lời xin**: 2h/tuần coach + $15 API + 15–20 HV pilot → **đổi lại**: báo cáo bằng chứng sau 2 tuần, chấp nhận dừng nếu metric fail | **Cả nhóm** |

## Phần B — Chuẩn bị 3 câu phản biện

Business owner/instructor sẽ hỏi mỗi nhóm 1–2 câu. Viết sẵn câu trả lời:

1. *"Số liệu / giả định này lấy ở đâu?"*
   → 80 học viên track Product lấy từ `00-context.md` (stakeholder cung cấp). Con số 2 câu/buổi và 5 phút/câu là ước tính nhóm — ghi rõ là giả định, cần validate bằng khảo sát 10 học viên trước khi chạy pilot thật.

2. *"Nếu giả định quan trọng nhất của bạn sai thì sao?"*
   → Giả định chính: học viên có ~160 câu/buổi cần tra Handbook. Nếu sai (học viên dùng Google thay vì hỏi AI), adoption thấp. Plan: nếu < 10 câu/3 ngày đầu pilot → khảo sát lý do ngay, không chờ hết 2 tuần. Kết luận dừng sớm nếu nhu cầu không đủ lớn.

3. *"Tình huống nào sẽ khiến bạn dừng pilot?"*
   → Dừng ngay khi: citation accuracy < 65% sau review 50 câu đầu **hoặc** AI trả lời sai gây hiểu nhầm ≥3 học viên. Quyền dừng thuộc Instructor — không phải nhóm tự quyết, tránh conflict of interest.

## Phần C — AI Support Log

| Câu hỏi | Trả lời |
|---|---|
| AI giúp được gì trong lab này? | Tách 7 use case từ Big Ask · chấm điểm 4 trục Quick Win · vẽ ASCII flow kiến trúc RAG · soạn nháp exit criteria và budget |
| AI đưa output nào nghe hợp lý nhưng nhóm phải sửa? | AI chấm #3 Glossary điểm cao nhất (4.70) nhưng nhóm phán đoán scope quá hẹp → chọn #1 Q&A (4.55) vì chứng minh đúng core value hơn. AI không tự nhận ra điều này. |
| Phần nào nhóm tự lập luận, KHÔNG copy AI? | Lý do chọn #1 thay vì #3 dù điểm thấp hơn · quyết định pilot 15–20 HV (không phải 80) · ngưỡng exit 65%/80% dựa trên bối cảnh thật của khóa · phán đoán "Buy sau khi pilot chứng minh nhu cầu" |

---

## Tổng kiểm tra trước khi nộp

| Hạng mục | Xong? |
|---|---|
| 5 slide, mỗi slide 1 thông điệp, đã phân ai nói slide nào | ✓ — Linh: S1+S2 · Điềm: S3+S4 · Cả nhóm: S5 |
| Slide 5 có lời xin rõ ràng (xin gì · hứa gì) | ✓ — Xin: 2h coach + $15 API + 15–20 HV · Hứa: báo cáo 2 tuần |
| Có câu trả lời sẵn cho cả 3 câu phản biện | ✓ |
| AI Support Log điền đủ 3 dòng | ✓ |
| Tất cả file worksheet/ đã commit + push, link dán vào Discord | / — cần làm sau |

Đây là file cuối. Pitch 5 phút + nhận phản biện theo bảng 5 Gate (`templates/rubric-gate-sheet.md`).

*Liên quan: handbook §A9 · `templates/5-slide-pitch.md` · `templates/ai-support-log.md`*
