# Diagnostic — EOS Operating Dashboard

**Date:** 2026-09-19  
**Status:** In progress (interactive)  
**Stage assumption:** Pre-product / pre-EOS adoption (prior attempt abandoned)

## Premise (as stated)

A single Azure-hosted web dashboard so management (then departments) can run L10, Focus Days, Traction, and “all the things” in one site; store data for reporting, analysis, and agents.

## Coach position (updated)

**Primary failure mode last time was process fidelity + power dynamics, not tool sprawl alone.**

| Factor | Type | Will a dashboard fix it? |
|--------|------|--------------------------|
| Artifacts lived in whiteboard / notes / Teams / SharePoint; people did it differently | Consistency / SSOT | **Yes — this is the real product job** |
| Bruce (MD) adapted EOS until it wasn’t EOS; others didn’t challenge | Power / culture | **No.** At best SSOT + implementer give challengers a script |
| Third-party implementer hired to hold accountability (esp. Bruce) | External governance | Dashboard is a **prop for the implementer**, not a substitute |
| Ops “Traction” became a solo meeting; passengers; pick-and-choose | Cadence / buy-in | **No** if department rollout stays early; prove leadership L10 first |

Building software to “keep Bruce in line” is a weak product bet if Bruce can still override the room. Building an **opinionated, hard-to-fork EOS meeting system** that the implementer and non-Bruce leaders can point at is a coherent bet — **if** those people will actually use it in the room.

**What would change my mind toward full platform now:** Evidence the implementer + ≥2 management members will refuse to run L10 outside this system starting on a fixed date.

**What would change my mind toward “don’t build yet”:** Implementer not contracted for ongoing L10 facilitation, or Bruce will not accept a non-customizable EOS path for 90 days.

## Evidence gaps

| Gap | Status |
|-----|--------|
| Post-mortem of last attempt | **Filled** (see Q2) |
| Engineering repo | Still missing |
| Named primary user of the *product* | Open — Bruce vs implementer vs Integrator vs you |
| Committed L10 restart date | Open |
| Wedge | Emerging: opinionated leadership L10 SSOT — not departments/agents yet |

## Session log

### Q1 — Demand reality

*Upset if dashboard disappeared tomorrow?*

**Answer:** Pre-adoption; prior attempt dropped; want one site for L10 / Focus Days / Traction / everything + data for agents.

**Position:** Vision, not demand. Stage = second-chance adoption.

### Q2 — Status quo / post-mortem

*What exactly was the maintenance / failure mode?*

**Answer (paraphrased):**

1. **No single place:** loop / notes / Teams / SharePoint; management members did things differently every time.
2. **Bruce (MD)** treated EOS as optional template; tweaked immediately; others lacked strength/position to challenge. User notes tooling won’t fix that, but SSOT enables “that’s not what we agreed.”
3. **Third-party EOS implementer** exists mainly to hold accountability / keep Bruce in line; Bruce broke process; others wouldn’t challenge.
4. **Downstream:** too many passengers; ops Traction became one person driving a solo meeting; pick-and-choose process killed value.

**Position on this answer:** Strong, specific, believable. Factor 1 justifies a product. Factors 2–4 mean **software is secondary to facilitation and authority**. Calling the old pain “effort maintaining separate EOS tools” was incomplete — the deeper pain was **inconsistent practice + unchallengeable MD drift + fake departmental EOS**.

**Push (next):** Who is the product *for* in the room — Bruce, the implementer, or a named Integrator who will enforce the path?

### Q3 — Desperate specificity (asked next)

Name the human who needs this most for *their* job to work (not “the management team”).

---

## Sharpest reframe (current)

You are not building “EOS in Azure.” You are building a **canonical, opinionated L10 / Traction system of record** so the implementer and management peers can enforce “this is the plan” against ad-hoc Bruce variants — and so department rollouts don’t start until leadership cadence is real.

**v1 design implication:** Optimize for *process rigidity* (agenda, Scorecard, Rocks, Issues, To-Dos, same every week), not customization. Customization is how attempt #1 died.

**v1 scope implication:** Leadership team L10 only. No Focus Days, no department Traction, no analytics/agents until ~8 consecutive real L10s with >1 active participant per seat.

## Weakest link

Using a dashboard as a proxy for challenging the MD. If the implementer won’t (or can’t) escalate, and peers still won’t speak, SSOT becomes a museum of ignored agreements.

## One assignment (update at close)

_TBD_
