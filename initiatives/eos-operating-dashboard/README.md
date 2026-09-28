# EOS Operating Dashboard

**Status:** Live. L10 #1 ran **21 Sep 2026** on https://eos.prodriveit.co.uk  
**Timeline:** L10 #2 **Mon 29 Sep**. Focus Day **1 Oct 2026** (Rob Liddiard; no dashboard; set Q4 Rocks). L10 #3 **Mon 6 Oct**. Then 5 consecutive pure L10s. Hold dashboard automations until Rob validates the L10 method.  
**Owner:** James Stock (Integrator)  
**Stakeholders:** James, Bruce Penson (Visionary), Matt Taylor, **Rob Liddiard** (Mission Group)  
**Roadmap:** [`roadmap.md`](./roadmap.md)  
**Engineering repo:** https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS  
**Live board:** https://eos.prodriveit.co.uk  
**Hub (not the L10 board):** https://prodrive365.sharepoint.com/sites/ManagementTeam  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)  
**1-pager:** [`prd/1-pager-eos-operating-dashboard.md`](./prd/1-pager-eos-operating-dashboard.md)  
**Design:** [`design/design-brief-leadership-l10-console.md`](./design/design-brief-leadership-l10-console.md)  
**Current decision:** [`decision-revision-sharepoint-rejected.md`](./decision-revision-sharepoint-rejected.md)  
**Repo analysis:** [`engineering-repo-analysis.md`](./engineering-repo-analysis.md)

## Initiative Goal

Make James’s EOS week workable with a purpose-built Leadership L10 dashboard, not SharePoint Lists. Friday prep under 20 minutes. Five consecutive pure-EOS L10s.

**Working v1 (C′):** Azure L10 room mode. James owns the path. Bruce and Matt sign the product after 3 live L10s. **Out:** Lists-as-meeting-board, department Traction before cadence sticks, time logging.

## Current Status

- [x] User research / dummy Hub L10 (Lists rejected)
- [x] Primary user named *(James — Integrator)*
- [x] Product diagnostic survived *(wedge = L10 room mode)*
- [x] Engineering repo analysed
- [x] One-pager revised to **C′**
- [x] Decision Register updated — https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/pull/3
- [x] Dashboard stand-up — https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/pull/5
- [x] Implementer + Focus Day dated — **Rob Liddiard, 1 Oct 2026**
- [x] C′ path decided by James (19 Sep)
- [x] Azure host live — B1 UK South, Easy Auth, `eos.prodriveit.co.uk`
- [x] Live meeting store — Azure `/home/eos-data/state.json` (instant save)
- [x] Eight Leadership KPIs, Q3 Rocks, SSO for James / Bruce / Matt
- [x] First live L10 — **21 Sep 2026** (planned slot had been 22 Sep)
- [ ] L10 #2 — **Mon 29 Sep 2026** (Q3 content; Q4 Rocks wait for Rob)
- [ ] Focus Day with Rob — **1 Oct 2026** (**no dashboard**; set Q4 Rocks)
- [ ] L10 #3 — **Mon 6 Oct 2026** (load agreed Q4 Rocks; Bruce + Matt sign the product)
- [ ] Five consecutive pure-EOS L10s recorded
- [ ] Dashboard automations (Planner, KPI pull, transcripts) — **held until Rob validates the L10 method**

## Quick Links

- [Roadmap](./roadmap.md)
- [Design brief](./design/design-brief-leadership-l10-console.md)
- [Decision revision](./decision-revision-sharepoint-rejected.md)
- [1-pager](./prd/1-pager-eos-operating-dashboard.md)
- [L10 runbook (ProDrive-EOS `main`)](https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/blob/main/prodrive/deployment/Dashboard-Bakeoff-Runbook.md)

## Notes

- Meeting state is Azure JSON. GitHub `data/` is the seed / catalogue, not the in-meeting editor.
- Sign in as `James.Stock@prodriveit.co.uk`, not `admin-jstock`.
- Focus Day (1 Oct): **no dashboard**. Set Q4 Rocks there; enter them on the board before the 6 Oct L10.
- Phase 1 product = L10 only (Issues, Rocks, To-Dos, KPIs). Hold Planner / KPI / transcript work until Rob.
- Client monthly reports: [`../client-monthly-report/`](../client-monthly-report/).
