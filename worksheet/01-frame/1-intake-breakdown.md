---
artifact: 1 — Track & Big Ask + 2 — Tool Breakdown
bai-tap: Frame — nghe đúng đề rồi tách nhỏ
phase: Double Diamond vòng 1 · ◇ giãn (nghe rộng, chưa chốt)
time: ~12 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 00-context.md · track card · prompts/01-breakdown.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 1 — Intake & Breakdown: nghe đúng đề, tách nhỏ

Mục tiêu: cả nhóm hiểu giống nhau "công cụ lớn stakeholder muốn", rồi tách nó thành 5–8 use case nhỏ làm được riêng. Đây là nửa "giãn ra" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1 — nghe rộng, tách rộng, chưa chọn.

Lý do làm bước này: hai cái bẫy chết người ở đây. Một, nhận đề literal ("làm con chatbot") rồi nhảy vào build — trong khi yêu cầu mơ hồ thường chỉ là triệu chứng. Hai, ôm cả công cụ lớn đi pitch "build cả platform" → trượt Gate 1 ngay. Tách nhỏ là động tác bắt buộc để từ "một ý tưởng to" sang "danh sách phần làm được".

Quy tắc: **nghe trước, tách trước, chưa chọn.** Bước này không được chốt Quick Win (việc đó ở file `2`).

## Bước 0 — Đọc track card + 00-context (2 phút)

Đọc track card được giao và `00-context.md` (mục 2 đã điền). Đừng lướt.

## Quy trình 12 phút

```text
2 phút  — Bước 0: đọc track card + context
4 phút  — Phần A: phát biểu lại Big Ask bằng lời nhóm
6 phút  — Phần B: tách 5–8 use case + check độc lập
```

---

## Phần A — Phát biểu lại Big Ask bằng lời nhóm

Đừng chép lại đề. Cả nhóm nói lại "công cụ lớn stakeholder muốn" bằng lời mình. Nếu 3 người nói 3 kiểu khác nhau → chưa hiểu giống nhau, bàn thêm.

Câu hỏi phụ (tự trả lời):

- Stakeholder nói họ muốn gì, và họ thực sự *cần* gì — có khác nhau không?
- "Tại sao bây giờ?" — ở quy mô ~500 người, cái gì đang đau khiến phải làm công cụ này lúc này?
- Ai là người dùng đầu tiên thật sự, không phải "cả khóa"?

### Trả lời

- **Big Ask, viết lại bằng lời nhóm (2–3 câu)**: Khóa AI20k có ~500 học viên với một kho tài liệu lớn (Handbook, Slide, tài liệu tham khảo) trên LMS. Thay vì học viên tự lục tìm hoặc phải đợi coach trả lời, nhóm muốn xây một AI tutor ngồi "bên trong" LMS, học viên hỏi thì AI trả lời ngay — có dẫn nguồn rõ tài liệu nào, trang nào. Mini practice (câu hỏi luyện tập) là phần mở rộng, chưa phải trọng tâm đầu tiên.
- **Tại sao bây giờ**: Quy mô ~500 người khiến coach không thể trả lời hết câu hỏi cá nhân. Học viên hỏi cùng một câu lặp đi lặp lại ("Pilot Plan khác Project Plan thế nào?") và không biết câu trả lời nằm ở đâu trong tài liệu dài.
- **Người dùng đầu tiên cụ thể**: Học viên track Product đang làm worksheet Day 28 — cần tra nhanh định nghĩa/khái niệm trong Handbook mà không cần thoát khỏi LMS.

## Phần B — Tách công cụ lớn thành 5–8 use case

Nhìn mục **Big Vision Modules** trong track card. Mỗi dòng = 1 use case làm được riêng, viết dạng *"AI làm X cho ai để họ Y"* — không phải tính năng mơ hồ. Cần 5–8 dòng (ít hơn 5 = chưa tách đủ; nhiều hơn 8 = đang liệt kê vụn).

| # | Use case (AI làm gì · cho ai · để họ làm được gì) | Người dùng | Làm được độc lập? |
|---|---|---|---|
| 1 | AI trả lời câu hỏi học viên **có dẫn nguồn** (tên tài liệu + section) từ Handbook/Slide trên LMS → học viên tự tra được ngay, không đợi coach | Học viên | **Có** |
| 2 | AI **tóm tắt nội dung** một bài giảng/slide cụ thể theo yêu cầu → học viên ôn nhanh trước buổi coaching hoặc lab | Học viên | **Có** |
| 3 | AI **giải thích thuật ngữ/khái niệm** (VD: "Double Diamond là gì?") dựa trên Handbook + Glossary của khóa → học viên không bị lạc khi gặp thuật ngữ lạ | Học viên | **Có** — glossary.md đã có sẵn |
| 4 | AI tạo **câu hỏi luyện tập (mini quiz)** từ nội dung bài học → học viên tự kiểm tra hiểu bài trước khi nộp assignment | Học viên | **Không hoàn toàn** — phụ thuộc #1 (cần RAG engine đọc tài liệu trước) |
| 5 | AI **gợi ý tài liệu liên quan** khi học viên hỏi một câu → học viên biết đào sâu ở đâu mà không cần tìm thủ công | Học viên | **Không** — phụ thuộc #1 (cùng cơ chế RAG) |
| 6 | AI **đưa feedback formative** cho bài nộp của học viên bằng cách đối chiếu với rubric/Handbook → học viên biết chỗ cần cải thiện trước khi coach chấm | Học viên | **Không** — cần rubric đã được calibrate bởi người, rủi ro cao |
| 7 | AI **hướng dẫn onboarding** cho học viên mới (tìm Discord, cách nộp bài, lịch lab) bằng hỏi-đáp → học viên mới không bị lạc tuần đầu | Học viên (mới) | **Có** |

Cần ít nhất **4 use case thật sự độc lập** (làm được mà không cần cái khác xong trước). Nếu nhiều cái phụ thuộc nhau → gộp hoặc viết lại cho tách bạch.

---

## Phát hiện ban đầu

- Use case **#1 (Q&A có nguồn)** là nền tảng — #4, #5 đều phụ thuộc vào nó. Nếu chọn Quick Win thì #1 là ứng viên rõ nhất: làm được độc lập, demo được ngay, giải quyết đúng pain point thật.
- Use case **#6 (Feedback bài nộp)** nghe hấp dẫn nhưng rủi ro cao nhất: cần human calibrate rubric trước, dễ sai → vi phạm ràng buộc "Human review" của track.
- Use case **#4 (Mini quiz)** liên quan đến Red Flag thứ 2 của track card (ranh giới “gia sư” vs “máy sinh đáp án”) — không nên chọn làm Quick Win vì phụ thuộc #1 và dễ làm học viên hỏi bot thay vì đọc tài liệu.
- 5/7 use case độc lập hoàn toàn → đủ điều kiện (yêu cầu ≥4).

## Câu hỏi mở (mang sang bước chọn Quick Win)

- Phạm vi tài liệu index ban đầu là gì? Chỉ Handbook, hay cả Slide + tài liệu tham khảo? (ảnh hưởng effort bước 1)
- Citation cần granular đến mức nào — đủ "Handbook §A1" hay cần số trang chính xác?
- Use case #7 (onboarding) có overlap với tool khác trong AI20k Learning OS không?

---

## Tổng kiểm tra trước khi sang `2-quick-win.md`

| Hạng mục | Xong? |
|---|---|
| Cả nhóm phát biểu lại Big Ask giống nhau, không cần nhìn card | ✓ |
| Có 5–8 use case dạng "AI làm X cho ai để Y" | ✓ — 7 use case |
| Có ≥4 use case thật sự độc lập | ✓ — 5 use case độc lập (#1, #2, #3, #4 phần nào, #7) |
| Nhóm KHÔNG còn ý định pitch "build cả platform" | ✓ — scope đã tách rõ |

Sau bước này, mở `2-quick-win.md` — chấm điểm chọn 1 lát cắt làm trước.

*Liên quan: handbook §A1+§A2 · `prompts/01-breakdown.md` · `00-context.md`*
