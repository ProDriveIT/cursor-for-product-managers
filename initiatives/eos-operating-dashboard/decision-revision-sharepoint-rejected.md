# Decision revision — SharePoint Hub rejected after use

**Date:** 2026-09-19  
**Owner:** James Stock (Integrator)  
**Status:** Proposed LT decision — overturn Lists-as-meeting-UX; revive CEOS/Azure dashboard path  
**Supersedes:** 1-pager revision A′ (continue Power App on Lists)

---

## What changed

James ran a **dummy L10 against the live Management Team EOS Hub** (SharePoint Lists / EOS.aspx). Assessment:

| Signal | Observation |
|--------|-------------|
| In-meeting UX | Feels like a **fudge**. Forcing L10 into SharePoint lists is hard to manage in the room |
| Team engagement | Hub shared with LT → **zero engagement** |
| Familiarity trap | Feels too close to the failed stack (OneNote, Loop, Planner, to-do lists) |
| Alternative | The **CEOS / Azure dashboard** in ProDrive-EOS (never fully tested in production) looked far more powerful and would be more effective for L10 |

This is stronger evidence than the 03 Sep architecture paper. **Adoption and in-meeting friction beat platform preference.**

---

## Coach position

**Overturn A′.** Do not keep investing in “Lists as the L10 board,” and do not assume an unbuilt Power App will fix a product that already reads as SharePoint choreography to Bruce and Matt.

**What the evidence supports:** Meeting UX must be a purpose-built EOS console (agenda + Scorecard + Rocks + Issues + To-Dos in one composition), not list views.

**What the evidence does not yet prove:** That the CEOS/Azure dashboard will win with Bruce and Matt in a live L10. It was never fully tested. “Looked powerful” is interest. Gate revival on **two facilitated L10s** (dummy then real) with the same success bar: pure EOS agenda, Friday prep under 20 minutes, and someone other than James driving updates.

**Honest caveat:** The M365 plan’s intended meeting surface was a **Power App**, not raw Lists. James tested the Hub/Lists experience. That still matters: zero engagement with the Hub is a failed adoption signal for “EOS lives in SharePoint,” and Power App would still sit on the same Lists mental model. Prefer a clean revive of the CEOS dashboard over another SharePoint-shaped bet unless LT insists on a Power App bake-off first.

**What would change this position back to M365:** Bruce and Matt complete one L10 from a Power App prototype without James navigating Lists, and rate the meeting ≥8 with agenda fidelity.

---

## Revised decision options

| Option | Meaning |
|--------|---------|
| **C′ (recommended)** | **Revive CEOS/Azure Leadership L10 dashboard** as the meeting console. Update EOS Decision Register: Azure dashboard is again an active production candidate for **meeting UX**. Run a 2-meeting bake-off before declaring SSOT cutover. |
| **A′′** | Build **Power App** L10 room mode only (no raw Lists in meeting). Timebox vs C′. |
| **B′** | Keep using Hub Lists for 4 more weeks (reject — already failed the feel test). |
| **D** | Pause product build; coach-led L10 on paper/template until Rob/LT Agree seats and V/TO. |

### Scope lock under C′

**In for bake-off:** Shared-screen L10 (fixed agenda, Scorecard, Rocks, Issues, To-Dos), hosted on Pro Drive Azure, fed by existing Scorecard pipeline (Data Entry / spreadsheet) where needed so Friday prep stays under 20 minutes.

**Out until five consecutive pure L10s:** Department Traction, Focus Days, AI chase, Bruce customization sandbox, dual live SSOTs (do not keep GitHub `data/` and Lists and Azure all “live”).

**SSOT rule for the bake-off:** Pick one writable meeting store for the trial (dashboard/API). SharePoint Lists may remain read/archive or Scorecard feed — not the in-meeting editor.

---

## Decision Register action required

File in ProDrive-EOS `prodrive/governance/EOS-Decision-Register.md` (engineering repo):

> **2026-09-19 — Meeting UX:** SharePoint Lists / Hub rejected after dummy L10 and zero LT engagement. Azure/CEOS dashboard path reopened for Leadership L10 console pending 2-meeting bake-off. M365 remains allowed for identity, Teams meetings, and data feeds; Lists are not the L10 board.

Until that row exists, AGENTS.md will keep telling builders “do not execute Azure brief.”

---

## Sign-off

| Name | Role | Decision (C′/A′′/B′/D) | Date |
|------|------|-------------------------|------|
| James | Integrator | C′ (proposed) | 2026-09-19 |
| Bruce | Visionary / MD | | |
| Matt | Management | | |
