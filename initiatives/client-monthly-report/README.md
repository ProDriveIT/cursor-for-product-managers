# Client Monthly Report

**Status:** Process live from PRD v0.1 (28 Sep 2026). Option **A** still stands (Bruce 20 Sep). Spine change is unsigned.  
**Timeline:** One Quest month. Facts match before any drafter. Scale stays gated.  
**Owner:** James Stock (Head of Operations); operator = Bruce Penson (**vCIO**); TAM = Danny Bray  
**Pilot:** Quest Fund Placement (`Quest Fund Placement Ltd`)  
**Stakeholders:** Bruce (vCIO), Danny (TAM), James (ops), Quest economic buyer (reaction test)  
**1-pager:** [`prd/1-pager-client-monthly-report.md`](./prd/1-pager-client-monthly-report.md) (approved)  
**Working PRD:** [`prd/prd-monthly-client-service-report.md`](./prd/prd-monthly-client-service-report.md)  
**Spine decision:** [`decision-prd-v0.1-spine.md`](./decision-prd-v0.1-spine.md) (proposed; canonical path unchanged until signed)  
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
- [x] 1-pager signed — option **A** (James 19 Sep, Bruce 20 Sep); scope lock confirmed
- [x] Engineering PRD v0.1 ingested (28 Sep) — facts.json + Cowork + Quest layout
- [x] Opportunities, solutions, assumptions v1 written (evidence is thin; no interview snapshots)
- [x] Working PRD, design brief, parent tasks
- [ ] James signs the spine decision (A / B / C) **← next**
- [ ] James answers the nine questions on the working PRD
- [ ] Sub-tasks (`Go` on the parent list)
- [ ] Quest facts match a manual count (A2; can kill Phase 1)
- [ ] User research: Bruce usability session snapshot, then Quest buyer reaction snapshot
- [ ] Synthesis (`/synthesize-snapshots`) once 3+ snapshots exist
- [ ] First Quest pilot report shipped *(Bruce-approved draft matching pack)*
- [x] Design brief — Quest layout, tokens proposed until the August HTML sample is linked
- [ ] Figma / new prototype — skip; the Quest sample is the layout
- [ ] Full / multi-client PRD — only if Phase 1 value test passes

## Framework path (designed gateways)

Order follows the Cursor-for-PMs skills plus the initiative-planner. Option **A** forbids interviewing the Quest buyer before the first draft. The kill switch is now the facts match (A2), not a missing HTML pack. CDH v1 is written; interview synthesis still waits on real sessions.

| # | Gateway | Skill / agent | Status | When it fires |
|---|---------|---------------|--------|----------------|
| 0 | Initiative setup | `/setup-initiative` | Done | — |
| 1 | Prior art + canonical path | (this folder) | Done | — |
| 2 | 1-pager decision | `/create-one-pager` | **Approved A** | — |
| 3 | Feasibility test | Assumptions A2 | **Next after the decision** | Quest `facts.json` matches a manual count on 6 fields. Mismatch with no written cause → stop |
| 4 | Opportunities | `/create-opportunities` | v1 proposed | Review notes #1 and #2 still open for James |
| 5 | Solutions | `/generate-solutions` | v1 | Human rounds were the 1-pager and PRD v0.1. Top 3 written |
| 6 | Assumptions + test cards | `/identify-test-assumptions` | v1 | LoFA = buyer recall, facts match, Bruce’s 15-minute review |
| 7 | Phase 1 PRD | `/create-prd` | Draft | Working copy from PRD v0.1. Nine questions unanswered |
| 8 | Task breakdown | `/generate-tasks` | Parents only | Reply Go for sub-tasks |
| 9 | ICE (optional) | `/calculate-ice-score` | Skip | Company rank is already #2; do not re-score the wedge |
| 10 | Usability test | operator session | After A2 passes | Bruce reviews one draft; James observes; 15 minutes, zero tile edits |
| 11 | Interview snapshots | `/create-interview-snapshots` | No transcripts | Snapshot the Bruce session; later snapshot the Quest buyer reaction. Do not run option B (buyer interview first) |
| 12 | Value test | 1-pager LoFA | After first send or walkthrough | Named Quest economic buyer reaction in writing |
| 13 | Synthesis | `/synthesize-snapshots` | Blocked | After 3–5 snapshots (Bruce, Quest buyer, ideally Danny / a second client later) |
| 14 | Analytics | `/analyze-metrics` | Not started | Baseline: Quest reactive volume vs pack contents for the pilot month. After send: whether the buyer can name the work |
| 15 | Design brief | `/create-design-brief` | Draft | Quest layout. Do not redraw; link the August sample before any visual change |
| 16 | Figma Make | `/generate-figma-prompt` | Optional | Static visual exploration of chrome. Skip if we ship pack HTML as-is |
| 17 | Working prototype | `/build-prototype` | Optional | Pack HTML *is* the Phase 1 artefact. Use this for Phase 2 narrative + vCIO/TAM meeting footer after Phase 1 exit |
| 18 | Phase 2 / multi-client PRD | `/create-prd` | Gated | Only if the value test passes. Then tasks again |

Discovery-researcher and initiative-planner subagents are available at those gates; do not skip the folders they write into.

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
- [Spine decision (unsigned)](./decision-prd-v0.1-spine.md)
- [Prior art (GitHub-Repos)](./prior-art-github-repos.md)
- [1-pager](./prd/1-pager-client-monthly-report.md)
- [Working PRD](./prd/prd-monthly-client-service-report.md)
- [Opportunities v1](./opportunities/opportunities-quest-value-visibility-v1.md)
- [Solutions v1](./solutions/solutions-quest-value-visibility-v1.md)
- [Assumptions v1](./assumptions/assumptions-quest-value-visibility-v1.md)
- [Design brief](./design/design-brief-quest-monthly-report.md)
- [Parent tasks](./tasks/tasks-monthly-client-service-report.md)
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

### Open questions (post approval)

1. Chosen pilot `YYYY-MM` + confirmed Quest `client-pack-*.html` in KPI Insights
2. Named Quest economic buyer for the reaction test (operator is Bruce; reader may differ)
3. Path to the **external reports repo** for HTML templates
4. Whether packs for Quest land in `{AccountSlug}/` or still flat in KPI Insights root
5. Danny acknowledgement on TAM cadence / Phase 2 meeting inputs (not blocking Phase 1)

### Next step

James marks A, B, or C on [`decision-prd-v0.1-spine.md`](./decision-prd-v0.1-spine.md) and answers the nine questions on the working PRD. Then reply **Go** to expand sub-tasks. Facts for Quest are still the kill switch: if the six fields do not match a manual count, stop.

---
*Created using initiatives template. Use `/setup-initiative` for new initiatives.*
