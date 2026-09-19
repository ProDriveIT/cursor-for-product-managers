# EOS Operating Dashboard

**Status:** Planning  
**Timeline:** TBD  
**Owner:** TBD (Pro Drive product owner)  
**Stakeholders:** Bruce (MD), third-party EOS implementer (name TBD), management team, eng owner of Azure hosting  
**Engineering repo:** `ProDrive-EOS` (assumed) — **not accessible from this workspace yet**  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Enable a **second EOS adoption** with a single Azure-hosted **system of record** for leadership operating rhythm — so process isn’t reinvented each week in Teams/SharePoint/notes, and the third-party implementer (plus peers) can point at an agreed plan when the MD drifts off EOS.

**Working v1 hypothesis:** Opinionated **leadership L10 only** (fixed agenda, Scorecard, Rocks, Issues, To-Dos). Defer Focus Days, department Traction, analytics, and agents until ~8 consecutive L10s with real multi-person participation.

**Explicit non-goal for v1:** Software that “manages Bruce.” Authority stays with implementer + leadership; product makes drift visible and costly to ignore.

## Current Status

- [ ] User Research Complete
- [ ] Opportunities Identified
- [x] Failure post-mortem captured *(SSOT gap + MD process drift + passenger departments)*
- [ ] Product diagnostic survived *(in progress)*
- [ ] One-pager drafted
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
