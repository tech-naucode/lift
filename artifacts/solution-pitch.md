# LIFT Solution Pitch — 5 Components

**Trạng thái:** Spec draft. Nguồn chính: `2ngnhan/may26ws/lift.html` slide 07.

## Mục đích

Khi một LCNC project bắt đầu, team không có syntax để đếm. Solution Pitch là
**artifact đầu vào** của LIFT — buộc thinking phải explicit ở 5 chiều trước
khi bắt đầu execution. Mỗi component tương ứng với một loại unknown cần
chuyển thành validated.

## 5 thành phần

> TODO: Extract chi tiết từng component từ deck (slide 07).

| # | Component | Câu hỏi cần trả lời | Validated khi |
|---|---|---|---|
| 1 | TODO — Component 1 | TODO | TODO |
| 2 | TODO — Component 2 | TODO | TODO |
| 3 | TODO — Component 3 | TODO | TODO |
| 4 | TODO — Component 4 | TODO | TODO |
| 5 | TODO — Component 5 | TODO | TODO |

(Khung tạm — fill content từ may26ws/lift.html slide 07. Workshop deck có
visual layout của 5 cards.)

## Cách sử dụng

1. Tại Project Kickoff: team draft Solution Pitch
2. AI Certainty Engine stress-test mỗi component (xem [`certainty-engine.md`](certainty-engine.md))
3. Score → Certainty Units cho từng component (xem [`certainty-units.md`](certainty-units.md))
4. Roll-up thành Project Certainty Score → pricing input + go/no-go decision
5. Re-score weekly trong suốt engagement

## Quan hệ với Propozel platform

Propozel UI là nơi consultant nhập Solution Pitch + xem Certainty Score real-time.
Repo `2ngnhan/lift-pitch` là UI prototype độc lập (offline).

## Anti-patterns

- ❌ Skip components vì "nhỏ" — Solution Pitch incomplete = pricing input sai
- ❌ Update 1 component mà không re-score toàn bộ — components có dependency
- ❌ Treat Solution Pitch như static document — phải re-score per sprint
- ❌ Để AI tự fill components — practitioner judgment là input chính, AI chỉ stress-test

## Version control

Mỗi Solution Pitch là 1 file trong `engagement-*/discovery/output/solution-pitch_*.md`.
Snapshot vào `versions/internal-use/` khi pattern ổn định.
