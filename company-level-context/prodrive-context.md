# Pro Drive — Company Context

**Status:** Grounded from GitHub org inventory (19 Sep 2026)  
**Last updated:** 2026-09-19  
**Owner:** James Stock (Integrator / Head of Operations)

This file is the grounding reference for Cursor skills in this workspace. Prefer short, factual bullets over marketing language. Proposed V/TO content is labelled **Proposed** until Rob / LT agrees it.

**Sources reviewed:** `ProDriveIT/*` private + public repos, `Pro-Drive-IT-Limited/ProDrive-EOS`, Supporting Data `OPERATING-SYSTEM.md` / `50-eos` / `35-clients`, Agent Ops product STATUS docs, existing initiatives in this toolkit.

---

## 1. Who we are

| Field | Value |
|-------|--------|
| Company | **Pro Drive** (legal: Pro Drive IT Limited). Prose name: Pro Drive. GitHub: `ProDriveIT` (user) + org `Pro-Drive-IT-Limited` |
| What we sell | Managed IT for regulated professional services — MSP delivery (Service Desk + Professional Services + Tech/Cyber), strategic outsourced IT management, alignment / Inforcer baselines, vCIO / TAM cadence. Proven Process (**Proposed**): **Pro Drive 360** — Audit → Roadmap → Align → Enforce |
| Who buys | **Proposed List:** CEOs/CFOs of 20–100 seat businesses in central London or ~2 hours from Woking — **legal, financial services, accountancy** that want outsourced strategic IT management |
| Geography | UK (Woking / London catchment). M365: `prodrive365.sharepoint.com`, `prodriveit.co.uk` |
| Approximate size | ~10 people (LT Acc Chart draft). Leadership: Bruce Penson (Visionary / MD), James Stock (Integrator / Ops), Matt Taylor (Finance/Admin + Tech Success) |
| Commercial targets (Proposed V/TO) | FY25–26: MRR £90k, 12.5% adj. EBIT, 6 net new clients. 3-year (to Sep 2028): £3M revenue, 20% EBIT. 10-year: £20M / 20% EBIT; niche #20in10 = 200 legal/FS/accountancy firms by 2034 |

**Client packs in Supporting Data (`35-clients/`):** ashtead-engineering, goddards-landscape, msp-secretaries, principia-advisory, quest-fund-placement, stewart-and-co — plus live product clients not yet fully packed (Pixel Global, Brunner UK, David Shepherd Wildlife Foundation, CSC).

---

## 2. How we run the business today (EOS)

| Field | Value |
|-------|--------|
| EOS status | Chosen company OS. Prior adoption abandoned; re-adopting with external implementer. Hub/Lists alone rejected as L10 board after use test |
| Why prior attempt failed | (1) No SSOT — whiteboard/notes/Teams/SharePoint; (2) Bruce adapted process until it wasn’t EOS; (3) no implementer holding fidelity; (4) Department Traction became solo/passenger meetings |
| Visionary / Integrator | **Visionary: Bruce Penson.** **Integrator: James Stock** (also Hub technical operator). Decided 07-09-2026 |
| LT functional split (Proposed) | Bruce = Visionary + Sales & Marketing. James = Integrator + Operations (SD + PS + Tech/Cyber). Matt = Finance / Admin + Tech Success. Dual seats intentional at ~10 people |
| Third-party EOS implementer | **Rob Liddiard**, Mission Group (`rob@mission-group.co.uk`) |
| Focus Day | Supporting Data Decision Register: **Thu 17 Sep 2026** booked. This toolkit’s EOS materials still cite **1 Oct 2026** (no-dashboard Focus Day / bake-off framing) — **reconcile which event is which** |
| Cadence | Monday Leadership L10; James Scorecard prep Friday. Pure-EOS L10 not yet sticky on new console |
| KPI pipeline today | Autotask → Azure KPI / SharePoint Excels → management Scorecard → (planned) dashboard / Hub thin view |
| Hosting constraint | **Azure + Microsoft 365 + Copilot only.** Self-hosted in Pro Drive. No third-party SaaS OS tools for Traction |
| Peer / TruMethods | **Cancel Peer** (07-09-2026) to offset EOS year-one cost. TruMethods / ProDrive 360 = MSP delivery methods, not a second company OS |
| Pain / risk | Integrator admin + chase load; Bruce process drift; Matt update friction; scope → platform before L10 habit |

**EOS components — aspiration vs live:**

| Component | Live today? | In product ambition? |
|-----------|-------------|----------------------|
| Vision / V/TO | Proposed pack only | Yes — agree with Rob |
| Rocks / Issues / To-Dos / Scorecard | Spreadsheet + Hub Lists path; not pure L10 habit | Yes — CEOS/Azure L10 console (C′) |
| Level 10 meeting | Monday slot; tool bake-off | Yes (management → Technical Team dept) |
| Focus Days | Booked / in flight with Rob | Yes |
| People analyzer | BreatheHR for sensitive GWC | Hub = Acc Chart seats only |
| EOS Facilitator / EHAN / Reporting agents | Design in flight | Company OS agent trio (under EOS) |

---

## 3. Systems & data (source of truth)

| System | What it holds | Owner / notes |
|--------|---------------|---------------|
| **Autotask** | PSA — tickets, time, contracts, RTEM/RHEM inputs | Numbers spine for EHAN / Insights packs |
| **Datto RMM** | Device health / remote | Ops product key `datto_rmm` |
| **IT Glue (EU)** | Published desk docs; PDKB org `2915570`; client orgs | Git packs in `35-clients/` and `70-policy-and-procedures/PDKB/` mirror |
| **M365 / Entra / Intune** | Identity, tenants, CA, SharePoint | CIPP forks; Inforcer baselines |
| **ConnectSecure** | Vulnerability management | Platform projects in GitHub-Repos |
| **Huntress / Mimecast / LastPass / etc.** | Security stack | See Supporting Data `ops-products-catalog.yaml` |
| **BreatheHR** | People Analyser / GWC / formal reviews | Not Hub |
| **SharePoint Management Team Hub** | https://prodrive365.sharepoint.com/sites/ManagementTeam — rejected as L10 *board*; still candidate for Lists SoT after cutover |
| **Azure KPI / SharePoint Files Excels** | Computed Autotask KPIs / Insights packs | Feeding Scorecard + client reports |
| **DeskDirector** | End-user learning / portal | Guides tooling in Supporting Data |
| **GitHub** | Engineering + knowledge | See §6 |

**Scorecard layers (never mix answers):** (1) Azure/SharePoint KPI Excels = computed numbers; (2) Management Team EOS Lists = Leadership L10 thin view after cutover; (3) `60-team-management` YAML/CSV = engineer review evidence, not company Scorecard.

---

## 4. Locked work order (capacity)

**Set by James Stock, 2026-09-19.** Detail: [`product-vision-and-strategy/product-work-order.md`](./product-vision-and-strategy/product-work-order.md)

| Order | Product | Exit before next |
|-------|---------|------------------|
| 1 | EOS Operating Dashboard — L10-ready | Console usable for a real leadership L10 |
| 2 | Client monthly reports — one client, full HTML | Quest (or named pilot) complete HTML Pro Drive will show externally |
| 3 | Self-Service Travel — evidence sprint | Only after #1 and #2; then 1-Day Evidence Sprint → re-run PRISM |

Other live products (MSP minutes, SPAT, CE Mobile, Archiver, Inforcer portal, Performance Hub) are **operational** — maintain under change control; do not displace #1–#3 unless James reorders in writing.

---

## 5. Product portfolio (threshold filter)

**Initiative threshold:** named users beyond James alone; shipped or near-shipped software; ongoing product intent (not a one-off project or platform-only repo).

### Active / priority initiatives

| Initiative | Status | Engineering home |
|------------|--------|------------------|
| [EOS Operating Dashboard](../initiatives/eos-operating-dashboard/) | Priority #1 — C′ CEOS/Azure L10 bake-off | `Pro-Drive-IT-Limited/ProDrive-EOS` |
| [Client Monthly Report](../initiatives/client-monthly-report/) | Priority #2 — Quest pilot planning | GitHub-Repos KPI automation + Reporting Agent |
| [Self-Service Travel](../initiatives/self-service-travel/) | Priority #3 — **live**, strategy HOLD | `prodrive-agent-ops` / Travel Entra app |

### Live / operational products (initiatives stood up)

| Initiative | Status | Notes |
|------------|--------|-------|
| [MSP Meeting Minutes](../initiatives/msp-meeting-minutes/) | **Live · stable v1.0** | Board minutes from audio + agenda + pack. **Change freeze: do not update without James Stock input** |
| [SharePoint Permissions Audit (SPAT)](../initiatives/sharepoint-permissions-audit/) | **Live** | Pixel Global `/c/pixel-global` in production use |
| [CE Mobile Status](../initiatives/ce-mobile-status/) | **Live** | Azure Automation 3×/day; dogfood + Brunner UK |
| [SharePoint Archiver](../initiatives/sharepoint-archiver/) | **Operational** | Quest, CSC, Pixel COMPLETE Aug 2026; MSP Org enrolled |
| [Inforcer Alignment Portal](../initiatives/inforcer-alignment-portal/) | **Live (internal)** | Azure Static Web App; IT Glue remains SoR |
| [PD Performance Hub](../initiatives/pd-performance-hub/) | **Built · adoption unclear** | Team KPI / BreatheHR review app; last push ~Mar 2026 |

### Below initiative threshold (track here only)

| Item | Why below bar |
|------|----------------|
| Directory Group Review | Local HTML report; no hosted product |
| SharePoint Standardiser | Phase 0 inventory only |
| Agent Ops platform | Shared identity / telemetry — platform, not a user product |
| CIPP / CIPP-API forks | Vendor multitenant tooling |
| EHAN / EOS Facilitator | Company OS agents — Facilitator under EOS initiative; Reporting under Client Monthly Report |
| One-off GitHub-Repos projects | Delivery / integrations — not productised |
| [`client-facing-reports/`](../initiatives/client-facing-reports/) | Stub redirect → `client-monthly-report` |

---

## 6. Products in flight (detail)

### A. EOS Operating Dashboard (order #1)

- **Intent:** Purpose-built Leadership L10 console (CEOS/Azure), not SharePoint Lists as the meeting board
- **Engineering:** https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS
- **Practice notes:** https://github.com/ProDriveIT/Github-SupportingData/tree/main/50-eos
- **Current recommendation:** **C′** — revive Azure/CEOS dashboard; 2-meeting bake-off
- **Primary users:** James, Bruce, Matt; implementer Rob Liddiard
- **Success bar:** 5 consecutive pure-EOS L10s; Friday prep under 20 minutes
- **Initiative:** [`initiatives/eos-operating-dashboard/`](../initiatives/eos-operating-dashboard/)

### B. Client monthly reports (order #2)

- **Intent:** Auto-generated HTML monthly report — proactive work, initiatives, alignment, vCIO/TAM updates — so clients understand value when reactive tickets drop
- **Spine:** Insights packs (`reporting-kpi-automation`) + Reporting Agent (`agent-ecosystem-copilot`); archived `reporting-client` **superseded**
- **Pilot:** Quest Fund Placement · vCIO Bruce · TAM Danny Bray · ops James
- **Initiative:** [`initiatives/client-monthly-report/`](../initiatives/client-monthly-report/)

### C. Self-Service Travel (order #3 — live, strategy HOLD)

- **Intent:** Client IT Contact books time-boxed geo sign-in; destination-lazy CA; home named location never written
- **Host:** `https://travel.prodriveit.co.uk` · Entra app `ProDrive-Travel` (not Agent Ops)
- **Live:** MSP Secretaries (Claire Kett, Philippa Keith); David Shepherd (Natalie Archer, Katie Abbott); Pro Drive dogfood
- **PRISM:** HOLD — sprint day only after #1 and #2 exit
- **Initiative:** [`initiatives/self-service-travel/`](../initiatives/self-service-travel/)

### D. MSP Meeting Minutes Agent (**live · change-controlled**)

- **Intent:** SharePoint-triggered Azure + Power Automate pipeline: agenda/pack/audio → draft Word minutes for Chairman review
- **Clients/styles:** qed, avca, swc, wakam, rgg
- **Status:** Stable v1.0; production flow documented
- **Action:** **Cannot be updated without James Stock input** — treat as change-controlled / freeze until explicit approval
- **Initiative:** [`initiatives/msp-meeting-minutes/`](../initiatives/msp-meeting-minutes/)

### E–H. Other ops products

- **SPAT** — snapshot “who can open this?” for client IT Contacts; Pixel live  
- **CE Mobile Status** — phone readiness gate; Automation Account schedules  
- **SharePoint Archiver** — non-synced Archive library pattern (OneDrive 300k)  
- **Inforcer Alignment Portal** — browsable baseline alignment (Azure SWA; Entra-locked to Pro Drive)  
- **PD Performance Hub** — manager KPI dashboard + BreatheHR PDFs (desktop Flask app)

---

## 7. Engineering & knowledge map

| Repo | Role |
|------|------|
| [ProDriveIT/GitHub-Repos](https://github.com/ProDriveIT/GitHub-Repos) | Active projects (`10 Projects/`) — KPI automation, agent ecosystem, integrations |
| [ProDriveIT/Github-SupportingData](https://github.com/ProDriveIT/Github-SupportingData) | Business knowledge vault; EOS in Practice (`50-eos`); client packs; PDKB |
| [Pro-Drive-IT-Limited/ProDrive-EOS](https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS) | EOS product engineering (CEOS-based) |
| [ProDriveIT/prodrive-agent-ops](https://github.com/ProDriveIT/prodrive-agent-ops) | Multi-tenant app-only Agent Ops + product folders (Travel is separate Entra app) |
| [ProDriveIT/msp-meeting-minutes-agent](https://github.com/ProDriveIT/msp-meeting-minutes-agent) | Meeting minutes product |
| [ProDriveIT/inforcer-alignment-portal](https://github.com/ProDriveIT/inforcer-alignment-portal) | Alignment portal site |
| [ProDriveIT/pd-performance-hub](https://github.com/ProDriveIT/pd-performance-hub) | Performance Hub |
| [ProDriveIT/Pro-Drive-Public](https://github.com/ProDriveIT/Pro-Drive-Public) | Public service desk docs / runbooks |
| [ProDriveIT/cursor-for-product-managers](https://github.com/ProDriveIT/cursor-for-product-managers) | This PM toolkit |
| [ProDriveIT/CIPP](https://github.com/ProDriveIT/CIPP) / [CIPP-API](https://github.com/ProDriveIT/CIPP-API) | M365 multitenant management forks |
| [ProDriveIT/second-brain-skills](https://github.com/ProDriveIT/second-brain-skills) | Claude second-brain skills |

**Company OS agent roster** (under EOS — not separate initiatives):

| Agent | Job | Primary home |
|-------|-----|--------------|
| EOS Facilitator | Traction / L10 / Issues / Rocks | ProDrive-EOS |
| EHAN Agent | Autotask-derived KPIs (evolves from KPI Analysis Assistant) | GitHub-Repos agent-ecosystem + KPI spine |
| Reporting Agent | Draft monthly client HTML from packs | GitHub-Repos → Client Monthly Report initiative |

---

## 8. Strategy & OKRs (pointers)

- Work order + SST strategy: [`product-vision-and-strategy/`](./product-vision-and-strategy/)
- Proposed V/TO seed: Supporting Data `50-eos/vision/` (not yet Agreed)
- OKRs: [`okrs/`](./okrs/)
- Team / R&R: [`team-structure/`](./team-structure/) — Acc Chart draft in §2; Performance Hub org codes: BP, MT, JS, DB, CR, DS

Until those folders have agreed docs, treat this file as the primary company context.

---

## 9. Access notes for Cloud Agents

| Identity / tool | What it can see |
|-----------------|-----------------|
| `gh` as ProDriveIT integration | Often **public-only** / org list 404 — do not trust `gh` alone for private inventory |
| GitHub MCP | **Can** read private ProDriveIT repos + `Pro-Drive-IT-Limited/ProDrive-EOS` |
| Live Hub / Azure | Needs Pro Drive admin machine / named identity — not inventable from GitHub |

Do **not** invent live Scorecard/Rock values from GitHub `data/` — fictional/pilot seed. Live Hub: Management Team SharePoint.

Snapshot: [`team-structure/github-access-snapshot.md`](./team-structure/github-access-snapshot.md)

---

## 10. Open questions / actions

1. **Reconcile Focus Day dates** — Supporting Data says 17 Sep 2026; EOS initiative materials say 1 Oct 2026. Confirm what happened and what is next with Rob.
2. **MSP Meeting Minutes change control** — James to define who may propose changes and how freeze is lifted (**explicit owner action**).
3. **PD Performance Hub** — confirm whether managers still use it, or archive / Power Platform path wins.
4. Inventory of automated vs manual KPIs in the spreadsheet Scorecard path.
5. Confirm L10 bake-off dates relative to Focus Day outcome.
6. Client reporting commercially: separate product vs export of same data spine — still open.
7. Will Rob facilitate from the CEOS dashboard after Focus Day / Vision Building?
8. Promote missing live product clients (Pixel, Brunner, David Shepherd, CSC) into `35-clients/` packs where durable truth is needed.

---

## 11. Named people (quick reference)

| Person | Role |
|--------|------|
| Bruce Penson | Visionary / MD; Sales & Marketing; vCIO (Quest pilot) |
| James Stock | Integrator; Head of Operations; Hub operator; product owner for most internal tools |
| Matt Taylor | Finance / Admin + Tech Success (LT) |
| Danny Bray | Technology Success / TAM (Quest pilot) |
| Chris Ross-Lewin | Sales & Marketing (team sheet CR) |
| Dan Sheather | Professional Services (team sheet DS) |
| Rob Liddiard | EOS implementer — Mission Group |
| Claire Kett / Philippa Keith | MSP Secretaries travel contacts |
| Jamie Hanna / John Tytherleigh | Pixel Global SPAT users |
