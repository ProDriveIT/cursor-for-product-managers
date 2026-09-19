# EOS Operating Dashboard

**Status:** Planning  
**Timeline:** TBD  
**Owner:** You (Integrator)  
**Stakeholders:** You (Integrator), Bruce (MD), Matt (management), third-party EOS implementer (name TBD), eng owner of Azure hosting  
**Engineering repo:** `ProDrive-EOS` (assumed) — **not accessible from this workspace yet**  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Make the **Integrator’s** EOS week workable: one opinionated portal where leadership updates Scorecard/KPIs, Rocks, and Issues (and you run L10 from the same SSOT) — so chase/admin cost drops and you can hold Bruce and Matt to the process.

**Working v1 hypothesis:** **B — Leadership L10 room mode** (fixed agenda, Scorecard, Issues, To-Dos on shared screen). Optimize for Integrator facilitation and Bruce’s “what next / why.”

**v1.1 (after first real L10s):** Matt’s 2-minute async Scorecard/Rock updates.

**Explicit non-goals for v1:** Time logging (dropped), AI chase/automation, Focus Days, department Traction, Bruce customization sandbox.

## Current Status

- [ ] User Research Complete
- [ ] Opportunities Identified
- [x] Failure post-mortem captured *(SSOT gap + MD process drift + passenger departments)*
- [x] Primary user named *(Integrator — you; contributors Bruce, Matt)*
- [x] Product diagnostic survived *(wedge = L10 room mode B; conditions apply)*
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
