# PRISM Strategy Review — Self-Service Travel

**Decision: HOLD**  
**Reviewed:** 2026-09-19 · **Next review:** 2026-09-26  
**Doc:** [`self-service-travel-strategy.md`](./self-service-travel-strategy.md) · **Hub:** [`../../initiatives/self-service-travel/`](../../initiatives/self-service-travel/)  
**Machine-readable:** [`review.json`](./review.json)

## Executive Summary

- Evidence gate fails: **1/5** core items (hub link only). Missing mandatory tagged assumptions (#2) and success criterion (#3).
- Intake is a **feature list** (reporting, one-click deploy, onboarding), not a strategy. Live for MSP Org proves existence, not multi-client demand.
- PRISM overall **0.2/5**. Score-based Approve/Conditional/Revise does not apply until the gate returns PROCEED.
- What would change this: ≥3 dated 180-day signals, ≥2 falsifiable assumptions, one OMTM, and ≥3 options with kill rules.
- Immediate path: run the [1-Day Evidence Sprint](../../initiatives/self-service-travel/evidence-sprint-1day.md), then re-run `/product-strategy-review`.

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

1. **2026-09-22 — TBD owner:** Complete [1-Day Evidence Sprint](../../initiatives/self-service-travel/evidence-sprint-1day.md).
2. **2026-09-22 — TBD owner:** Tag ≥2 riskiest assumptions + ≤14-day tests.
3. **2026-09-22 — TBD + eng/ops:** OMTM + MSP Org baseline status counts.
4. **2026-09-26 — TBD owner:** ≥3 strategic options with kill rules; rewrite strategy past features.
5. **2026-09-26 — TBD owner:** Add product to `prodrive-context.md`; state priority vs EOS Operating Dashboard.

## Next Review Date

**2026-09-26** — only after sprint outputs land and inputs (owner, window, assumptions, success criterion) are filled. Until then, do not fund reporting / one-click / onboarding as a strategy bet.
