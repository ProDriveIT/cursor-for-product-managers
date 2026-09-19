# EOS Operating Dashboard

**Status:** Planning  
**Timeline:** TBD  
**Owner:** TBD (Pro Drive product owner)  
**Stakeholders:** TBD — Integrator, Visionary, department heads, eng owner of Azure hosting  
**Engineering repo:** `ProDrive-EOS` (assumed) — **not accessible from this workspace yet**  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Enable a **second EOS adoption** at Pro Drive by putting L10, Focus Days, Traction, and related operating work in one Azure-hosted site — so the management team (later departments) is not killed by multi-tool maintenance like last time. Persist structured data for later reporting, analysis, and agents.

**Working v1 hypothesis (unvalidated):** Ship only the meeting loop that removes the *named* admin burden from the failed attempt (likely Scorecard + Issues + To-Dos for L10). Defer Focus Days, full Traction suite, department rollouts, analytics, and agents until one team completes ~8 consecutive L10s.

## Current Status

- [ ] User Research Complete
- [ ] Opportunities Identified
- [ ] Product diagnostic survived *(in progress — pre-adoption; prior attempt abandoned)*
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

- This PM toolkit repo holds discovery and specs only. Application code lives in the EOS engineering repo once access is confirmed.
- Client monthly reports are intentionally **not** in this initiative; they depend on a clear data spine and should get their own folder later.
- CIPP / CIPP-API under ProDriveIT may matter for M365/Azure tenant context — do not assume they are the EOS product.

---
*Created from initiatives template. Use `/setup-initiative` for new initiatives.*
