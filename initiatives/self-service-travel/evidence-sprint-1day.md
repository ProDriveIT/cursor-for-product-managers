# 1-Day Evidence Sprint — Self-Service Travel

**Goal:** Clear the PRISM evidence readiness gate from HOLD → PROCEED (≥4 core items, must include #2 and #3).  
**Owner:** James Stock  
**Eng/ops contact:** TBD · **MSP Org champion:** TBD  
**Sprint day date:** TBD — **only after** [work order](../../company-level-context/product-vision-and-strategy/product-work-order.md) #1 (EOS L10-ready) and #2 (one-client full HTML)  
**Prep checklist:** [`sprint-prep.md`](./sprint-prep.md)

Do not run this day while EOS L10 or the one-client HTML report is still open.

---

## Morning (3–4 hours) — Core #1 and #5

| # | Task | Output path | Done when |
|---|------|-------------|-----------|
| 1 | File last-180-day signals: ≥3 items from tickets, Teams/email, usage logs, or competitor notes | `evidence/signals-180d.md` | Three dated entries with sources |
| 2 | Pull MSP Org counts by status (planned / actioned / ended / failed) + deploy/onboarding times if known | `product-analytics/baseline-msp-org.md` | Table with dates and definitions |
| 3 | Confirm evidence hub versioning (this folder + git commit) | README + strategy draft links | Links stable |

## Midday (2–3 hours) — Core #2 and #3

| # | Task | Output path | Done when |
|---|------|-------------|-----------|
| 4 | Finalize ≥2 riskiest assumptions (A1/A2) with tags + ≤14-day tests | `assumptions/riskiest-assumptions.md` | Test designs filled |
| 5 | Choose one success criterion (OMTM preferred) for next 90 days | `prd/success-criterion.md` | Metric + threshold + source |

Starter assumptions live in the assumptions file; rewrite with evidence from morning pulls.

## Afternoon (2–3 hours) — Core #4 and options

| # | Task | Output path | Done when |
|---|------|-------------|-----------|
| 6 | Confirm 2-week discovery plan against the chosen OMTM | `prd/discovery-plan-2wk.md` | Dates + owners set |
| 7 | Write ≥3 strategic options (not feature variants) with investment, impact, kill rule | Strategy draft §Options | Three options documented |
| 8 | Re-run `/product-strategy-review` | `review.md` / `review.json` | Gate = PROCEED or explicit gaps |

**Option starters (replace on the day):**

1. Deepen MSP Org only (instrument + reporting for one tenant).  
2. Productize deploy + onboarding for client #2 (narrow wedge).  
3. Park build; instrument only until OMTM moves.

---

## Definition of done for PROCEED

- [ ] Core #1: ≥3 last-180-day signals filed
- [ ] Core #2: ≥2 tagged riskiest assumptions with test designs
- [ ] Core #3: success criterion written
- [ ] Core #4: discovery plan dated
- [ ] Core #5: versioned evidence hub linked from strategy doc
- [ ] Owner (James Stock) + review_window_start/end set on strategy draft
- [ ] Work-order #1 and #2 marked exited in product-work-order / initiative READMEs

If Core #2 or #3 still missing at end of day: stay on HOLD; do not score for Approve.
