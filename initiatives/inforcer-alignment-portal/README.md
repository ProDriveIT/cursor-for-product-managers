# Inforcer Alignment Portal

**Status:** Live (internal) — Azure Static Web App  
**Owner:** James Stock  
**Stakeholders:** Pro Drive engineers running Inforcer Blueprint alignment workshops  
**Engineering:** https://github.com/ProDriveIT/inforcer-alignment-portal  
**Content source:** Supporting Data `70-policy-and-procedures/PDKB/scripts/` (generate → publish)  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Provide a branded, CSS-intact browsable portal for Inforcer Blueprint alignment (baseline order, deployment guide, per-baseline policy impact) so the team can work alignments live — IT Glue remains system of record but strips CSS.

## Current Status

- [x] Azure Static Web App (Standard) — subscription *Pro Drive Internal Automations*
- [x] Entra ID lock to Pro Drive IT Limited tenant
- [x] CI deploy on push to `main` (`site/` upload)
- [ ] Content regen cadence owned / documented in this initiative
- [ ] User Research Complete
- [ ] Opportunities for client-facing variant (if ever)

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

- Pages are **generated**, not hand-edited — regenerate from PDKB scripts then `publish-alignment-portal.ps1`
- App registration client secret rotates every 2 years (see repo README)
- Same hosting model pattern as CIPP SWA

---
*Created using initiatives template.*
