# Client Monthly Report

**Status:** Planning — 1-pager drafted for Quest pilot decision  
**Timeline:** Align with Reporting Agent Phase 1 (one Quest month after pack confirmed)  
**Owner:** James Stock (Head of Operations); operator = Bruce Penson (**vCIO**); TAM = Danny Bray  
**Pilot:** Quest Fund Placement (`Quest Fund Placement Ltd`)  
**Stakeholders:** Bruce (vCIO), Danny (TAM), James (ops), Quest economic buyer (reaction test)  
**1-pager:** [`prd/1-pager-client-monthly-report.md`](./prd/1-pager-client-monthly-report.md)  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)  
**Prior art:** [`prior-art-github-repos.md`](./prior-art-github-repos.md)  
**Canonical path (SSOT):** [`canonical-path.md`](./canonical-path.md) · [GitHub-Repos twin](https://github.com/ProDriveIT/GitHub-Repos/blob/main/00%20Meta/Client-Monthly-Report-Canonical-Path.md)  
**Related engineering:** [GitHub-Repos — reporting-kpi-automation](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-01%20reporting-kpi-automation), [agent-ecosystem-copilot (Reporting Agent)](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-09%20agent-ecosystem-copilot), [archived reporting-client — SUPERSEDED](https://github.com/ProDriveIT/GitHub-Repos/tree/main/90%20Archive/2026-01%20reporting-client)  
**Related initiative:** [`../eos-operating-dashboard/`](../eos-operating-dashboard/) (EOS Facilitator / EHAN handoff — separate surface)

## Initiative Goal

Make proactive MSP value visible to clients every month via an auto-generated HTML report (emailed and/or client-visible), so that when reactive ticket volume drops, clients still understand what they are paying for.

The report must give a clear, client-facing picture of:

- **Proactive work** delivered for them
- **Initiatives** Pro Drive is pushing on their behalf
- **Alignment work** (strategy, roadmap, and relationship cadence)
- **Business updates** and their **vCIO / TAM** meeting outcomes / next steps

**Why it matters:** Pro Drive has shifted from reactive break-fix to proactive, strategy-based client management. Reactive tickets and issues have dropped significantly — which is the intended outcome — but clients are starting to ask *"What are we doing? What are we paying for?"* This report is the proof-of-value surface for that model.

## Current Status

- [x] Prior art inventoried (GitHub-Repos — see [`prior-art-github-repos.md`](./prior-art-github-repos.md))
- [x] Stalled starts marked **superseded** / DO NOT RESUME (GitHub-Repos hygiene 19-09-2026)
- [x] Canonical path SSOT published ([`canonical-path.md`](./canonical-path.md))
- [x] Pilot named: Quest Fund Placement · vCIO Bruce · TAM Danny · ops James
- [x] 1-pager drafted — [`prd/1-pager-client-monthly-report.md`](./prd/1-pager-client-monthly-report.md)
- [ ] 1-pager signed (Bruce Approve on option A)
- [ ] Quest Insights pack confirmed for chosen `YYYY-MM`
- [ ] User Research Complete *(Quest buyer reaction after first approved cycle)*
- [ ] Opportunities Identified
- [ ] Assumptions logged / leap-of-faith tests defined
- [ ] Full PRD *(only if pilot proves value; Phase 1 does not need a heavyweight PRD)*
- [ ] Tasks Generated
- [ ] Development Started *(engineering already in flight via Insights packs + Reporting Agent docs)*
- [ ] First Quest pilot report shipped *(Bruce-approved draft matching pack)*

## Folder Structure

- **[user-interviews/](./user-interviews/)** - Customer discovery and research
  - `snapshots/` - Individual interview insights using `/create-interview-snapshots`
  - `synthesis/` - Cross-interview analysis and patterns
  - `transcripts/` - Raw interview recordings and notes
- **[opportunities/](./opportunities/)** - Identified opportunities and pain points
- **[assumptions/](./assumptions/)** - Assumption logs and test cards from `/identify-test-assumptions`
- **[solutions/](./solutions/)** - Solution explorations from `/generate-solutions`
- **[design/](./design/)** - Design briefs and Figma prompts from `/create-design-brief` and `/generate-figma-prompt`
- **[prototype/](./prototype/)** - Working prototype and companion doc from `/build-prototype`
- **[product-analytics/](./product-analytics/)** - Data analysis and metrics
- **[prd/](./prd/)** - Product Requirements Document using `/create-prd`
- **[tasks/](./tasks/)** - Implementation tasks using `/generate-tasks`

## Quick Links

- [Canonical path (SSOT)](./canonical-path.md)
- [Prior art (GitHub-Repos)](./prior-art-github-repos.md)
- [1-pager](./prd/1-pager-client-monthly-report.md)
- [User Research Summary](./user-interviews/synthesis/)
- [Priority Opportunities](./opportunities/)
- [Assumptions & Tests](./assumptions/)
- [Solution Explorations](./solutions/)
- [Prototype & Companion Doc](./prototype/)
- [Implementation Tasks](./tasks/)

## Notes

### Problem framing (working)

- Success of proactive management looks like *fewer* tickets — which currently reads to some clients as *less* service.
- The report is not a ticket dump; it is a narrative + evidence of proactive, initiative, and alignment work, plus **vCIO / TAM** cadence and business context.

### What already exists (do not ignore)

1. **Archived value-add generator** — same “background work you can’t see” problem; STOP’d for RTEM focus Aug 2026.
2. **Insights client packs (WIP-027)** — Autotask-based monthly HTML packs (preventative vs end-user, jobs, alignment).
3. **Reporting Agent (Sep 2026)** — Copilot draft → **vCIO** approve → send; Phase 2 narrative + meeting footer.

Engineering decisions already locked: HTML artefact, vCIO sign-off, numbers from packs only, no auto-send. Challenge content and pilot choice — not the spine — unless evidence says the spine fails.

### Constraints (from company context + prior art)

- Hosting / tooling: **Azure + Microsoft 365 + Copilot only** (self-hosted in Pro Drive; no third-party tools).
- Reuse **reporting-kpi-automation** Insights packs; do not rebuild KPI math.
- Delivery: HTML draft → vCIO approval → email / portal (human-gated).

### Open questions (post 1-pager)

1. Bruce sign-off on option **A** in the 1-pager
2. Chosen pilot `YYYY-MM` + confirmed Quest `client-pack-*.html` in KPI Insights
3. Named Quest economic buyer for the reaction test (operator is Bruce; reader may differ)
4. Path to the **external reports repo** for HTML templates
5. Whether packs for Quest land in `{AccountSlug}/` or still flat in KPI Insights root

### Suggested next step after sign-off

Confirm Quest pack for the chosen month → Bruce runs one Reporting Agent draft → approve cycle → capture Quest buyer reaction.

---
*Created using initiatives template. Use `/setup-initiative` for new initiatives.*
