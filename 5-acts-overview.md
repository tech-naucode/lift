# LIFT — 5-Act Narrative

Tóm tắt hành trình phát triển LIFT theo Design Science Research. Mỗi Act tương
ứng với một giai đoạn thực tế trong nghiên cứu. Đọc theo thứ tự để theo
hành trình từ practitioner observation đến framework có Rigor.

Source nguyên bản: deck trong `2ngnhan/may26ws/lift.html`.

---

## Act 01 · LCNC reality

**Slide marker:** Act 01 · LCNC reality + Act 01 · The artifact emerges

### Observation

NAUCode làm WordPress, FlutterFlow, WooCommerce. **Không syntax. Không pull
request. "Code" là configure plugin, kéo thả component.**

Shape Up's Hill Chart **gần đúng** — nhưng thiếu một thứ: nó không phân biệt
được hai trạng thái rất khác nhau mà cùng trông như "in progress":

| Trạng thái | "Đang tìm hiểu xem được không" | "Đang cấu hình thứ đã biết" |
|---|---|---|
| Plugin X có làm được yêu cầu Y? | Chưa biết | Đã biết được |
| Rủi ro | Cao | Thấp |
| Time-to-resolve | Bất định | Ước tính được |
| Hành động | Thăm dò, chưa cam kết | Thực thi |

**Burndown chart không phân biệt được.** Status meeting chỉ thấy "in progress".
Nhưng người quản lý cần biết đó là loại "in progress" nào.

### Artifact emerges

**LIFT Solution Pitch** — câu trả lời thực hành cho câu hỏi: làm sao biết
mình đang ở đâu trong một dự án không có code để đếm? 5 thành phần.

Detail: [`artifacts/solution-pitch.md`](artifacts/solution-pitch.md)

### DSR audit Act 01

- **Relevance:** ✓ vấn đề có thực
- **Rigor:** ✗ chưa có lý thuyết bệ đỡ. Đổi mới do practitioner tạo ra.
- Pattern của Agile, Lean, Shape Up — và LIFT giai đoạn này cũng vậy.

---

## Act 02 · The hidden axiom

**Slide marker:** Act 02 · Hệ thống đang đo sai đơn vị · Why Effort Assumption is wrong

### Insight

Câu hỏi đặt ra trong workshop NAUCode: tại sao các framework cũ (Agile, Shape
Up) gặp khó khi gặp LCNC + AI?

Trả lời qua **ba lens**:

1. **Frederick Taylor · 1911** — Scientific management cho factory work.
   Trong context đó, effort và output có tương quan rõ ràng. Story Points
   thừa hưởng giả định này.
2. **Knowledge work ≠ factory work.** Một giờ "figuring out plugin X" có thể
   định đoạt cả tuần execution phía sau. Effort như nhau, impact khác hoàn toàn.
3. **AI thay đổi giả định gốc.** Khi AI tạo ra effort gần như vô hạn, đo
   effort không còn có ý nghĩa — phải đo cái khác.

### Articulated axiom

> **Certainty Assumption** — giá trị tạo ra không phải lúc nỗ lực bỏ ra, mà
> lúc một câu hỏi chưa biết được trả lời thành validated.

Detail: [`artifacts/certainty-units.md`](artifacts/certainty-units.md)

---

## Act 03 · Paradox + the only meaningful metric

**Slide marker:** Act 03 · Paradox + The only meaningful metric

### Paradox

Khi đội bắt đầu dùng AI nhiều hơn:
- **Chạy nhanh hơn đáng kể.**
- **Không ai chắc chắn hơn về hướng đi.**

Tốc độ tăng, nhưng decision quality không tăng — đôi khi giảm. Vì sao?

### Trả lời

Story Points đo effort tương đối — **hữu ích khi implementation là bottleneck**.
Mất tác dụng khi effort được AI tạo ra với chi phí gần bằng 0.

**Certainty Units** đo sự chuyển dịch từ unknown sang validated. **Không thay
thế story points — thay thế chính paradigm "đo effort".**

| | Story Points | Certainty Units |
|---|---|---|
| Đo gì | Effort tương đối | Sự dịch chuyển unknown→validated |
| Khi nào hiệu quả | Implementation là bottleneck | Direction & decision là bottleneck |
| Bottleneck trong AI era | Đã giải tỏa (AI làm effort cheap) | Đang trở thành bottleneck thật |

---

## Act 04 · DSR audit · Where LIFT stands today

**Slide marker:** Act 04 · Where LIFT actually stands today + Lessons · DSR Layer 5

### Stress-test, not replace

**AI được phép đặt câu hỏi khó cho từng claim trong Solution Pitch** — công cụ
để tăng certainty trước khi cam kết execution. Nhưng quyết định "đặt cược vào
claim nào" vẫn thuộc về người làm.

### Audit 5 trục

Chi tiết: [`dsr-audit/current-state.md`](dsr-audit/current-state.md)

- **Relevance:** mạnh — vấn đề từ thực tế NAUCode
- **Rigor:** trung bình — vẫn thiếu literature grounding cho Certainty Engine scoring
- **Design Cycle:** đã có separation build/measure
- **Demonstration:** đã chạy trên 5+ projects nội bộ
- **Communication:** mới qua 1 workshop

### Khoảng trống còn lại

> Certainty Engine chưa giải thích được vì sao nó chấm điểm X cho một dự án
> cụ thể — đây là hướng nghiên cứu tiếp theo.

### Lessons cho AI-augmented researcher (4 principles)

(Extract từ slide deck — sẽ paste vào `dsr-audit/peffers-6-phases.md` ở
phase Communication.)

---

## Act 05 · Framework biến thành sản phẩm

**Slide marker:** Act 05 · Nơi làm = Nơi đo + Cách định giá là một dạng tuyên bố + Team in this room

### Ba khối xây dựng cốt lõi

1. **LIFT framework** — methodology spec (repo này)
2. **Certainty Engine** — algorithm (repo này, artifacts/)
3. **Propozel** — platform: nơi làm = nơi đo. `propozel.com`

### Khoảnh khắc quan trọng nhất từ góc độ DSR

Khi framework không còn là tài liệu — mà trở thành **system of work + system of
measure trùng một chỗ**. Propozel là minh chứng: consultant làm việc trên đó,
và certainty của project tự lộ ra khỏi chính dữ liệu đang được produce.

### Cách định giá là một dạng tuyên bố

| Mô hình cũ | Mô hình LIFT |
|---|---|
| Bán theo giờ | Tính theo engagement |
| Effort Assumption thể hiện trong pricing | Certainty Assumption dịch ra mô hình kinh tế |
| Khách và team cùng tối ưu một biến số sai | Khách mua **"một đơn vị sự chắc chắn được giao"** — không phải một đơn vị "công sức đã bỏ ra" |

### Team in this room

Đây không chỉ là một case study — đây là **company họ đang build** (NAUCode +
Propozel). Reflexive observation: phương pháp đang được sản phẩm hóa bởi
chính team phát triển nó.

---

## Năm câu hỏi để đem về

(Workshop closing — slide cuối)

TODO: extract từ slide cuối của may26ws/lift.html

---

## Trục thời gian

| Mốc | Sự kiện |
|---|---|
| Pre-2026 | Practitioner-led observation tại NAUCode LCNC projects |
| 2026-Q1 | Solution Pitch artifact hình thành (Act 01) |
| 2026-Q1/Q2 | Certainty Assumption articulated (Act 02) |
| 2026-Q2 | Certainty Units + Engine sketch (Act 03) |
| 2026-04 | DSR audit lần đầu — Layer 5 (Act 04) |
| 2026-05-26 | Workshop 1 · AI Workflows for DSR (presentation milestone) |
| 2026-Q3+ | Propozel productization (Act 05 ongoing) |
