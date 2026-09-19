# EOS Operating Dashboard

**Status:** Planning  
**Timeline:** TBD  
**Owner:** James (Integrator)  
**Stakeholders:** James (Integrator), Bruce (MD), Matt (management), third-party EOS implementer (name TBD), eng owner of Azure hosting  
**Engineering repo:** `ProDrive-EOS` (assumed) — **not accessible from this workspace yet**  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)
**1-pager:** [`prd/1-pager-eos-operating-dashboard.md`](./prd/1-pager-eos-operating-dashboard.md)

## Initiative Goal

Make **James’s** EOS week workable: Leadership L10 room mode on Azure / M365 / Copilot so Friday prep stays under 20 minutes, Monday L10 runs pure EOS from one Scorecard/agenda/Issues/To-Dos screen, and Bruce/Matt have a single plan to follow.

**Success bar:** 5 consecutive pure-EOS leadership L10s; KPIs via dashboard and/or current automated+manual → spreadsheet path mirrored to the Scorecard.

**Working v1:** L10 room mode only. **v1.1:** Matt async updates. **Out:** time logging, AI chase, departments, Focus Days, third-party SaaS.

## Current Status

- [ ] User Research Complete
- [ ] Opportunities Identified
- [x] Failure post-mortem captured
- [x] Primary user named *(James — Integrator)*
- [x] Product diagnostic survived *(wedge = L10 room mode)*
- [x] One-pager drafted *([prd/1-pager-eos-operating-dashboard.md](./prd/1-pager-eos-operating-dashboard.md))*
- [ ] One-pager signed off *(James, Bruce, Matt)*
- [ ] PRD Drafted / prototype built
- [ ] Tasks Generated
- [ ] Development Started (in engineering repo)
- [ ] Analytics Setup Complete

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
- [Diagnostic notes](./diagnostic-eos-dashboard.md)

## Notes

- Prior attempt: inconsistent artifacts (loop/notes/Teams/SharePoint); Bruce adapted EOS; peers didn’t challenge; implementer hired for accountability; ops Traction collapsed to solo meeting.
- Design implication: **rigidity over flexibility** in v1.
- This PM toolkit holds discovery/specs only; app code lives in the engineering repo once accessible.
- Client monthly reports are a separate later initiative.
- CIPP / CIPP-API may matter for M365/Azure context — not the EOS product.

---
*Created from initiatives template. Use `/setup-initiative` for new initiatives.*
