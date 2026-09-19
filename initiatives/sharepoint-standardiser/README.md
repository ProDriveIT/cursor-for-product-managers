# SharePoint Standardiser

**Status:** Core product (Estate Control spine) — Phase 0 audit live; provisioning later  
**Owner:** James Stock  
**Stakeholders:** Client SharePoint / M365 owners; Pro Drive PS / Tech Success; Principia and dual-site pattern clients  
**Engineering:** https://github.com/ProDriveIT/prodrive-agent-ops/tree/main/products/sharepoint-standardiser  
**Product map:** [`../../company-level-context/product-vision-and-strategy/product-map.md`](../../company-level-context/product-vision-and-strategy/product-map.md)  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Make SharePoint / Teams estates measurable against **declarative designs** so Pro Drive can sell and deliver Align work under Pro Drive 360 — reducing reactive tickets from sprawl, bad structure, and permission chaos (RTEM), then package the same motion as a service (and later as an externalisable module).

**Why core:** Without Standardiser, Archiver / SPAT / Inforcer look like unrelated tools. With it, they become modules on a design → audit → remediate spine.

## Current Status

- [x] Declared core product (elevated from “below bar”, 2026-09-19)
- [x] Designs: `prodrive-dual-site`, `principia-project-hub`
- [x] Phase 0 scripts: site audit, compare-to-design, full client audit, M365 workspace inventory
- [x] Dogfood ACL apply on Pro Drive Files (12 Sep 2026)
- [ ] Client registry coverage for all Estate Control clients
- [ ] Billable SOW / SKU language (“Estate Design & Alignment”)
- [ ] Provisioning from designs (future — not Phase 0)
- [ ] RTEM baseline categories defined for before/after
- [ ] User Research Complete
- [ ] Opportunities / PRD for service packaging

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

### Not Archiver

Archiver moves cold folders for sync-limit remediation. Standardiser **measures structure** against a design and supports governance programmes. They attach; they are not the same product.

### Auth

Same multi-tenant Agent Ops cert (`ProDrive-Agent-Ops`). PnP needs SharePoint `Sites.FullControl.All`. Teams inventory uses Graph `Group.Read.All` + `Sites.Read.All`.

### Commercial framing (draft)

| Goal | How Standardiser contributes |
|------|------------------------------|
| **A RTEM** | Prevent tickets from mis-structured libraries, shadow sites, and permission sprawl |
| **B Services** | Sell Phase 0 audit + Align programme as PS; attach Archiver / SPAT / Inforcer modules |
| **C External** | Later — only after enrol + support model; not ready to sell outside MSP base yet |

### Suggested next step

Pick one client with a registered design (e.g. Principia or Copper Street reference) → run full `Invoke-SpoDesignAudit` → turn gaps into a priced Align SOW draft → log which ticket types would have been avoided (RTEM link).

---
*Created using initiatives template.*
