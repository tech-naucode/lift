# Certainty Units

**Trạng thái:** Spec draft. Nguồn chính: `may26ws/lift.html` Act 02-03.

## Paradigm

> **Story Points đo effort tương đối** — hữu ích khi implementation là
> bottleneck. **Certainty Units đo sự chuyển dịch từ unknown sang validated** —
> hữu ích khi direction là bottleneck.

Trong AI era, effort gần như vô hạn → bottleneck dịch chuyển. Certainty là
metric duy nhất còn ý nghĩa.

## Định nghĩa

1 Certainty Unit (CU) = 1 đơn vị giảm uncertainty về một claim cụ thể trong
Solution Pitch, đo bằng:

- Bằng chứng (evidence) đã collect
- Test case đã pass
- Stakeholder confirmation đã có
- Constraint đã được explicit

## Scoring rubric (đang draft)

> TODO: Codify rubric. Hiện đang là tacit knowledge của Principal. Phải document
> để team junior + AI Certainty Engine cùng dùng được.

| Level | Tên | Đặc điểm | Score |
|---|---|---|---|
| L0 | Speculation | Không có evidence, chỉ assumption | 0 CU |
| L1 | Hypothesis | Có 1 reference, chưa test | 1 CU |
| L2 | Tested-once | Đã chạy 1 test case nhỏ | 3 CU |
| L3 | Tested-multiple | Multiple test cases pass | 5 CU |
| L4 | Validated-with-stakeholder | Stakeholder đã confirm trong real context | 8 CU |
| L5 | Production-evidence | Đã chạy trong production của tương tự case | 13 CU |

(Fibonacci-like để đảm bảo distinction giữa levels. Total CU per project =
sum across all 5 components × multiplier per scope.)

## Khác biệt với Story Points

| | Story Points | Certainty Units |
|---|---|---|
| Đơn vị | Effort tương đối | Knowledge state transition |
| Reference point | "Story này so với story kia" | "Claim này so với claim chính nó hôm qua" |
| Đo ở thời điểm nào | Sprint planning | Continuous (re-score weekly) |
| Bottleneck giả định | Implementation | Direction / decision |
| AI tác động ra sao | Devalues (AI làm cheap) | Amplifies (AI stress-tests) |

## Anti-patterns

- ❌ "Cho project này 50 CU" mà không break down 5 components — score per
  component mới meaningful
- ❌ Equate CU với hours — pricing per CU không phải pricing per hour relabeled
- ❌ AI tự score CU — AI stress-tests, practitioner scores
- ❌ Backfill CU sau khi delivered — score phải trước commit execution

## Pricing implication

Xem `2ngnhan/may26ws/lift.html` Act 05 slide "Tính theo engagement".

Tóm tắt: 1 engagement giá X được tuyên bố là "delivering Y CU of certainty
across [scope]." Khi engagement closed:

- CU delivered ≥ Y → success, full payment
- CU delivered < Y với rõ root cause → partial + retro
- CU delivered ≫ Y → scope creep flag, không bonus (CU không phải for-profit
  metric của team)

## Open problem

Certainty Engine chưa giải thích được vì sao nó chấm điểm X cho 1 dự án cụ
thể. Đây là hướng research tiếp theo. Detail trong [`certainty-engine.md`](certainty-engine.md).
