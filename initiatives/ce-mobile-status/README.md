# CE Mobile Status

**Status:** Live — dogfood (Pro Drive) + Brunner UK; Azure Automation 3×/day  
**Owner:** James Stock  
**Stakeholders:** CE / calling enablement operators; client phone readiness owners  
**Engineering:** https://github.com/ProDriveIT/prodrive-agent-ops/tree/main/products/ce-mobile-status  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Maintain a reliable Green/Amber/Red SharePoint list of CE phone readiness so CE work only starts when the gate passes — synced unattended via Agent Ops cert + Azure Automation (07:00 / 12:00 / 17:00 UK).

## Current Status

- [x] Product folder + deployment plan in Agent Ops
- [x] Dogfood on Pro Drive
- [x] First client Brunner UK
- [x] Azure Automation Account `aa-pd-ce-mobile-ops`
- [ ] Broader client enrolment backlog prioritised
- [ ] User Research Complete
- [ ] Opportunities / PRD for next capability

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

- First product on the shared **ProDrive-Agent-Ops** Entra app (certificate auth)
- SOP: `SOP-CE-Phone-Readiness-Gate.md` in product folder
- Telemetry via `Write-AgentOpsTelemetry` with product + clientSlug tags

---
*Created using initiatives template.*
