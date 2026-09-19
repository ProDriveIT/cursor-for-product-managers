# Diagnostic — EOS Operating Dashboard

**Date:** 2026-09-19  
**Status:** In progress (interactive)  
**Stage assumption:** Pre-product / pre-EOS adoption (prior attempt abandoned)

## Premise (as stated)

A single Azure-hosted web dashboard so management (then departments) can run L10, Focus Days, Traction, and “all the things” in one site; store data for reporting, analysis, and agents.

## Coach position

**There is no demand evidence for a dashboard yet** — because EOS is not in use. Nobody can be “upset if it disappeared”; the product does not yet own a weekly ritual. What you have is a **hypothesis**: last EOS attempt died on multi-tool maintenance burden, so a unified site will make adoption stick.

That hypothesis is plausible. It is also the classic MSP/ops failure pattern: **build the system of record before the operating cadence exists**, then discover the real cost was human discipline (updating Scorecard numbers, IDS, Rock owners), not tab-switching.

**What would change my mind toward “build the full platform now”:** A named Integrator who will run L10 weekly starting on a fixed date, with a written list of the *specific* maintenance tasks that killed the last attempt, and willingness to ship **only** those first.

**What would change my mind toward “don’t build software yet”:** Last failure was “people stopped doing Scorecard / Rocks,” not “tools were fragmented.” Software cannot fix non-adoption of the meeting.

## Evidence gaps

| Gap | Needed |
|-----|--------|
| Engineering repo | Exact name + read access |
| Named primary user | Integrator / L10 owner — name + consequence |
| Post-mortem of last EOS attempt | What tools, what maintenance, who quit first |
| Demand | Not applicable until a cadence is live; proxy = committed start date + owner |
| Wedge | Smallest surface that removes the *named* maintenance pain |

## Session log

### Q1 — Demand reality

*What's the strongest evidence someone would be genuinely upset if this dashboard disappeared tomorrow?*

**Answer (paraphrased):** EOS not in use yet (dashboard or otherwise). Prior adoption attempt was dropped largely because of effort maintaining separate EOS tools. Intent: one place for management team, later departments — L10, Focus Days, Traction, everything; data stored for report/analyse/agents.

**Position on this answer:** This is **vision + post-mortem hint**, not demand evidence. Correct stage label: **pre-adoption rebuild**. Interest in “single site + analytics + agents” is not demand. The only hard fact is: **multi-tool maintenance correlated with dropping EOS last time.**

**Push 1:** If the dashboard shipped tomorrow and EOS still wasn’t running, would anyone notice? → Expected: no. So the product’s job is not “replace a loved tool”; it is “make a second adoption attempt cheaper than the first.”

**Push 2 (asked next):** What *exactly* was the maintenance effort last time — which tools, which weekly tasks, who did them, and what broke first?

**Push 3 (queued):** Who is the named person accountable for L10 sticking this time, and what date does the first L10 land?

---

## Sharpest reframe (current)

You are not buying an EOS dashboard. You are buying a **second chance at EOS adoption** with lower admin friction. v1 should eliminate the concrete maintenance work that killed attempt #1 — not deliver Traction + Focus Days + department portals + analytics + agents.

## Weakest link

Process risk mistaken for product opportunity: building “all the things + data platform” before proving one meeting cadence survives 8 consecutive weeks.

## One assignment (update at close)

_TBD_
