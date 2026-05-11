# LIFT Method · License Models

**Current default:** proprietary. NAUCode-internal use only.

**Commercialization gate:** Principal must approve any external licensing.
See `tech-naucode/hq/quality-gates.md` G-05.

## Maturity gate for licensing

Per `dsr-audit/current-state.md`, LIFT hiện đang ở DSR Layer 5 với gaps:

- Certainty Engine scoring chưa giải thích được (open problem)
- Literature grounding chưa formal
- Cross-domain demonstration chưa có

Khuyến nghị: **không license broadly** cho đến khi gaps trên đóng. Trong lúc
chờ, các license tier dưới đây có thể được consider:

## License tiers (proposed)

### Tier 0 · Internal NAUCode use

- License: proprietary
- Scope: NAUCode consult engagements only
- Cost: $0 (internal)
- Status: ✓ Active

### Tier 1 · Pilot license (1-3 friendly clients)

- License: pilot — non-transferable, time-limited (12 months), with shared
  learning agreement
- Scope: 1 specific engagement per licensee
- Cost: Discounted vs Tier 2 + obligation to share retrospective data
- Required: NDA + IP assignment for any LIFT-derived improvement back to NAUCode
- Status: Available now — Principal-approved case-by-case

### Tier 2 · Commercial license

- License: commercial — per-seat or per-engagement
- Scope: Unlimited engagements within licensee org for license period
- Cost: TBD (pricing model needed — pre-requisite: published case study)
- Required: full IP assignment for LIFT improvements (or revenue share)
- Status: **NOT YET AVAILABLE** — defer until DSR audit Layer 5 gaps closed

### Tier 3 · Training & certification program

- License: train-the-trainer + certified practitioner credential
- Scope: Individual certification, valid 2 years, requires continuing education
- Cost: TBD
- Status: **NOT YET AVAILABLE** — defer until 3+ external success cases + accreditation path

### Tier 4 · Open methodology release

- License: Creative Commons (TBD specific variant — CC-BY-SA candidate)
- Scope: Public release of LIFT spec
- Cost: Free
- Rationale: After core methodology mature + commercial IP differentiated
  via Certainty Engine + Propozel platform
- Status: **DEFERRED** — at minimum Tier 2 must succeed first

## Pricing approach (when Tier 2 ready)

Per Act 05 of LIFT narrative: pricing follows Certainty Assumption.

**Bán theo certainty, không theo effort.**

Implication for license pricing:

- Per-engagement license fee proportional to project CU target
- "1 LIFT engagement license" = "Right to apply LIFT for delivering Y CU
  scope" — not "X hours of methodology consultation"

This is structurally different from typical SaaS or per-seat models. Pricing
model design itself is a Phase-3 development (Design & Dev) — TODO.

## IP assignment terms (for any tier)

LIFT-derived improvements by licensee become NAUCode IP, with attribution
credit and (Tier 1-2) revenue share if commercialized.

Specific clause draft in `tech-naucode/compliance/contracts/` (TODO when first
license signed).

## Refund / termination

For pilot license:
- Refund if engagement does not deliver CU target after 12 weeks of LIFT application
- Termination right if NAUCode discontinues LIFT (rare event — would coincide
  with Tier 4 open release)

For commercial license:
- TBD when Tier 2 launches

## Update cadence

License models reviewed at G-07 monthly review. Tier promotions (e.g., Tier 1
→ Tier 2 readiness) require:

- DSR audit re-run with closed gaps
- 5+ documented successful applications (not just internal)
- Pricing model validated with 3+ buyer interviews
- Principal + Managing joint sign-off (this is a Both gate, see hq/quality-gates.md)
