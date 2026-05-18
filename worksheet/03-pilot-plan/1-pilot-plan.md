---
artifact: 7 — AI Pilot Plan core
bai-tap: Pilot Plan — cam kết hai chiều: xin – hứa – đo – dừng
phase: Double Diamond vòng 2 · ◇ giãn → ◆ siết (liệt kê hết rồi chốt gọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 02-solution/2-FINAL-solution.md · 00-context.md · prompts/06-pilot-plan-challenge.md
nop-cuoi: Không — file trung gian (bản nộp ở 2-FINAL-pitch.md)
---

# 1 — AI Pilot Plan core

Mục tiêu: viết phần kế hoạch xin pilot — scope, người, data, budget, timeline, metric, exit criteria, adoption, lời hứa, lời xin. Bước này giãn ra (liệt kê hết những thứ cần) rồi siết lại (chốt bản gọn đủ để stakeholder quyết).

Lý do làm bước này: đây là thứ stakeholder dùng để **quyết approve hay dừng**. AI Pilot Plan **không phải proposal xin tiền** — là *cam kết hai chiều*: nhóm xin nguồn lực, đổi lại hứa giao evidence + chấp nhận dừng nếu metric fail. Demo đẹp mà không nói được "xin gì, hứa gì, đo gì, dừng khi nào" → trượt Gate 5.

Quy tắc: **budget tách từng hạng mục, không gộp 1 cục; không có mục "miscellaneous".** Exit criteria phải có người có quyền thực thi, không chỉ trên giấy.

## Quy trình 10 phút

```text
6 phút  — Điền 10 mục core (kéo nguyên liệu từ 00 + 01-frame + 02-solution)
3 phút  — Phần exit criteria + adoption (chỗ nhóm hay bỏ quên)
1 phút  — Tự phản biện
```

---

## 10 mục core

Câu hỏi phụ (tự trả lời):

- Nếu tóm vấn đề không gọn trong 1 câu → nhóm chưa hiểu vấn đề.
- Exit criteria của nhóm có ai DÁM thực thi khi sếp vẫn thích pilot không?
- Adoption: ai dùng đầu tiên — không phải "cả khóa ~500 người"?

### Trả lời

1. **Tóm vấn đề** (1 câu):
   Học viên track Product mất 5–10 phút tra Handbook mỗi lần gặp khái niệm lạ khi làm worksheet, dồn ~160 câu/buổi lên coach — 70–80% không được giải đáp trong giờ lab.

2. **Cách làm + lý do**:
   **Boost** — LLM API có sẵn + RAG đơn giản trên Handbook/Slide LMS + prompt bắt buộc citation + coach review mẫu trước khi mở rộng.
   Không Build vì: Quick Win không cần platform, chỉ cần chứng minh Q&A có nguồn đủ hữu ích và an toàn.
   Không Buy ngay vì: chưa chắc kiểm soát được rule citation và cơ chế human review theo yêu cầu khóa.

3. **Scope pilot**:
   - Phục vụ: **15–20 học viên track Product** (volunteer), không phải cả 80 người ngay
   - Thời lượng: **2 tuần**
   - **2 phase**: Phase 1 (tuần 1) — setup + test nội bộ · Phase 2 (tuần 2) — pilot thật với học viên trong buổi lab

4. **Người**:
   - Nhóm làm: Hứa Quang Linh (Problem Framing + Metrics) · Dương Khoa Điềm (Solution + RAG pipeline)
   - Review output rủi ro cao: **Coach/Instructor** review 50 câu trả lời đầu tiên (3 tiêu chí: đúng nội dung · citation đúng · biết nói "không biết")
   - Quyết approve/dừng: **Instructor hoặc PM AI20k**

5. **Data**:
   - Dùng (trong lab): Handbook Day 28 (Markdown có sẵn) + `glossary.md` + worksheet templates — tài liệu khóa đã public, không phải data học viên
   - 20–50 câu hỏi mẫu giả định (VD: "Quick Win là gì?", "Pilot Plan khác Project Plan thế nào?", "Double Diamond dùng để làm gì?")
   - Privacy: không index bài nộp / log hành vi học viên; chỉ tài liệu học tập
   - Citation: mọi câu trả lời phải kèm **tên tài liệu + section**; thiếu nguồn = fallback "chưa tìm thấy nguồn, hỏi coach"

6. **Budget** (từng hạng mục):
   - API/tool: ~$10–15/2 tuần *(ước tính: 20 học viên × 5 câu/ngày × 14 ngày × ~$0.003/câu)*
   - Thời gian nhóm: ~4h setup pipeline + 2h/tuần monitoring = ~8h tổng
   - Thời gian coach: ~2h review 50 câu đầu (tuần 1)
   - Hạng mục ẩn: 30 phút brief học viên cách dùng · re-index nếu tài liệu được cập nhật giữa pilot

7. **Timeline + cổng**:
   - **Phase 1 (tuần 1)**: Index Handbook + RAG pipeline + test 20 câu nội bộ
     → **Cổng 1**: citation accuracy ≥ 80% trên 20 câu test nội bộ · coach xác nhận chất lượng mẫu
   - **Phase 2 (tuần 2)**: Mở cho 15–20 học viên dùng thật trong buổi lab
     → **Cổng 2**: ≥ 50% học viên dùng ≥1 câu · coach xác nhận không có câu gây hiểu sai

8. **Metrics**:

| Metric | Đo bằng gì · ai đo | Baseline | Ngưỡng đạt |
|---|---|---|---|
| Citation accuracy | Coach chấm 50 câu đầu theo 3 tiêu chí (đúng nội dung / citation đúng / biết từ chối) | 0% (chưa có hệ thống) | **≥ 80%** |
| Tỷ lệ học viên dùng | Đếm số học viên có ≥1 câu hỏi trong log (không phân tích nội dung) · nhóm đo | 0 (chưa có tool) | **≥ 50%** trong 15–20 người pilot |
| Câu hỏi lặp gửi coach | Coach ước lượng định tính sau phase 2 | ~30–40 câu lặp/buổi (giả định) | Coach nhận thấy giảm rõ rệt |

   **Leading indicator** (biết sớm trong tuần 1): phản hồi định tính của coach sau 10 câu đầu tiên — "đọc được không? citation có trỏ đúng không?"

9. **Exit criteria**:

| Mức | Điều kiện | Hành động | Ai có quyền dừng |
|---|---|---|---|
| Cảnh báo | Citation accuracy 65–80% sau 50 câu đầu | Sửa prompt/retrieval pipeline; chưa mở sang Phase 2 | Nhóm + Coach |
| Nghiêm trọng | Citation accuracy < 65% **HOẶC** AI trả lời sai gây hiểu nhầm ≥3 học viên | Dừng pilot ngay; không mở rộng | **Instructor** |

   *Red Flag check*: Exit criteria nghiêm trọng chặn được cả 2 Red Flag: (1) BỊ nội dung/không có nguồn → bị chặn qua Citation Check + ngưỡng 80%; (2) Không rõ ranh giới gia sư vs máy sinh đáp án → fallback “không biết” + Formative only + scope chỉ Q&A không mở mini practice.

10. **Adoption**:
    - Ai dùng đầu tiên: 15–20 học viên track Product, tự nguyện, trong buổi lab Day 28+
    - Workflow đổi: thêm bước "hỏi AI tutor trước khi post Discord/hỏi coach"
    - Train/support: brief 5 phút đầu buổi + link chatbox demo
    - Nếu không ai dùng: khảo sát 3 học viên không dùng (vì sao?) → điều chỉnh UX hoặc kết luận "nhu cầu không đủ lớn để scale"

11. **Lời hứa**:
    Cuối 2 tuần giao báo cáo gồm: citation accuracy thực tế · tỷ lệ học viên dùng · top 5 loại câu hỏi phổ biến nhất · lỗi thường gặp · đề xuất rõ ràng: **mở rộng** (nếu cả 2 cổng pass) hoặc **dừng + lý do** (nếu không).

12. **Lời xin**:
    - **Xin**: 2h/tuần của 1 coach để review 50 câu đầu · cho phép pilot 15–20 học viên track Product · ~$15 API budget
    - **Đổi lại**: báo cáo bằng chứng sau 2 tuần để stakeholder quyết mở rộng hay dừng
    - **Mức rủi ro**: thấp — formative only, có human review, không ảnh hưởng điểm, chỉ 15–20 người, tài liệu nguồn đã public

---

## Tự phản biện

- **Budget thiếu hạng mục ẩn không?** → Đã thêm: brief học viên 30 phút + re-index khi tài liệu cập nhật. Còn 1 ẩn: nếu LMS không cho embed chatbox, cần thêm ~2h setup standalone URL.
- **Exit criteria đủ mạnh để thật sự dừng không?** → Mức nghiêm trọng giao quyền dừng cho Instructor (không phải nhóm tự quyết) — đủ để thực thi ngay cả khi nhóm muốn tiếp tục.
- **Giả định quan trọng nhất sai → plan gì?** → Giả định: học viên có đủ 160 câu/buổi. Nếu sai (học viên dùng Google thay vì hỏi), adoption thấp. Plan: nếu < 10 câu/buổi sau 3 ngày pilot → khảo sát lý do, không chờ hết 2 tuần.

---

## Tổng kiểm tra trước khi sang `2-FINAL-pitch.md`

| Hạng mục | Xong? |
|---|---|
| Tóm vấn đề trong 1 câu | ✓ |
| Budget tách hạng mục, không "miscellaneous" | ✓ — 4 hạng mục rõ |
| Metric có baseline + ngưỡng + ai đo | ✓ — 3 metric, coach đo |
| Exit criteria có người có quyền thực thi (≥2 mức) | ✓ — Cảnh báo (nhóm+coach) · Nghiêm trọng (Instructor) |
| Adoption: chỉ rõ ai dùng đầu tiên (không "cả khóa") | ✓ — 15–20 HV volunteer track Product |

⚑ Coach kiểm tra ở Mốc 4: *"Xin gì? Hứa gì? Đo gì? Dừng khi nào?"*

Sau bước này, mở `2-FINAL-pitch.md` — dồn tất cả thành 5-slide pitch + AI Support Log.

*Liên quan: handbook §A7+§A8 · `templates/ai-pilot-plan-core.md` · `prompts/06-pilot-plan-challenge.md`*
