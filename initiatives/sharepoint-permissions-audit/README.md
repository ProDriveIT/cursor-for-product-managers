# SharePoint Permissions Audit (SPAT)

**Status:** Live — Pixel Global in production use  
**Timeline:** Hosted Aug 2026; Pixel link shared 28 Aug 2026  
**Owner:** James Stock  
**Stakeholders:** Client IT Contacts (Pixel: Jamie Hanna, John Tytherleigh); Pro Drive ops  
**Engineering:** https://github.com/ProDriveIT/prodrive-agent-ops/tree/main/products/sharepoint-permissions-audit  
**Status doc:** `products/sharepoint-permissions-audit/docs/STATUS.md` in Agent Ops  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Give client IT Contacts a safe, snapshot-based answer to “who can open this?” on pictured SharePoint places — without live Graph on click and without permission editing in v1.

## Current Status

- [x] Hosted on Azure (`rg-pd-spat-ops`, UK South)
- [x] First client Pixel Global live (`/c/pixel-global`)
- [x] Named-account gate + company isolation
- [ ] Quest clientLoginEnabled (review-only; do not send `/c/quest`)
- [ ] Custom domain / packaging parity with Travel (if desired)
- [ ] User Research Complete
- [ ] Opportunities / PRD for v2 (edit? more sites?)

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

- Scans use **Agent Ops cert**; UI uses second Entra app **ProDrive-SPAT**
- Not Travel. Not SharePoint Archiver. No permission editing in v1
- Do not send Pixel users the generic ops URL (opens every enrolled picture)
- Layout/copy/auth changes must keep Files opening for named Pixel people

---
*Created using initiatives template.*
