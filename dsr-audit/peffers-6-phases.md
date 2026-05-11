# DSR Process · Peffers 6 Phases

Retrofit LIFT development qua khung Peffers et al. (2007) DSR process model.
Source: `may26ws/lift.html` Act 04 — "Sáu phase Peffers — làm lại đúng cách".

Mục đích: documenting after the fact để xác nhận rigor, và codify quy trình
cho method tương lai (nếu phát triển method-<other>).

## Tổng quan

```
Problem ID  →  Objectives  →  Design & Dev  →  Demonstration  →  Evaluation  →  Communication
```

## Phase 1 · Problem Identification & Motivation

**Khi:** Pre-2026 (organic observation)
**Activities:**
- NAUCode practitioner observation: Hill Chart không phân biệt "thăm dò" vs "configure" trong LCNC
- Multiple project retrospectives: pattern lặp lại

**Output:**
- Problem statement (informal — chưa codify đến gần đây)
- Motivation: pricing model đang ép team optimize sai biến số

**Honest gap:** Phase 1 đã làm tacit, không document explicit cho đến Act 04
audit. Lesson: document earlier next time.

## Phase 2 · Objectives of a Solution

**Khi:** 2026-Q1
**Activities:**
- Articulate: cần artifact đo "đang ở đâu" trong LCNC project
- Articulate: artifact đó phải dùng được mà không cần code-counting

**Output:**
- Implicit objectives → mature thành Solution Pitch v0
- Pricing model objective: "đo cái khách quan, không phải effort"

## Phase 3 · Design & Development

**Khi:** 2026-Q1/Q2
**Activities:**
- Design Solution Pitch — 5 components artifact
- Design Certainty Units paradigm (Act 02 articulation)
- Sketch Certainty Engine workflow (Act 03)

**Output:**
- `artifacts/solution-pitch.md` (this repo)
- `artifacts/certainty-units.md`
- `artifacts/certainty-engine.md`

**Tool implementations:**
- `2ngnhan/lift-pitch` — UI prototype (React)
- `2ngnhan/propozel` — production platform

## Phase 4 · Demonstration

**Khi:** 2026-Q1 ongoing
**Activities:**
- Apply LIFT trên 5+ NAUCode internal projects
- Track Solution Pitch evolution per project
- Measure CU scoring against retrospective outcome

**Output:**
- Internal case material (anonymized — needs scrubbing before any external publish)
- Pattern catalog: stress-test questions that work per LCNC sub-domain

**Gap:** Public demonstration chưa có. Workshop May 26 là first step nhưng
audience nội bộ + academic, không phải buyer audience.

## Phase 5 · Evaluation

**Khi:** 2026-04 onwards
**Activities:**
- DSR audit (Act 04) — 5 trục
- Compare LIFT score predictions vs actual project outcomes
- Identify gaps (Certainty Engine explanation, literature grounding)

**Output:**
- [`dsr-audit/current-state.md`](current-state.md) — 5-trục assessment
- Open problems list (Certainty Engine explanation #1)

**Metrics tracked:**
- CU score at project start vs CU score at project end (delta = learning)
- Predicted-vs-actual scope creep events (when CU score should have flagged but didn't)
- Time saved per engagement (anecdotal — needs systematic measurement)

## Phase 6 · Communication

**Khi:** 2026-Q2 starting
**Activities:**
- Workshop 1 · AI Workflows for DSR (May 26 2026) — first communication
- This repo as ongoing documentation
- TODO: peer-reviewed publication
- TODO: industry conference talk

**Output so far:**
- `2ngnhan/may26ws` — workshop materials
- This repo — methodology spec
- Pending: paper, talk, blog post series (mkt-brand will handle)

**Communication audience strategy:**

| Audience | Channel | Status |
|---|---|---|
| Internal NAUCode team | Workshop + this repo | ✓ Done |
| Academic peers (VinUniversity MBA, DSR community) | Workshop deck + DSR primer (`may26ws/dsr.html`) | ✓ Started |
| Practitioners (consultants, project managers) | mkt-brand thought leadership content | TODO |
| Potential licensees | Direct presentation + case study (via ipcom) | TODO |
| Academic publication | Peer-reviewed venue (TBD) | TODO |

## Lessons applied to next method development

1. **Document Phase 1 explicit từ ngày 1** — đừng chờ retro
2. **Lit review trước Design & Development** — không phải after
3. **Demonstration sample size > 5 projects** trước khi self-report rigor
4. **Communication channel diversification** — academic + practitioner đồng thời
5. **Reflexive observation log** — track "what we changed our mind about" trong suốt 6 phases
