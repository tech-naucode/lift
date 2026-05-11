---
schema: agentcompanies/v1
kind: company
slug: lift
name: LIFT Method
description: >
  Methodology IP asset. LIFT is NAUCode's framework for measuring project
  progress in low-code/no-code contexts where Shape Up's Hill Chart fails.
  Core artifacts: Solution Pitch (5 components), Certainty Units
  (unknown→validated metric), Certainty Engine (stress-test algorithm).
  Developed under the Design Science Research framework. This repo holds
  the methodology spec — the platform that operationalizes it is propozel.com,
  and the operational application lives in tech-naucode/consult.
version: 0.1.0
license: proprietary
tags:
  - method
  - lift
  - certainty-units
  - dsr
  - ip-asset
metadata:
  parent_org: NAUCode
  primary_language: vi
  asset_type: methodology-ip
  dsr_layer: 5
  content_source:
    workshop_repo: https://github.com/2ngnhan/may26ws
    workshop_deck: https://github.com/2ngnhan/may26ws/blob/main/lift.html
    workshop_portal: https://github.com/2ngnhan/may26ws/blob/main/index.html
  related_repos:
    operational_application: tech-naucode/consult
    platform_implementation: https://github.com/2ngnhan/propozel
    ui_prototype: https://github.com/2ngnhan/lift-pitch
  approval_required: true
  human_operator: principal-consultant
---

# LIFT Method

> **Đo sự chuyển dịch từ unknown sang validated — không phải đo effort.**

## Một câu

LIFT là phương pháp đo tiến độ dự án trong bối cảnh **low-code / no-code**, nơi
Shape Up's Hill Chart không phân biệt được "đang thăm dò có làm được không" và
"đang cấu hình cái đã biết" — dù cả hai cùng trông như "in progress" trên
burndown chart.

## Core artifacts

- **LIFT Solution Pitch** — 5 components artifact ([artifacts/solution-pitch.md](artifacts/solution-pitch.md))
- **Certainty Units** — metric thay thế story points trong era AI-augmented ([artifacts/certainty-units.md](artifacts/certainty-units.md))
- **Certainty Engine** — algorithm stress-test claim trước khi commit execution ([artifacts/certainty-engine.md](artifacts/certainty-engine.md))

## 5-Act narrative

LIFT được phát triển theo Design Science Research (DSR). Hành trình từ
practitioner observation đến framework có Rigor — xem [`5-acts-overview.md`](5-acts-overview.md).

## DSR audit

LIFT hiện ở **Layer 5** của DSR scaffolding. Audit chi tiết 5 trục
(Relevance / Rigor / Design / Demonstration / Communication) trong
[`dsr-audit/current-state.md`](dsr-audit/current-state.md).

## Versioning

```
versions/
├── draft/             ← work-in-progress, không deploy
├── internal-use/      ← dùng trong consult engagements
├── client-licensed/   ← licensed cho khách cụ thể
└── public-release/    ← phiên bản công khai (chưa có)
```

## Cross-references

Xem [`links.md`](links.md) cho map đầy đủ tới may26ws, consult, propozel,
lift-pitch và các artifact bên ngoài.

## License model

Xem [`license-models.md`](license-models.md). Mặc định: proprietary, tham vấn
`ip-com` cho licensing options.
