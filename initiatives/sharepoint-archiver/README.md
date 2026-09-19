# SharePoint Archiver

**Status:** Operational — Quest, CSC, Pixel COMPLETE (Aug 2026); MSP Org enrolled  
**Owner:** James Stock  
**Stakeholders:** Client SharePoint owners facing OneDrive 300k sync limits; Pro Drive delivery engineers  
**Engineering:** https://github.com/ProDriveIT/prodrive-agent-ops/tree/main/products/sharepoint-archiver  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Deliver a repeatable, non-synced Archive library pattern (world icon) so large SharePoint estates stay under OneDrive sync limits without losing retention/access design — runbook Phases 0–6, Agent Ops cert on worker.

## Current Status

- [x] RUNBOOK Phases 0–6 documented
- [x] Quest, CSC, Pixel COMPLETE Aug 2026
- [x] MSP Org enrolled Sep 2026 (Secretaries Internal Files empty; real volume = MSP Org Internal Files — retarget before Phase 4)
- [ ] Customer pack deferred until Travel packaging process finishes, then reuse same process
- [ ] User Research Complete
- [ ] Opportunities / PRD for productised packaging

## Folder Structure

- **[user-interviews/](./user-interviews/)** - Customer discovery and research
- **[opportunities/](./opportunities/)** - Identified opportunities and pain points
- **[assumptions/](./assumptions/)** - Assumption logs and test cards
- **[solutions/](./solutions/)** - Solution explorations
- **[design/](./design/)** - Design briefs and Figma prompts
- **[prototype/](./prototype/)** - Working prototype and companion doc
- **[product-analytics/](./product-analytics/)** - Data analysis and metrics
- **[prd/](./prd/)** - Product Requirements Document
- **[tasks/](./tasks/)** - Implementation tasks

## Notes

- Requires SharePoint application permission `Sites.FullControl.All` on Agent Ops app
- Cursor Cloud: admin-consent + Graph discovery only — PnP runs on worker with cert
- Not Azure Automation in v1 (project/on-demand)
- Not SPAT; not Travel

---
*Created using initiatives template.*
