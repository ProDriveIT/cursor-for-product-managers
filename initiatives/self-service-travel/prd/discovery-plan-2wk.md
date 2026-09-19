# Discovery plan (2 weeks) — Self-Service Travel

**Owner:** James Stock  
**Starts:** After sprint day (and after work-order #1 + #2)  
**Tied to:** [`success-criterion.md`](./success-criterion.md)  
**PRISM core #4**

## Week 1 — Problem & demand

| Day | Activity | Owner | Output |
|-----|----------|-------|--------|
| 1–2 | Shadow / interview MSP Org travel operator(s) | James | Notes → `user-interviews/transcripts/` |
| 3 | Snapshot interviews (`/create-interview-snapshots`) | James | `user-interviews/snapshots/` |
| 4–5 | Pull remaining baseline gaps; map failed-request reasons | James + eng/ops | Update `product-analytics/baseline-msp-org.md` |

## Week 2 — Options & kill

| Day | Activity | Owner | Output |
|-----|----------|-------|--------|
| 6–7 | Test A1 (reporting demand) | James | Result in `assumptions/riskiest-assumptions.md` |
| 8–9 | Test A2 (deploy vs trust/process bottleneck) | James | Result in assumptions file |
| 10 | Write ≥3 strategic options + kill rules; update strategy draft | James | Strategy §Options; re-run `/product-strategy-review` |

## Out of scope these two weeks

- Building central reporting UI, one-click deploy, or full onboarding
- Multi-client rollout commitments

## Decision at end of week 2

- **PROCEED to PRD** for one option, or  
- **HOLD / park** SST build and keep instrumenting MSP Org only
