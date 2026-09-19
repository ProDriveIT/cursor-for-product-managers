# PD Performance Hub

**Status:** Built · adoption unclear (last engineering push ~Mar 2026)  
**Owner:** James Stock  
**Stakeholders:** Managers/directors using team KPI Excels and BreatheHR quarterly reviews  
**Engineering:** https://github.com/ProDriveIT/pd-performance-hub  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Give managers a single desktop app to view/enter team KPIs from SharePoint Excels and generate HTML/PDF review packs for BreatheHR — reducing spreadsheet friction for monthly/quarterly reviews.

## Current Status

- [x] Flask app + Windows installer path
- [x] Power Platform alternate path documented under `power-platform/`
- [ ] Confirm current adoption (who still launches it?)
- [ ] Decide: keep desktop, migrate Power Platform, or archive in favour of EHAN / KPI spine
- [ ] User Research Complete
- [ ] Opportunities / PRD if revived

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

### Org codes hardcoded in app

| Code | Manager | Department |
|------|---------|------------|
| BP | Bruce Penson | Leadership |
| MT | Matt Taylor | Leadership |
| JS | James Stock | Service Desk |
| DB | Danny Bray | Technology Success |
| CR | Chris Ross-Lewin | Sales & Marketing |
| DS | Dan Sheather | Professional Services |

### Relationship to company Scorecard

Team KPI Excels and this hub are **engineer review evidence** — not the company EOS Scorecard. Do not mix answers with Hub Lists or Azure Insights packs (see company context Scorecard layers).

### Suggested next step

James: 15-minute adoption check with managers (still installed? still used?). If unused, archive initiative; if used, decide desktop vs Power Platform vs EHAN read-path.

---
*Created using initiatives template.*
