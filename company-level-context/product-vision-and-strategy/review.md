# PRISM Strategy Review — Self-Service Travel

**Decision: HOLD**  
**Owner:** James Stock  
**Reviewed:** 2026-09-19 · **Next review:** after sprint day (work-order #3; not before EOS L10-ready + one-client HTML)  
**Doc:** [`self-service-travel-strategy.md`](./self-service-travel-strategy.md) · **Hub:** [`../../initiatives/self-service-travel/`](../../initiatives/self-service-travel/)  
**Work order:** [`product-work-order.md`](./product-work-order.md)  
**Machine-readable:** [`review.json`](./review.json)

## Executive Summary

- Evidence gate fails: **1/5** core items (hub link only). Missing mandatory tagged assumptions (#2) and success criterion (#3). Starter assumption templates exist; tests not run.
- Intake is a **feature list** (reporting, one-click deploy, onboarding), not a strategy. Live for MSP Org proves existence, not multi-client demand.
- PRISM overall **0.2/5**. Score-based Approve/Conditional/Revise does not apply until the gate returns PROCEED.
- **Sequencing locked:** EOS L10-ready → one-client full HTML reports → SST sprint day. That order is correct given HOLD and Focus Day pressure; do not pull SST discovery forward.
- Path: finish #1 and #2; complete [sprint prep](../../initiatives/self-service-travel/sprint-prep.md); run [1-Day Evidence Sprint](../../initiatives/self-service-travel/evidence-sprint-1day.md); re-run `/product-strategy-review`.

## Evidence readiness gate

| Core item | Met? |
|-----------|------|
| 1. Last-180-day signals (≥3) | No |
| 2. Riskiest assumptions tagged (≥2) | No |
| 3. Success criterion (OMTM / heuristic) | No |
| 4. 1–2 week discovery plan or OKR draft | No |
| 5. Versioned evidence hub link | Yes |

**Status: HOLD** (need ≥4 including #2 and #3). Citations: [[ev-intake|company-level-context/product-vision-and-strategy/self-service-travel-strategy.md#L13-L28|2026-09-19]], [[ev-hub|initiatives/self-service-travel/README.md#L14-L22|2026-09-19]].

## Impact × Confidence

| Item | Impact | Confidence | Note |
|------|--------|------------|------|
| Central reporting (planned → failed) | Unknown | Low | No baseline stuck/fail rates |
| Near one-click client deploy | Unknown | Low | Deploy may not be the binding constraint |
| Full client onboarding | Unknown | Low | Overlaps deploy; no funnel data |

## PRISM Scores

| Dimension | Score | Why |
|-----------|-------|-----|
| P — Problem Diagnosis | 0 | No JTBD, causality, or behavioral data [[ev-intake\|…strategy.md#L15-L22\|2026-09-19]] |
| R — Reframe Opportunity | 0 | No timing, whitespace, or shift [[ev-intake\|…strategy.md#L24-L28\|2026-09-19]] |
| I — Intentional Bets | 0 | No trade-offs, non-goals, or thresholds [[ev-intake\|…strategy.md#L17-L21\|2026-09-19]] |
| S — Systemized Execution | 0 | No OKRs / loops; company OKRs placeholder [[ev-ctx\|company-level-context/okrs/README.md\|2026-09-19]] |
| M — Momentum & Meta | 1 | Production live for MSP Org only; no retros/stopped work [[ev-intake\|…strategy.md#L13-L15\|2026-09-19]] |
| **Overall** | **0.2** | Equal-weighted average |

**Options compared:** 0 (warn: need ≥3 before Approve).

## Mode highlights

- **Socratic:** Thesis, outcomes, causality, alternatives, unit economics, and disconfirming evidence all absent.
- **Biases:** Availability (one live tenant), anchoring (three feature titles), sunk cost (already in production). Survivorship risk: non-adopters are invisible without the reporting you want to build — do not use that circularity as proof.
- **Stakeholders:** Board gets no thesis; eng cannot sequence work; GTM cannot sell multi-client without deploy proof; support needs ticket evidence before a console.

## Pre-mortem / Kill-Switch

**Top failure causes:** feature build without behavior change; MSP Org mistaken for PMF; EOS dashboard capacity collision; wrong bottleneck (trust/process vs deploy); no kill criteria.

**Leading indicators:** weekly requesters outside MSP Org; median planned→ended time; failed-request rate + reasons; hours per new client go-live.

**Kill if:** after 2-week discovery no named weekly reporting user; after 30 instrumented days no actionable stuck/fail volume; second-client one-click pilot misses SLA or burns excess support hours.

## Improvements (priority)

1. **Now — James:** Drive work-order #1 (EOS L10-ready); do not start SST sprint day.
2. **After #1 — James:** Deliver work-order #2 (Quest Fund Placement full HTML) via `initiatives/client-monthly-report/`.
3. **Before sprint day — James:** Finish [sprint-prep checklist](../../initiatives/self-service-travel/sprint-prep.md) (MSP Org champion, eng/ops, access, calendar).
4. **Sprint day — James + eng/ops:** Run [1-Day Evidence Sprint](../../initiatives/self-service-travel/evidence-sprint-1day.md) (signals, A1/A2 tests designed, OMTM, options).
5. **Day after sprint — James:** Re-run `/product-strategy-review`; only then consider funding reporting / one-click / onboarding.

## Next Review Date

**After sprint day** (work-order #3), not on a fixed calendar date that conflicts with EOS/HTML. Until #1 and #2 exit and sprint outputs land, do not fund reporting / one-click / onboarding as a strategy bet.
