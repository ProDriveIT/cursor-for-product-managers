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
| EOS status | TODO — implementing / running / stalled |
| EOS champion (named person) | TODO |
| Integrator / Visionary (named) | TODO |
| Cadence | TODO — Level 10 day/time, quarterly planning |
| Tools used for EOS today | TODO — Ninety.io, spreadsheets, Notion, whiteboard, other |
| Pain with current EOS tooling | TODO — what breaks weekly |

**EOS components in scope for product work (tick what we actually run):**

- [ ] Vision / V/TO
- [ ] Rocks
- [ ] Scorecard
- [ ] Issues list
- [ ] To-Dos
- [ ] Level 10 meeting
- [ ] People analyzer / accountability chart
- [ ] Other: TODO

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

| Product | Intended repo | Status from this agent |
|---------|---------------|------------------------|
| EOS Operating Dashboard | `ProDrive-EOS` (assumed) | **Not visible** — see §6 |
| Client monthly reports | TBD | Not started in this workspace |

---

## 4. Products in flight

### A. EOS Operating Dashboard (priority)

- **Intent:** Single Azure-hosted web dashboard to run Pro Drive’s EOS operating rhythm.
- **Primary users (named):** TODO — not “leadership”; name Integrator, department heads, etc.
- **Job to be done:** TODO — e.g. “run Level 10 without hunting across three tools”
- **v1 wedge (hypothesis):** Scorecard + Issues for Level 10 — *revisit after `/product-diagnostic`*
- **Out of scope for v1:** TODO
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

As of 2026-09-19, the agent authenticated as **ProDriveIT** can see these **public** repos:

- `CIPP`, `CIPP-API`, `cursor-for-product-managers`, `Pro-Drive-Public`, `second-brain-skills`

It **cannot** resolve `ProDriveIT/ProDrive-EOS` (or `prodrive-eos` / `EOS`). Private repos are not listable with the current token. To ground product work in existing code:

1. Confirm the exact repo name and org/user, **or**
2. Grant this agent/token read access to the private repo, **or**
3. Paste a repo snapshot / README into `initiatives/eos-operating-dashboard/` until access exists.

---

## 7. Open questions (block clarity)

1. Exact name and location of the EOS engineering repo?
2. Who is the named primary user of the EOS dashboard?
3. What is the current weekly workaround for Level 10 / Scorecard / Rocks?
4. Azure tenancy and hosting constraints (Entra ID, region, CIPP relationship)?
5. Is client reporting a separate product or an export surface of the same data spine?
