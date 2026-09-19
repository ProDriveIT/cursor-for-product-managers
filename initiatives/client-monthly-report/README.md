# Client Monthly Report

**Status:** Planning  
**Timeline:** TBD  
**Owner:** TBD  
**Stakeholders:** Bruce Penson (Visionary/MD), James Stock (Integrator), account / client success owners, client contacts (decision-makers on VC TAM)  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)  
**Related initiative:** [`../eos-operating-dashboard/`](../eos-operating-dashboard/) (shared operational data spine — dependency to clarify)

## Initiative Goal

Make proactive MSP value visible to clients every month via an auto-generated HTML report (emailed and/or client-visible), so that when reactive ticket volume drops, clients still understand what they are paying for.

The report must give a clear, client-facing picture of:

- **Proactive work** delivered for them
- **Initiatives** Pro Drive is pushing on their behalf
- **Alignment work** (strategy, roadmap, and relationship cadence)
- **Business updates** and their **VC TAM** meeting outcomes / next steps

**Why it matters:** Pro Drive has shifted from reactive break-fix to proactive, strategy-based client management. Reactive tickets and issues have dropped significantly — which is the intended outcome — but clients are starting to ask *"What are we doing? What are we paying for?"* This report is the proof-of-value surface for that model.

## Current Status

- [ ] User Research Complete
- [ ] Opportunities Identified
- [ ] Assumptions logged / leap-of-faith tests defined
- [ ] PRD Drafted
- [ ] Tasks Generated
- [ ] Development Started
- [ ] Analytics Setup Complete
- [ ] First client pilot report shipped

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
- The report is not a ticket dump; it is a narrative + evidence of proactive, initiative, and alignment work, plus TAM / business context.

### Constraints (from company context)

- Hosting / tooling: **Azure + Microsoft 365 + Copilot only** (self-hosted in Pro Drive; no third-party tools).
- Likely depends on a stable operational data contract (PSA, RMM, meeting notes, initiative tracking) — same spine the EOS dashboard may need. Confirm whether this is a separate product or an export of that spine before locking architecture.
- Delivery: auto-generated HTML, either emailed to clients or made visible in HTML format (or both).

### Open questions before heavyweight PRD

1. Named owner (PM / CS lead) and named pilot client(s)
2. Primary reader: economic buyer, technical contact, or both?
3. What "good" looks like for a client after reading (renew, expand, stop asking "what am I paying for," prepare for TAM)?
4. Data sources for proactive work, initiatives, alignment, and VC TAM updates
5. Generation cadence and who reviews before send (human-in-the-loop vs fully auto)
6. Relationship to EOS Operating Dashboard data spine

### Suggested next skills

1. `/product-diagnostic` — pressure-test demand before building the full report surface
2. Client interviews → `/create-interview-snapshots` (pilot clients who raised "what are we paying for?")
3. `/create-one-pager` once the wedge and audience are locked

---
*Created using initiatives template. Use `/setup-initiative` for new initiatives.*
