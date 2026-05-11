# Certainty Engine

**Trạng thái:** Sketch — chưa phải production spec. Nguồn: `may26ws/lift.html`
Act 03-05.

## Mục đích

Cho mỗi claim trong LIFT Solution Pitch, Certainty Engine **đặt câu hỏi khó**
(stress-test) trước khi team cam kết execution. Là cơ chế để tăng Certainty
Units có hệ thống thay vì dựa vào "feeling".

## Nguyên tắc cốt lõi

> **Stress-test, not replace.**

AI engine không quyết định **đặt cược vào claim nào** — đó là việc của
practitioner. AI chỉ:

1. Generate stress-test questions từ claim
2. Surface evidence gaps
3. Flag claim quá tự tin so với evidence
4. Đề xuất next-step để raise Certainty level

## Workflow

```
[Solution Pitch claim]
        │
        ▼
Certainty Engine generates 3-7 stress-test questions
        │
        ▼
Practitioner answers OR flags "need evidence"
        │
        ▼
Engine scores current CU level cho claim đó
        │
        ▼
Roll-up: 5 components × CU per component = Project Certainty Score
        │
        ▼
Score < threshold? → Suggest discovery actions
Score ≥ threshold? → Green-light execution
```

## Stress-test question patterns

Engine sinh câu hỏi dạng:

- **Evidence question:** "Bạn có dẫn chứng X trong context Y không?"
- **Boundary question:** "Claim này còn đúng khi [edge case] không?"
- **Dependency question:** "Component A đang giả định Component B đã validated — đã validate chưa?"
- **Reversibility question:** "Nếu sai, mất bao nhiêu để revert?"
- **Stakeholder question:** "Stakeholder Z đã ack điều này chưa, hay chỉ team nội bộ tự thống nhất?"

(Library đầy đủ sẽ ở `artifacts/stress-test-patterns.md` — TODO)

## Open problem

> Certainty Engine **chưa giải thích được** vì sao nó chấm điểm X cho một dự
> án cụ thể.

Nói cách khác: scoring là một black-box ở mức hiện tại. Đây là hướng research
chính của LIFT trong các Act tiếp theo.

Hướng tiếp cận đang cân nhắc:

1. Explanation-by-tracing — log mọi stress-test question + answer, tổng hợp
   thành explanation tự nhiên.
2. Counterfactual scoring — "Nếu claim A có evidence thì score sẽ là Y thay vì X."
3. Calibration với historical engagements — score thực vs outcome thực.

## Implementation note

Certainty Engine **chỉ tồn tại như spec ở repo này**. Implementation thực sẽ
chạy bên trong:

- Propozel platform (`2ngnhan/propozel`) — production deployment
- Consult agent layer (`tech-naucode/consult`) — orchestration of engine calls

Repo `lift` define **what + why**. Propozel implement **how**.

## Anti-patterns

- ❌ Engine auto-approve khi score ≥ threshold — practitioner phải re-confirm trước commit
- ❌ Engine sinh > 10 stress-test questions cho 1 claim — quá tải, mất focus
- ❌ Engine reuse stress-test pattern chung cho mọi domain — phải tune per
  vertical (LCNC, custom dev, data engineering, etc.)
- ❌ Treat engine output như authority — engine là tool, không phải oracle

## Backlog

- [ ] Library stress-test patterns per vertical
- [ ] Calibration dataset từ NAUCode historical engagements
- [ ] Explanation API spec
- [ ] Integration spec với Propozel platform
- [ ] User study với senior consultant: engine có align với judgment không?
