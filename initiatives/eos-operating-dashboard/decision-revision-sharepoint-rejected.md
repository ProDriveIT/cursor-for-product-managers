# Decision revision — SharePoint Hub rejected after use

**Date:** 2026-09-19  
**Owner:** James Stock (Integrator)  
**Status:** Decided by Integrator 19 Sep 2026 — overturn Lists-as-meeting-UX; revive CEOS/Azure dashboard path. Product sign-off after 3 L10s.  
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

**What the evidence does not yet prove:** That the CEOS/Azure dashboard will win with Bruce and Matt in a live L10. It was never fully tested. “Looked powerful” is interest. Gate the **product** (not the path) on **three facilitated L10s** with the same success bar: pure EOS agenda, Friday prep under 20 minutes, and someone other than James driving updates.

**Honest caveat:** The M365 plan’s intended meeting surface was a **Power App**, not raw Lists. James tested the Hub/Lists experience. That still matters: zero engagement with the Hub is a failed adoption signal for “EOS lives in SharePoint,” and Power App would still sit on the same Lists mental model. Prefer a clean revive of the CEOS dashboard over another SharePoint-shaped bet unless LT insists on a Power App bake-off first.

**What would change this position back to M365:** Bruce and Matt complete one L10 from a Power App prototype without James navigating Lists, and rate the meeting ≥8 with agenda fidelity.

---

## Revised decision options

| Option | Meaning |
|--------|---------|
| **C′ (decided, now live)** | **CEOS/Azure Leadership L10 dashboard** at https://eos.prodriveit.co.uk. Three live L10s; then Bruce + Matt sign the product. |
| **A′′** | Build **Power App** L10 room mode only (no raw Lists in meeting). Timebox vs C′. |
| **B′** | Keep using Hub Lists for 4 more weeks (reject — already failed the feel test). |
| **D** | Pause product build; coach-led L10 on paper/template until Rob/LT Agree seats and V/TO. |

### Scope lock under C′

**In for the live L10s:** Shared-screen L10 (fixed agenda, Scorecard, Rocks, Issues, To-Dos) at https://eos.prodriveit.co.uk, fed by existing Scorecard pipeline (Data Entry / spreadsheet) where needed so Friday prep stays under 20 minutes.

**Out until five consecutive pure L10s:** Department Traction, Focus Days, AI chase, Bruce customization sandbox, dual live SSOTs (do not keep GitHub `data/` and Lists and Azure all “live”).

**SSOT rule:** Azure `/home/eos-data/state.json` is the writable meeting store. SharePoint Lists may remain read/archive or Scorecard feed — not the in-meeting editor.

## Current operating state — 20 Sep 2026

| Item | Value |
|------|--------|
| URL | https://eos.prodriveit.co.uk |
| Host | Azure App Service Linux B1, UK South, Easy Auth |
| Users | James, Bruce, Matt (`James.Stock@` — not `admin-jstock`) |
| First live L10 | Monday 22 Sep 2026 |
| Still gated | Product sign-off after L10 #3; five consecutive pure L10s |

---

## Decision Register action required

**Done (merged):** https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/pull/3 → `main`

Updates now on `main`:

- `prodrive/governance/EOS-Decision-Register.md` — 19 Sep 2026 meeting-UX rows
- `AGENTS.md` — Azure/CEOS bake-off allowed; Lists-as-board forbidden
- `prodrive/dev/Cursor-Azure-EOS-Dashboard-Build-Prompt.md` — reopened
- `prodrive/README.md` — current direction

---

## Stand-up (Phase 0) — merged

**Merged:** https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/pull/5 → `main` (superseded conflicted #4)

| Open today | How |
|------------|-----|
| Local host | `python apps/eos-dashboard/server.py` → `http://localhost:8000/` (after `python dashboard/build.py`) |
| Artifact | Actions → Build Pro Drive EOS dashboard → download `prodrive-eos-dashboard` |
| Azure | `prodrive/deploy/azure/` after `az login` — target `eos.prodriveit.co.uk` + Easy Auth |

Runbook: [`prodrive/deployment/Dashboard-Bakeoff-Runbook.md`](https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/blob/main/prodrive/deployment/Dashboard-Bakeoff-Runbook.md) on `main`.

**Focus Day (1 Oct 2026):** no dashboard — Rob Liddiard runs the day as he wishes. Phase 1 product scope stays Leadership L10 (Issues, Rocks, To-Dos, KPIs). Quarterly / Focus Day dashboard use is a later assessment only.

---

## Sign-off

| Name | Role | Decision (C′/A′′/B′/D) | Date |
|------|------|-------------------------|------|
| James | Integrator | C′ (decided) | 2026-09-19 |
| Bruce | Visionary / MD | Product after 3 L10s | |
| Matt | Management | Product after 3 L10s | |
