---
artifact: 5 — Solution Approach + 6 — Demo/Mockup/Flow (bản nộp phase Solution)
bai-tap: Solution — chốt cách làm + cho stakeholder nhìn thấy
phase: Double Diamond vòng 2 · ◆ siết (chốt 1 cách làm + 1 artifact trực quan)
time: ~12 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-find-existing-solutions.md · 00-context.md · templates/demo-examples.md · prompts/05-demo-challenge.md
nop-cuoi: Có — bản nộp của phase Solution (Part B + C · A3 mục Solution Approach + Demo/Mockup/Flow)
---

# 2 — FINAL: Solution Approach + Demo/Mockup/Flow

Mục tiêu: chốt cách làm cho Quick Win (Build / Buy / Boost / Partner), nói rõ data & ai review cần có, và tạo 1 bản vẽ trực quan để stakeholder *nhìn* được. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 và là bản nộp của phase Solution.

Lý do làm bước này: hai cái bẫy. Một, "tự build" cho oai — trong khi 80–90% nhu cầu nội bộ chỉ cần Boost/Buy; tự build là quyết định khó rút lại nhất. Hai, chỉ nói bằng chữ — stakeholder không duyệt một đoạn văn, họ duyệt khi *nhìn thấy* flow. Không có bản vẽ → trượt Gate 4 dù lập luận tốt.

Quy tắc: **bản vẽ trực quan là BẮT BUỘC; demo chạy được chỉ là điểm cộng.** *Demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu.*

## Quy trình 12 phút

```text
4 phút  — Phần A: chốt Build/Buy/Boost/Partner (decision tree + ego check)
3 phút  — Phần B: data & ai review cần có
5 phút  — Phần C: vẽ 1 artifact trực quan + đánh dấu chỗ người review
```

---

## Phần A — Chốt cách làm

Đi decision tree, đừng chọn theo cảm giác:

```text
Bài này có phải LỢI THẾ CẠNH TRANH CỐT LÕI không?
 ├─ CÓ  → đội có AI engineer mạnh? CÓ → Build · KHÔNG → Boost
 └─ KHÔNG (chỉ là productivity layer) → có tool sẵn?
          CÓ → Buy · KHÔNG → Boost (model sẵn + data riêng)
```

Câu hỏi phụ:

- Nhóm chọn cách này vì *cần* hay vì *thích tự build*? Một câu thành thật.
- Hướng nào ở file `1` (đã tìm được người làm rồi) khớp với cách này — "đi từ 5 lên"?

### Trả lời

- **Cách làm chốt**: **Boost** — dùng LLM/API có sẵn + RAG đơn giản trên Handbook/Slide LMS + prompt bắt buộc citation + coach review mẫu trước khi mở rộng.

- **Lý do CẦN (không phải thích), 2–3 câu**:  
  Quick Win của nhóm là **Q&A có dẫn nguồn từ Handbook/Slide LMS**, không phải xây một LMS tutor platform đầy đủ. Mục tiêu của pilot là kiểm chứng xem học viên có thể tra câu trả lời trong tài liệu nhanh hơn, có nguồn rõ ràng hơn, và giảm câu hỏi lặp cho coach hay không. Vì vậy **Boost** là hướng phù hợp nhất: tận dụng model có sẵn, chỉ thêm dữ liệu khóa + retrieval + luật citation để chạy pilot nhỏ trong 1–2 tuần.

- **Vì sao KHÔNG "Build từ số 0"**:  
  Build từ số 0 sẽ kéo nhóm sang xây cả platform: đăng nhập, quản lý người dùng, tracking tiến độ, mini practice, personalization, dashboard... Những phần đó vượt scope Quick Win và dễ làm nhóm trượt trọng tâm. Với pilot đầu tiên, nhóm chưa cần chứng minh năng lực xây platform, mà cần chứng minh **Q&A có nguồn có đủ hữu ích và đủ an toàn để mở rộng hay không**.

- **Vì sao KHÔNG chọn Buy ngay**:  
  Buy một tool document QA/chatbot có sẵn có thể nhanh, nhưng nhóm chưa chắc kiểm soát được format citation theo yêu cầu khóa, rule "thiếu nguồn thì nói không biết", và cơ chế coach review 50 câu đầu. Buy có thể được cân nhắc sau nếu pilot chứng minh nhu cầu thật và cần triển khai rộng hơn.

- **Tool / API / vendor cần + ước lượng chi phí thô**:

| Hạng mục | Cần gì | Ghi chú |
|---|---|---|
| LLM/API | Một model có khả năng trả lời tiếng Việt/Anh tốt, bám context | Chưa chốt vendor cụ thể trong file này; có thể dùng OpenAI/Claude/Gemini tùy điều kiện lớp |
| Retrieval/RAG | Công cụ chia đoạn tài liệu, tìm 3–5 đoạn liên quan theo câu hỏi | Có thể prototype bằng script đơn giản hoặc framework RAG nhẹ |
| Data storage | Nơi lưu chunks + metadata citation | Metadata tối thiểu: tên tài liệu, section, trang nếu có |
| UI demo | Chatbox mockup hoặc standalone URL | Nếu LMS chưa cho embed, dùng demo mockup/standalone trước |
| Human review | Coach review 50 câu đầu | Dùng bảng review thủ công để đo citation accuracy |

> Ước lượng chi phí trong file này chỉ ở mức định tính vì nhóm chưa có giá API/vendor cụ thể. Chi phí sẽ được tách rõ hơn ở `03-pilot-plan/1-pilot-plan.md`.

---

## Phần B — Data & ai review (cách làm này cần gì để chạy được)

| Cần gì | Có sẵn trong AI20k? | Trong lab dùng (mẫu/giả định) | Privacy? |
|---|---|---|---|
| Data: Handbook / tài liệu hướng dẫn Day 28 | Có hoặc giả định có trong LMS/worksheet | Dùng các file handbook/worksheet/glossary được phép dùng trong lab | An toàn hơn vì là tài liệu khóa, không phải dữ liệu cá nhân |
| Data: Slide hoặc section LMS liên quan đến Product track | Chưa xác nhận định dạng | Nếu chưa có slide thật, dùng section từ worksheet/handbook hiện có | Chỉ dùng tài liệu học tập, không dùng log học viên |
| Data: 20–50 câu hỏi mẫu | Chưa có đủ, cần thu thập/giả định | Dùng câu hỏi mẫu như: "Pilot Plan khác Project Plan thế nào?", "Quick Win là gì?", "Double Diamond dùng để làm gì?" | Không chứa thông tin cá nhân |
| Metadata citation | Chưa rõ tài liệu có sẵn page/section chưa | Gắn metadata thủ công: tên tài liệu + section; nếu có PDF thì thêm trang | Không nhạy cảm |
| Review rubric | Chưa có sẵn | Tạo bảng review 3 tiêu chí: đúng nội dung, citation đúng, biết nói không biết | Không dùng điểm chính thức của học viên |

- **Output nào rủi ro cao**:
  1. AI trả lời sai nhưng nghe tự tin.
  2. AI bịa nguồn hoặc citation trỏ sai section/trang.
  3. AI trả lời câu hỏi ngoài phạm vi tài liệu thay vì nói "không biết".
  4. AI khiến học viên hiểu nhầm đây là câu trả lời chính thức thay cho coach/instructor.

- **Ai review + bao nhiêu mẫu + pass/fail theo gì**:  
  Coach hoặc instructor review **50 câu trả lời đầu tiên** trước khi mở rộng pilot. Mỗi câu được đánh giá theo 3 tiêu chí:

| Tiêu chí review | Pass khi | Fail khi |
|---|---|---|
| Đúng nội dung | Câu trả lời bám vào đoạn tài liệu được tìm thấy | Trả lời sai, thiếu ý chính, hoặc tự suy diễn ngoài tài liệu |
| Citation đúng | Nguồn trỏ đúng tài liệu + section/trang liên quan | Citation sai, mơ hồ, hoặc không có nguồn |
| Biết từ chối khi thiếu nguồn | Nếu không có nguồn đủ chắc, AI nói "chưa đủ nguồn" | AI vẫn trả lời dù không tìm thấy nguồn |

  **Ngưỡng pass ban đầu**: citation accuracy ≥ 80% sau khi coach review 50 câu đầu. Nếu dưới ngưỡng này, không mở rộng pilot; nhóm phải sửa pipeline retrieval/citation trước.

- **Có cần citation / nói "không biết" khi thiếu nguồn không**:  
  Có, đây là ràng buộc bắt buộc. Mọi câu trả lời phải có nguồn tối thiểu gồm **tên tài liệu + section**; nếu tài liệu có số trang thì thêm số trang. Nếu hệ thống không tìm thấy nguồn đủ chắc, câu trả lời phải là:

```text
Mình chưa tìm thấy nguồn đủ chắc trong tài liệu LMS để trả lời câu này. Bạn nên hỏi coach hoặc kiểm tra lại tài liệu gốc.
```

---

## Phần C — Bản vẽ trực quan (BẮT BUỘC)

Chọn **1** dạng nhẹ nhất đủ rõ: user flow + prompt/RAG flow. Stakeholder nhìn vào có thể hiểu học viên làm gì, AI xử lý thế nào, và coach review ở đâu.

```text
USE CASE: Q&A có dẫn nguồn từ Handbook/Slide LMS

Ví dụ câu hỏi:
"Pilot Plan khác Project Plan thế nào?"

┌─────────────────────────────┐
│ 1. Học viên hỏi trong LMS    │
│    hoặc chatbox demo         │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│ 2. Query Router              │
│ - Kiểm tra câu hỏi có thuộc  │
│   phạm vi tài liệu LMS không │
│ - Nếu quá ngoài phạm vi,     │
│   yêu cầu hỏi lại rõ hơn     │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│ 3. Retriever / RAG           │
│ - Tìm 3–5 đoạn liên quan     │
│   trong Handbook/Slide       │
│ - Lấy kèm metadata:          │
│   tên tài liệu, section/trang│
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│ 4. LLM Answer Generator      │
│ - Chỉ trả lời dựa trên       │
│   các đoạn nguồn tìm được    │
│ - Viết ngắn, dễ hiểu         │
│ - Không suy diễn ngoài nguồn │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│ 5. Citation Check            │
│ - Có nguồn không?            │
│ - Nguồn có đúng section không│
│ - Nếu thiếu nguồn → fallback │
└───────┬─────────────────────┘
        │
        ├── Nếu đủ nguồn
        │       ▼
        │  ┌─────────────────────────────┐
        │  │ 6A. Trả lời cho học viên     │
        │  │ - Câu trả lời ngắn           │
        │  │ - Citation: tài liệu/section │
        │  │ - Gợi ý đọc thêm             │
        │  └──────────────┬──────────────┘
        │                 │
        │                 ▼
        │  ┌─────────────────────────────┐
        │  │ 7. Feedback nhẹ từ học viên  │
        │  │ 👍 hữu ích / 👎 chưa đúng     │
        │  └─────────────────────────────┘
        │
        └── Nếu thiếu nguồn
                ▼
           ┌─────────────────────────────┐
           │ 6B. Fallback an toàn         │
           │ "Mình chưa tìm thấy nguồn    │
           │ đủ chắc trong tài liệu LMS.  │
           │ Bạn nên hỏi coach."          │
           └─────────────────────────────┘

CHỖ CON NGƯỜI REVIEW:
- Coach review 50 câu trả lời đầu tiên sau buổi pilot.
- Coach kiểm tra: câu trả lời đúng không, citation đúng không, AI có biết nói "không biết" không.
- Nếu citation accuracy < 80% → dừng mở rộng, sửa retrieval/citation pipeline.
```

### Sample input–output minh họa

```text
Input của học viên:
"Quick Win khác phần dễ nhất như thế nào?"

Output mong muốn:
Quick Win không đơn giản là phần dễ làm nhất. Trong AI Pilot Plan, Quick Win là lát cắt nhỏ chứng minh được giá trị nhanh, có người dùng thật và có người ủng hộ. Một phần rất dễ demo nhưng tác động hẹp vẫn có thể không phải Quick Win tốt.

Nguồn:
- Day 28 Glossary — mục "Quick Win"
- 01-frame/2-quick-win.md — phần "Lý do làm bước này"

Gợi ý đọc thêm:
Bạn nên đọc lại phần Quick Win Scoring để hiểu vì sao điểm số chỉ là gợi ý, không phải đáp án.
```

```text
Input của học viên:
"Dự án này có nên dùng AI để chấm điểm chính thức không?"

Output an toàn mong muốn:
Mình chưa tìm thấy nguồn đủ chắc trong tài liệu được index để kết luận việc chấm điểm chính thức. Tuy nhiên, trong ràng buộc lab, AI feedback/chấm bằng AI chỉ nên là formative và cần người review/calibrate trước khi dùng cho đánh giá chính thức.

Nguồn:
- 00-context.md — mục Ràng buộc mọi track phải tôn trọng: Formative ≠ summative
```

### Mini practice để ở phase sau

Track gốc có nhắc "mini practice", nhưng nhóm **không đưa mini practice vào Quick Win đầu tiên**. Lý do: mini practice phụ thuộc vào việc Q&A có nguồn hoạt động ổn định trước. Sau khi citation accuracy đạt ngưỡng và học viên dùng thật, phase sau có thể thêm bước:

```text
Sau câu trả lời có nguồn → AI tạo 1 câu hỏi luyện tập nhỏ dựa trên đúng đoạn nguồn vừa dùng.
```

---

## Rủi ro chính và cách giảm thiểu

| Rủi ro | Vì sao nguy hiểm | Cách giảm thiểu trong pilot |
|---|---|---|
| AI bịa nguồn hoặc citation sai | Làm học viên tin sai, vi phạm ràng buộc citation | Bắt buộc Citation Check; coach review 50 câu đầu; dưới 80% thì không mở rộng |
| Retrieval lấy sai đoạn tài liệu | LLM có thể trả lời sai dù prompt tốt | Bắt đầu với phạm vi tài liệu nhỏ: Handbook/Slide Day 28; chunk theo section; giữ metadata rõ |
| User hỏi ngoài phạm vi tài liệu | AI dễ trả lời theo kiến thức chung, không còn bám nguồn | Prompt bắt buộc: thiếu nguồn thì nói "không biết"; log lại câu hỏi ngoài scope |
| Học viên quá tin AI | AI chỉ là tutor hỗ trợ, không thay coach/instructor | UI/answer ghi rõ: "Câu trả lời dựa trên tài liệu được index, hãy kiểm tra nguồn" |
| Scope creep sang full tutor/mini quiz | Làm pilot nặng, khó hoàn thành | Giữ Quick Win: chỉ Q&A có nguồn; mini practice để phase sau |

---

## Tổng kiểm tra trước khi sang `../03-pilot-plan/`

| Hạng mục | Xong? |
|---|---|
| Cách làm có lý do CẦN, không phải "mặc định tự build" | ✓ — chọn Boost vì hợp Quick Win và budget nhỏ |
| Nói rõ data cần + ai review output rủi ro cao | ✓ — data, metadata citation, coach review 50 câu đầu |
| Có ≥1 bản vẽ trực quan, người ngoài hiểu trong ~20 giây | ✓ — có user flow/RAG flow ASCII |
| Có đánh dấu chỗ con người review | ✓ — coach review sau 50 câu đầu, ngưỡng citation accuracy ≥ 80% |

⚑ Coach kiểm tra ở Mốc 3: *"Stakeholder nhìn vào đâu để hiểu flow? Mockup/sketch/demo đâu?"* Chỉ nói bằng chữ = chưa qua.

Sau bước này, mở `../03-pilot-plan/1-pilot-plan.md`.

*Liên quan: handbook §A5+§A6 · `templates/demo-examples.md` · `prompts/05-demo-challenge.md`*
