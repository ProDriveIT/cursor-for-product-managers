# 1-Day Evidence Sprint — Self-Service Travel

**Goal:** Clear the PRISM evidence readiness gate from HOLD → PROCEED (≥4 core items, must include #2 and #3).  
**Date target:** 2026-09-22 (or next working day after owner assigned)  
**Owner:** TBD (product) · Eng/ops contact: TBD · MSP Org champion: TBD

---

## Morning (3–4 hours) — Core #1 and #5

| # | Task | Output path | Done when |
|---|------|-------------|-----------|
| 1 | Export or screenshot last-180-day signals: ≥3 items from tickets, Teams/email threads, usage logs, or competitor notes about travel requests | `evidence/signals-180d.md` | Three dated entries with source links |
| 2 | Pull production counts for MSP Org: requests by status (planned / actioned / ended / failed) and any deploy/onboarding time if known | `product-analytics/baseline-msp-org.md` | One table with dates and definitions |
| 3 | Confirm evidence hub versioning (this folder + git commit) | README status updated | Link stable in strategy draft |

## Midday (2–3 hours) — Core #2 and #3

| # | Task | Output path | Done when |
|---|------|-------------|-----------|
| 4 | Write ≥2 riskiest assumptions with tags (desirability / viability / feasibility) | `assumptions/riskiest-assumptions.md` | Each has falsification test ≤14 days |
| 5 | Define one success criterion (OMTM preferred) for next 90 days | `prd/success-criterion.md` | Metric + threshold + measurement source |

**Starter assumption candidates (replace with evidence-backed wording):**

- A1 (desirability): MSP Org operators will change weekly behavior if they get central status reporting.
- A2 (viability): Other clients will adopt if deploy drops to near one-click; deployment friction is the binding constraint, not trust/process/training.
- A3 (feasibility): Full client onboarding can ship without blocking EOS Operating Dashboard capacity.

## Afternoon (2–3 hours) — Core #4 and options

| # | Task | Output path | Done when |
|---|------|-------------|-----------|
| 6 | Draft 1–2 week discovery plan OR OKR draft tied to the success criterion | `prd/discovery-plan-2wk.md` or `../../company-level-context/okrs/` | Time-boxed activities + owners |
| 7 | Write ≥3 strategic options (not feature variants): e.g. deepen MSP Org only; productize deploy+onboarding; park and instrument only | Update strategy draft §Options | Each option has investment, impact, kill rule |
| 8 | Re-run `/product-strategy-review` with filled inputs | New `review.md` / `review.json` | Gate = PROCEED or explicit remaining gaps |

---

## Definition of done for PROCEED

- [ ] Core #1: ≥3 last-180-day signals filed
- [ ] Core #2: ≥2 tagged riskiest assumptions
- [ ] Core #3: success criterion written
- [ ] Core #4: discovery plan or OKR draft
- [ ] Core #5: versioned evidence hub linked from strategy doc
- [ ] Owner + review_window_start/end set on strategy draft

If Core #2 or #3 still missing at end of day: stay on HOLD; do not score for Approve.
