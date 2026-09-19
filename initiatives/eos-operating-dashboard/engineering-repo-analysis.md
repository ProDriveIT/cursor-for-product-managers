# ProDrive-EOS repo analysis

**Analysed:** 2026-09-19  
**Repo:** https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS  
**Access note:** Visible via GitHub MCP under org `Pro-Drive-IT-Limited`. Not under `ProDriveIT`. `gh` CLI from this VM still returns 404 (different token).

This note is product-facing. It does not copy live KPI numbers or secret connection details.

---

## Verdict (updated 2026-09-19 — after Hub use test)

**Architecture paper said M365 Lists + Power App. Lived experience says Lists-as-L10-board failed.**

James’s dummy L10 and zero LT engagement overturn “continue the Hub/Lists path” (A′). Meeting UX should return to a **purpose-built CEOS/Azure dashboard**, with the Decision Register updated. Full decision note: [decision-revision-sharepoint-rejected.md](./decision-revision-sharepoint-rejected.md).

The earlier sections below remain accurate as a snapshot of what the repo *contains* and what was *decided on 03 Sep*. Treat the 03 Sep “Azure superseded” row as **pending reversal**, not as binding product direction for L10 UX.

---

## Verdict (original repo read — 2026-09-19 morning)

Pro Drive already has an EOS **product engineering home** (CEOS-based), a **decided M365-native runtime**, a **live Management Team Hub** with Lists + Scorecard grid, and **19 CEOS skills** plus Copilot Facilitator design. The **Azure App Service dashboard/API path is formally superseded** (Decision Register, 03 Sep 2026). AGENTS.md says: do not execute `prodrive/dev/Cursor-Azure-EOS-Dashboard-Build-Prompt.md`.

The PM 1-pager briefly aligned to Power App + Lists. **That interim alignment is withdrawn after the Hub use test** (see Revision 2 / decision-revision-sharepoint-rejected.md).

---

## What the repo is

| Layer | Role |
|-------|------|
| Upstream | [bradfeld/ceos](https://github.com/bradfeld/ceos) imported; private fork/adaptation |
| `skills/` | 19 reusable EOS facilitation skills (agent methodology) |
| `dashboard/build.py` | Static CEOS dashboard builder (reference / rollback), not the production target |
| `data/` | Fictional / pilot seed — **not** live business state |
| `learn/` | Curated EOS methodology (partially seeded to SharePoint Knowledge) |
| `prodrive/` | Pro Drive engineering: M365 deployment, Copilot, governance, integrations |
| Sister home | [Github-SupportingData / 50-eos](https://github.com/ProDriveIT/Github-SupportingData/tree/main/50-eos) = Pro Drive’s EOS-in-practice notes |

**Day-to-day users are meant to work in Teams / SharePoint / Power App / Copilot**, not GitHub.

---

## Decided production architecture (do not reopen casually)

From `prodrive/governance/EOS-Decision-Register.md` and `prodrive/deployment/M365-EOS-Deployment-Plan.md`:

```text
Teams + Microsoft Facilitator (spoken evidence)
        +
Pro Drive EOS Facilitator (Copilot Studio)
        ↓
Management Team SharePoint site
  → Power App (Leadership dashboard)
  → Microsoft Lists (Scorecard, Rocks, Issues, To-Dos, L10, …)
  → Controlled Power Automate / agent flows
```

| Decision | Status |
|----------|--------|
| Production EOS = M365-native | Decided |
| Azure dashboard/API production build | **Superseded** |
| Site | Reuse Management Team (live) |
| Visionary | Bruce Penson |
| Integrator | James Stock |
| External coach | Rob / Mission Group (pending reference) |
| Leadership commitment | 100% to implement EOS with coach |

Live Hub: https://prodrive365.sharepoint.com/sites/ManagementTeam  
EOS page: …/SitePages/EOS.aspx

---

## Skills inventory (`skills/`)

| Skill | Job |
|-------|-----|
| `ceos-l10` | Run/review Level 10 (7-section agenda, time boxes; orchestrates other data) |
| `ceos-dashboard` | Read-only “state of the business” pulse |
| `ceos-scorecard` | Scorecard metrics / weekly values |
| `ceos-rocks` | Quarterly Rocks |
| `ceos-ids` | Issue Identify/Discuss/Solve |
| `ceos-todos` | To-Dos |
| `ceos-vto` | Vision/Traction Organizer |
| `ceos-accountability` | Accountability chart |
| `ceos-people` | People analyzer |
| `ceos-process` | Process documentation |
| `ceos-quarterly` / `ceos-quarterly-planning` / `ceos-annual` | Cadence meetings |
| `ceos-kickoff` | Kickoff |
| `ceos-checkup` | Checkup |
| `ceos-clarity` | Clarity break |
| `ceos-delegate` | Delegation |
| `ceos-trends` | Trends |
| `ceos-calendar` | Calendar |

These skills historically bind to GitHub `data/`. Production plan says agent-facing process should move to SharePoint Knowledge + Copilot instructions + controlled flows; skills remain engineering/methodology reference.

**L10 skill agenda (matches wedge B):** Segue → Scorecard → Rock Review → Headlines → To-Do Review → IDS → Conclude.

---

## Dashboard: what exists vs what was meant

| Asset | Status |
|-------|--------|
| CEOS static dashboard (`dashboard/build.py`) | Reference / rollback evidence |
| Azure App Service build brief | **Superseded — do not execute** |
| SharePoint Lists + Leadership Scorecard grid | **Live** on Management Team |
| EOS.aspx Hub landing | **Live** (Traction bar: Scorecard, Rocks, Issues, To-Dos) |
| Canvas Power App “Pro Drive EOS” | **Not started** (Phase 4) |
| Controlled flows (GetEOSSnapshot, SetRockStatus, …) | **Not started** (Phase 3) |
| Copilot Facilitator production cutover | **Not started** (Phases 6–7) |

**Scorecard today (aligned with James’s description):** people still enter in Weekly Data Entry; Hub 13-week Leadership Scorecard is refreshed from that pipeline (Management Scorecard / AllData). One Scorecard surface for LT (Weekly Values ledger is plumbing only).

---

## Phase progress (from Management-Team-Live)

| Phase | Status |
|-------|--------|
| 0 Inventory + site decision | Done |
| 1 Hub foundation (8 Lists, Knowledge, EOS page) | Done |
| Knowledge seed from `learn/` | Done (partial) |
| Proposed V/TO, Acc Chart, Scorecard load | Done (Proposed, not all Agreed) |
| List-first Hub unlocked to James/Bruce/Matt | Done 12 Sep 2026 |
| Issues: no Priority (Open → IDS in meeting) | Done 15 Sep 2026 |
| Scorecard 13-week refresh | Done 15 Sep 2026 |
| **3 Flows / controlled ops** | **Not started** |
| **4 Power App L10/weekly UX** | **Not started** |
| **5–10 Knowledge/Copilot/meeting pilot/cutover** | Mostly ahead |

Documented “next”: Power App UX · Friday Automate · Facilitator — still under EOS rules.

---

## Implications for our PM artifacts

| Artifact | Impact |
|----------|--------|
| Diagnostic wedge B (L10 room mode) | **Still valid as UX intent** — but the build home is **Power App on Lists**, not a new Azure web app |
| 1-pager option A “build on Azure” | **Misaligned** with Decision Register; revise to M365 Power App path |
| “No third-party tools” | Consistent with M365/Azure stack; CEOS skills are in-repo methodology, not Ninety |
| Success bar (5 pure L10s, Friday prep &lt;20 min) | Still good; measure against Hub + Power App, not a greenfield dashboard |
| Client monthly reports | Still later; same Lists may eventually feed reporting |

---

## Recommended next product moves (engineering-aligned)

1. **Revise 1-pager** so option A = continue/accelerate **Power App L10 room mode** on existing Lists (not Azure App Service).
2. Stay in **ProDrive-EOS** for build work; keep this PM toolkit for decisions/discovery.
3. Do not reopen Azure dashboard unless LT explicitly overturns the 03 Sep decision.
4. Sequence matches deployment plan: Phase 3 controlled ops → Phase 4 Power App (Home/Scorecard/Rocks/Issues/To-Dos/L10) → then Copilot write cutover.
5. Use `ceos-l10` agenda as the behavioural spec for the Power App L10 view.

---

## Open engineering questions (for James)

1. Exact Power Platform environment names / solution status?
2. Is Friday Automate for Scorecard refresh designed or only manual scripts?
3. First Monday L10 date intended to run from Hub lists (even pre–Power App)?
