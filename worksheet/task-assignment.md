---
title: Task Assignment — Day 28 Lab
track: 02 / Interactive LMS Tutor
group: 2 người — Hứa Quang Linh + Dương Khoa Điềm
---

# Phân công task — Day 28 Lab

**Track**: 02 — Interactive LMS Tutor  
**Big Ask**: Biến tài liệu LMS thành tutor tương tác, hỏi-đáp có nguồn, mini practice.

> Quy tắc chung: người "chịu trách nhiệm" = người chốt bản cuối và đẩy lên repo. Cả hai vẫn cùng bàn trước khi chốt. Khi dùng AI, **luôn paste `00-context.md` vào đầu chat**.

---

## Tổng quan luồng làm việc

```
[Cả nhóm] Setup context
      ↓
[Linh] Bước 1 — Problem Framing (01-frame/)
      ↓  ← Điềm review trước khi chốt
[Điềm] Bước 2 — Solution Design (02-solution/)
      ↓  ← Linh review trước khi chốt
[Cả nhóm] Bước 3 — AI Pilot Plan + Pitch (03-pilot-plan/)
      ↓
[Cả nhóm] Pitch / nộp bài
```

---

## Bước 0 — Setup (Cả nhóm | ~5 phút đầu buổi)

| File | Việc cần làm | Ai điền |
|------|-------------|---------|
| [worksheet/00-context.md](00-context.md) | Điền mục 2 (Track số/tên, Big Ask) + mục 4 nếu cần | Cả nhóm thống nhất |
| [worksheet/group-members.md](group-members.md) | Điền tên nhóm, mã nhóm, repo GitHub | Linh tạo repo → điền link |

**Xong bước 0 khi**: `00-context.md` đã có track + big ask đầy đủ, `group-members.md` có link repo.

---

## Bước 1 — Problem Framing (Linh phụ trách | ~30 phút)

**Mục tiêu**: Tách Big Ask thành các tính năng nhỏ, chọn 1 Quick Win, viết Problem Statement rõ ràng.

### 1.1 — Intake Breakdown
- **File output**: [worksheet/01-frame/1-intake-breakdown.md](01-frame/1-intake-breakdown.md)
- **Prompt dùng**: [prompts/01-breakdown.md](../prompts/01-breakdown.md)
- **Việc làm**:
  1. Paste `00-context.md` vào đầu chat AI
  2. Dùng prompt `01-breakdown.md`, yêu cầu AI liệt kê các tính năng con của Track 02
  3. Điền kết quả vào file, ghi rõ: tính năng nào Phức tạp / Nhanh / Rủi ro
- **Điềm review**: đọc qua, comment nếu thiếu tính năng quan trọng

### 1.2 — Chọn Quick Win
- **File output**: [worksheet/01-frame/2-quick-win.md](01-frame/2-quick-win.md)
- **Prompt dùng**: [prompts/02-quick-win-challenge.md](../prompts/02-quick-win-challenge.md)
- **Việc làm**:
  1. Từ danh sách bước 1.1, dùng AI chấm điểm từng tính năng (Impact / Effort / Risk)
  2. Chọn 1 Quick Win: **ưu tiên "Q&A có dẫn nguồn từ Handbook"** vì đơn giản nhất, ít rủi ro nhất, demo được ngay
  3. Ghi lý do chọn (2–3 câu)
- **Template tham khảo**: [templates/quick-win-scoring.md](../templates/quick-win-scoring.md)

### 1.3 — Problem Framing (bản chốt)
- **File output**: [worksheet/01-frame/3-FINAL-problem-framing.md](01-frame/3-FINAL-problem-framing.md)
- **Prompt dùng**: [prompts/03-problem-framing-challenge.md](../prompts/03-problem-framing-challenge.md)
- **Việc làm**:
  1. Viết Problem Statement theo cấu trúc: *Who / Pain / Impact / Root cause*
  2. Linh chốt bản cuối → **gọi Điềm review trước khi commit**

**Xong bước 1 khi**: `3-FINAL-problem-framing.md` có Problem Statement rõ Who/Pain/Impact, Quick Win đã chọn và có lý do.

---

## Bước 2 — Solution Design (Điềm phụ trách | ~30 phút)

**Mục tiêu**: Đề xuất giải pháp cụ thể cho Quick Win đã chọn, phác thảo demo/mockup, đánh giá rủi ro.

### 2.1 — Khảo sát giải pháp hiện có
- **File output**: [worksheet/02-solution/1-find-existing-solutions.md](02-solution/1-find-existing-solutions.md)
- **Prompt dùng**: [prompts/04-find-solutions.md](../prompts/04-find-solutions.md)
- **Việc làm**:
  1. Paste `00-context.md` + tóm tắt Quick Win từ bước 1.2
  2. Yêu cầu AI liệt kê tool/API sẵn có phù hợp (RAG, LLM API, chatbot embed...)
  3. Ghi chú: tool nào phù hợp budget nhỏ, tool nào cần infra lớn → loại
- **Ràng buộc cần nhớ**: Citation bắt buộc, Budget nhỏ, Privacy (dùng data mẫu)

### 2.2 — Solution Design (bản chốt)
- **File output**: [worksheet/02-solution/2-FINAL-solution.md](02-solution/2-FINAL-solution.md)
- **Prompt dùng**: [prompts/05-demo-challenge.md](../prompts/05-demo-challenge.md)
- **Việc làm**:
  1. Chọn 1 stack giải pháp và phác thảo flow: *Học viên hỏi → AI lookup Handbook → trả lời + cite trang*
  2. Vẽ sơ đồ text-based (ASCII hoặc bullet flow) mô tả kiến trúc đơn giản
  3. Liệt kê 2–3 rủi ro chính + cách giảm thiểu
  4. Điềm chốt bản cuối → **gọi Linh review trước khi commit**
- **Template tham khảo**: [templates/demo-examples.md](../templates/demo-examples.md)

**Xong bước 2 khi**: `2-FINAL-solution.md` có stack giải pháp, flow mô tả được, rủi ro đã liệt kê.

---

## Bước 3 — AI Pilot Plan + Pitch (Cả nhóm | ~30 phút)

**Mục tiêu**: Viết AI Pilot Plan đủ để xin chạy pilot, chuẩn bị slide pitch 5 phút.

### 3.1 — AI Pilot Plan
- **File output**: [worksheet/03-pilot-plan/1-pilot-plan.md](03-pilot-plan/1-pilot-plan.md)
- **Prompt dùng**: [prompts/06-pilot-plan-challenge.md](../prompts/06-pilot-plan-challenge.md)
- **Phân công nội bộ**:

| Phần trong Pilot Plan | Người phụ trách |
|----------------------|----------------|
| Problem + Quick Win (copy từ bước 1) | **Linh** |
| Solution + Stack (copy từ bước 2) | **Điềm** |
| Pilot Scope (ai dùng, bao nhiêu người, bao lâu) | Cả nhóm bàn |
| Success Metrics (đo gì để biết thành công) | **Linh** |
| Risk & Mitigation | **Điềm** |
| Timeline (tuần 1–2 làm gì) | Cả nhóm bàn |

- **Template bắt buộc dùng**: [templates/ai-pilot-plan-core.md](../templates/ai-pilot-plan-core.md)

### 3.2 — Pitch Deck (bản chốt)
- **File output**: [worksheet/03-pilot-plan/2-FINAL-pitch.md](03-pilot-plan/2-FINAL-pitch.md)
- **Template tham khảo**: [templates/5-slide-pitch.md](../templates/5-slide-pitch.md)
- **Phân công nói slide** (điền tên vào file khi chốt):

| Slide | Nội dung | Người nói |
|-------|---------|-----------|
| 1 | Problem — Pain point học viên | Linh |
| 2 | Quick Win — Chọn gì, tại sao | Linh |
| 3 | Solution — Demo flow / mockup | Điềm |
| 4 | Pilot Plan — Scope + Metrics | Điềm |
| 5 | Ask — Cần gì để chạy pilot | Cả nhóm |

**Xong bước 3 khi**: `1-pilot-plan.md` đầy đủ các mục, `2-FINAL-pitch.md` đã phân slide rõ ai nói.

---

## Checklist nộp bài

- [ ] `worksheet/00-context.md` — đã điền track + big ask + ghi chú
- [ ] `worksheet/group-members.md` — đã điền tên nhóm + repo link
- [ ] `worksheet/01-frame/1-intake-breakdown.md` — đã có danh sách tính năng
- [ ] `worksheet/01-frame/2-quick-win.md` — đã chọn Quick Win + lý do
- [ ] `worksheet/01-frame/3-FINAL-problem-framing.md` — đã có Problem Statement
- [ ] `worksheet/02-solution/1-find-existing-solutions.md` — đã có danh sách giải pháp
- [ ] `worksheet/02-solution/2-FINAL-solution.md` — đã có stack + flow + rủi ro
- [ ] `worksheet/03-pilot-plan/1-pilot-plan.md` — đã đầy đủ các mục
- [ ] `worksheet/03-pilot-plan/2-FINAL-pitch.md` — đã phân slide ai nói
- [ ] Repo GitHub public, tất cả file đã push

---

## Lưu ý quan trọng

1. **Luôn paste `00-context.md` vào đầu mỗi chat AI mới** — AI không nhớ giữa các cuộc trò chuyện.
2. **Dùng data mẫu** khi demo — không dùng data thật của học viên.
3. **Mọi câu trả lời AI phải có nguồn** (tên tài liệu + trang/section) — đây là Red Flag #1 của track.
4. **Pilot đủ nhỏ**: target 10–20 học viên, 1–2 tuần, 1 tính năng duy nhất.
5. **Rubric chấm** nằm ở [templates/rubric-gate-sheet.md](../templates/rubric-gate-sheet.md) — đọc trước khi nộp.
