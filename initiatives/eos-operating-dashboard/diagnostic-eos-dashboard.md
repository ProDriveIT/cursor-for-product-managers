# Diagnostic — EOS Operating Dashboard

**Date:** 2026-09-19  
**Status:** In progress (interactive)  
**Stage assumption:** Pre-product / pre-EOS adoption (prior attempt abandoned)

## Premise (as stated)

A single Azure-hosted web dashboard so management (then departments) can run L10, Focus Days, Traction, and “all the things” in one site; store data for reporting, analysis, and agents.

## Coach position (updated)

**Primary user is clear: you (Integrator).** That is real specificity. The product thesis is now: *reduce Integrator admin/chase cost so you can enforce process on Bruce and Matt.*

That thesis can work. The current feature cloud does **not**:

| Ask | Verdict |
|-----|---------|
| One place for Rocks / Issues / Scorecard (KPI) updates | **Core** — this is the Integrator wedge |
| User-friendly, minutes-not-hours for Matt | **Core UX constraint** on that wedge |
| “What we’re supposed to do next and why” for Bruce in-meeting | **L10 run mode** — second surface, same data |
| Time logging | **Creep** — PSA territory unless Scorecard literally needs it; defer |
| AI chase / automation | **Leap of faith** — build after manual chase works inside the portal |
| Make Bruce stop doing random things | **Still not a software problem** — you + implementer enforce; product supplies the script |

**Failure pattern named:** Solution expanding to “Integrator OS + PSA lite + AI chief of staff” before one weekly Scorecard/Rocks update habit exists.

**What would change my mind on AI-in-v1:** Written list of the exact chase messages you send today, frequency, and proof people respond to async nudges (email/Teams) — then automate *those* only.

**What would change my mind on time-logging-in-v1:** A Scorecard KPI that cannot be computed without time entry and is required for the first L10.

## Evidence gaps

| Gap | Status |
|-----|--------|
| Post-mortem | Filled |
| Named primary user | **Filled — you (Integrator)** |
| Secondary users | Bruce (MD, process drift); Matt (time-poor updater) |
| Engineering repo | Still missing |
| Committed L10 restart date | Open |
| Narrowest wedge | Asked next |

## Session log

### Q1 — Demand reality

Pre-adoption; second-chance bet. No “upset if disappeared” yet — proxy demand = Integrator pain when cadence restarts.

### Q2 — Post-mortem

SSOT gap + Bruce remix + weak challenge + passenger department Traction. Implementer for accountability.

### Q3 — Desperate specificity

*Who is the product for?*

**Answer (paraphrased):** Largely for you as Integrator — meeting admin, number collection, chasing Rocks/Issues/KPIs. Want one portal (time, numbers, KPIs, Rocks), user-friendly; later AI to automate chase. Easier for you → easier to push Bruce (random/unplanned) with “what next and why,” and Matt (200-item list / time-poor) with a 2-minute browser update habit. Auto-pull KPIs where possible.

**Position:** Best answer so far. Primary buyer/user = Integrator. Bruce and Matt are **constrained contributors**, not co-primary personas for v1 scope. “Make Integrator’s life easy” is a valid product; “AI + time log + full Traction + department rollout” is scope suicide.

**Push into Q4:** Strip to the smallest thing that removes *your* weekly chase burden for the first L10.

### Q4 — Narrowest wedge (asked next)

What’s the smallest version that makes *your* Integrator week easier for the first L10 — shippable before Focus Days, AI, time logging, or department Traction?

---

## Sharpest reframe (current)

**EOS Integrator Console (leadership only):** Matt (and peers) update Scorecard numbers + Rock status + Issues in one place in minutes; you run L10 from that same SSOT with a fixed agenda (“what next / why”); you chase from incomplete fields — manually first, AI later. Bruce sees the plan in the room; he does not get a customization sandbox.

## Weakest link

Building for your future AI-assisted self before proving Bruce/Matt will update anything weekly. If Matt won’t open a tab for 2 minutes, automation amplifies empty data.

## One assignment (update at close)

_TBD_
