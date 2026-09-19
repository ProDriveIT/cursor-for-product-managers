# Pro Drive — Company Context (working draft)

**Status:** Skeleton — fill gaps before heavyweight PRDs.  
**Last updated:** 2026-09-19  
**Owner:** TBD

This file is the grounding reference for Cursor skills in this workspace. Incomplete sections are marked `TODO`. Prefer short, factual bullets over marketing language.

---

## 1. Who we are

| Field | Value |
|-------|--------|
| Company | Pro Drive (ProDriveIT) |
| What we sell | TODO — MSP / IT services? managed services? projects? |
| Who buys | TODO — named segment (e.g. mid-market professional services in NZ/AU) |
| Geography | TODO |
| Approximate size | TODO — headcount, client count, ARR band if shareable |

---

## 2. How we run the business today (EOS)

| Field | Value |
|-------|--------|
| EOS status | **Not in use.** Prior adoption abandoned. Re-adopting via custom dashboard + third-party implementer. |
| Why prior attempt failed | (1) No SSOT — whiteboard/notes/Teams/SharePoint, inconsistent by person/week; (2) MD (Bruce) adapted process until it wasn’t EOS; peers didn’t challenge; (3) Implementer role exists to hold accountability; (4) Department Traction became solo/passenger meetings; pick-and-choose process |
| EOS champion (named person) | TODO — distinguish from Integrator |
| Integrator / Visionary (named) | **Integrator: James.** Visionary/MD: **Bruce**. Management peer: **Matt** (time-poor) |
| Third-party EOS implementer | **Yes** — accountability / process fidelity (esp. vs Bruce drift). Name: TODO |
| Cadence | Target: Monday L10; James prep Friday. **Not live yet** on the new console |
| KPI pipeline today | Mix of automated + manual → spreadsheet → management Scorecard → (planned) same numbers on dashboard |
| Hosting constraint | **Azure + Microsoft 365 + Copilot only.** Self-hosted in Pro Drive. **No third-party tools** |
| Tools used in failed attempt | Whiteboard/loop, notes, Teams, SharePoint (no single system) |
| Pain / risk | Integrator admin + chase load; Bruce process drift; Matt update friction; prior SSOT chaos. Risk: scope → platform before L10 habit |

**EOS components — aspiration vs live:**

| Component | Live today? | In “single site” ambition? |
|-----------|-------------|----------------------------|
| Vision / V/TO / Traction | No | Yes |
| Rocks | No | Yes |
| Scorecard | No | Yes |
| Issues list | No | Yes |
| To-Dos | No | Yes |
| Level 10 meeting | No | Yes (management → departments) |
| Focus Days | No | Yes |
| People analyzer / accountability chart | No | TODO |
| Reporting / analytics / agents on EOS data | No | Yes (later capability) |

---

## 3. Systems & data (source of truth)

List systems that hold operational truth the EOS dashboard or client reports might need.

| System | What it holds | Owner | Access notes |
|--------|---------------|-------|--------------|
| TODO — PSA (e.g. ConnectWise, Halo, Autotask) | Tickets, time, contracts | TODO | TODO |
| TODO — RMM | Device health | TODO | TODO |
| TODO — M365 / Azure | Identity, tenants | TODO | CIPP forks exist under ProDriveIT |
| TODO — Finance | Invoices, margin | TODO | TODO |
| TODO — EOS tool | Rocks, scorecard, issues | TODO | TODO |
| GitHub org `ProDriveIT` | Engineering / automation | TODO | Public: CIPP, CIPP-API, Pro-Drive-Public, this PM toolkit |

**Engineering repos (product code — not this PM toolkit):**

| Product | Repo | Status from this agent |
|---------|------|------------------------|
| EOS Operating Dashboard / Hub | https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS | **Analysed 2026-09-19** — M365-native path decided; Azure dashboard superseded; Hub live |
| Client monthly reports | TBD | Not started in this workspace |
| EOS in Practice (business notes) | https://github.com/ProDriveIT/Github-SupportingData (`50-eos`) | Sister knowledge home |

---

## 4. Products in flight

### A. EOS Operating Dashboard (priority)

- **Intent:** Purpose-built Leadership L10 console (CEOS/Azure dashboard), not SharePoint Lists as the meeting board
- **Engineering:** https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS
- **Hub use test (2026-09-19):** Dummy L10 on Lists felt like a fudge; zero LT engagement; feels like OneNote/Loop/Planner. **A′ (Power App on Lists) withdrawn.**
- **Current recommendation:** **C′** — revive Azure/CEOS dashboard; update Decision Register; 2-meeting bake-off
- **Primary users:** James (Integrator), Bruce (Visionary), Matt; coach Rob / Mission Group
- **Success bar:** 5 consecutive pure-EOS L10s; Friday prep under 20 minutes
- **Decision note:** [`../initiatives/eos-operating-dashboard/decision-revision-sharepoint-rejected.md`](../initiatives/eos-operating-dashboard/decision-revision-sharepoint-rejected.md)
- **1-pager:** [`../initiatives/eos-operating-dashboard/prd/1-pager-eos-operating-dashboard.md`](../initiatives/eos-operating-dashboard/prd/1-pager-eos-operating-dashboard.md)
- **Initiative folder:** [`initiatives/eos-operating-dashboard/`](../initiatives/eos-operating-dashboard/)


### B. Client monthly reports (parked)

- **Intent:** Client-facing monthly proof of work / value.
- **Depends on:** Stable operational data contract (likely after EOS dashboard data spine is clear).
- **Initiative:** Not created yet — create after EOS diagnostic survives.

---

## 5. Strategy & OKRs (pointers)

- Vision / strategy drafts: [`product-vision-and-strategy/`](./product-vision-and-strategy/)
- OKRs: [`okrs/`](./okrs/)
- Team / R&R: [`team-structure/`](./team-structure/)

Until those folders have real docs, treat §1–4 of this file as the only company context.

---

## 6. Access notes for Cloud Agents

| Identity / tool | What it can see |
|-----------------|-----------------|
| `gh` as ProDriveIT | Public ProDriveIT repos only; **cannot** resolve ProDrive-EOS |
| GitHub MCP | **Can** read https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS |

Analysis written: [`../initiatives/eos-operating-dashboard/engineering-repo-analysis.md`](../initiatives/eos-operating-dashboard/engineering-repo-analysis.md)

Do not invent live Scorecard/Rock values from GitHub `data/` — that tree is fictional/pilot seed. Live Hub: Management Team SharePoint.

---

## 7. Open questions (block clarity)

1. Exact name and location of the EOS engineering repo? *(still blocking for build)*
2. Implementer name; will they run from this console?
3. Inventory of automated vs manual KPIs in the spreadsheet Scorecard path
4. First Monday L10 date on the new console
5. Client reporting: separate product or export of same data spine? *(parked)*

