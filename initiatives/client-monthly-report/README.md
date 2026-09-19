# Client Monthly Report

**Status:** Planning — prior art exists; consolidate, don’t restart  
**Timeline:** TBD (align with Reporting Agent Phase 1–2 in GitHub-Repos)  
**Owner:** TBD (product); builder historically James; operator = client’s **vCIO**  
**Stakeholders:** Client **vCIO**s (primary operators), Bruce Penson (Visionary/MD), James Stock (Integrator / builder), VSOs (meeting calendar), account / TAM contacts  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)  
**Prior art:** [`prior-art-github-repos.md`](./prior-art-github-repos.md)  
**Related engineering:** [GitHub-Repos — reporting-kpi-automation](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-01%20reporting-kpi-automation), [agent-ecosystem-copilot (Reporting Agent)](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-09%20agent-ecosystem-copilot), [archived reporting-client](https://github.com/ProDriveIT/GitHub-Repos/tree/main/90%20Archive/2026-01%20reporting-client)  
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
- [ ] User Research Complete
- [ ] Opportunities Identified
- [ ] Assumptions logged / leap-of-faith tests defined
- [ ] PRD Drafted *(prefer 1-pager that locks onto Reporting Agent roadmap, not a greenfield PRD)*
- [ ] Tasks Generated
- [ ] Development Started *(engineering already in flight via Insights packs + Reporting Agent docs)*
- [ ] Analytics Setup Complete
- [ ] First client pilot report shipped *(Reporting Agent Phase 1 exit criteria)*

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

- [Prior art (GitHub-Repos)](./prior-art-github-repos.md)
- [PRD](./prd/)
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

### Open questions before heavyweight PRD

1. Named product owner vs builder (James) vs pilot **vCIO**
2. Named pilot client(s) with a known-good `client-pack-*.html`
3. Primary *client* reader: economic buyer, technical contact, or both? *(operator is vCIO; reader may differ)*
4. What “good” looks like after reading (renew, expand, stop asking “what am I paying for,” prepare for next **vCIO / TAM** meeting)
5. Path to the **external reports repo** for HTML templates
6. Whether PM discovery validates locked workflow decisions or only report *content*

### Suggested next skills

1. `/product-diagnostic` — pressure-test demand against the *existing* Reporting Agent path (not a blank slate)
2. `/create-one-pager` that cites prior art and locks wedge = Reporting Agent Phase 1 pilot
3. Optional: interview pilot client buyers who raised “what are we paying for?” → `user-interviews/`

---
*Created using initiatives template. Use `/setup-initiative` for new initiatives.*
