# MSP Meeting Minutes

**Status:** Live · stable v1.0 — **change freeze without James Stock input**  
**Timeline:** In production (operational since 2026); maintenance only under explicit approval  
**Owner:** James Stock  
**Stakeholders:** MSP CoSec end users (client company secretaries / chairs); Pro Drive support engineers; client styles qed, avca, swc, wakam, rgg  
**Engineering:** https://github.com/ProDriveIT/msp-meeting-minutes-agent  
**Company context:** [`../../company-level-context/prodrive-context.md`](../../company-level-context/prodrive-context.md)

## Initiative Goal

Keep the live board-meeting minutes pipeline reliable: SharePoint upload (agenda + meeting pack + MP3) → Azure Speech + OpenAI → client-styled Word draft for Chairman review — without regressing production while James is capacity-locked on EOS → client reports → Travel.

**Why it is a product:** Named client users, stable v1.0, dedicated Azure Functions + Power Automate flow, documented onboarding. Not a one-off script.

## Current Status

- [x] Live in production (stable badge in repo README)
- [x] End-user + support-engineer documentation
- [x] Multi-client style mapping (`client_configs.json`)
- [ ] Change-control process written (who may propose; how freeze lifts) — **open action**
- [ ] Backlog triage of Suggested Improvements (31-03-2026) under freeze
- [ ] User Research Complete *(not required while frozen unless defect)*
- [ ] Opportunities / PRD for v2 — blocked until James unlocks

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

### Change freeze (owner instruction, 2026-09-19)

James Stock: product is live and working well; **it cannot be updated without his input**. Agents and engineers must not ship flow, prompt, or Function changes from this toolkit alone. Capture proposals here; wait for explicit approval.

### What the system does

1. User uploads Agenda (PDF), Meeting Pack (PDF), Audio (MP3) under `MSP CoSec/<Client>/<Meeting>/`
2. Creates `ready.txt` → Power Automate triggers
3. Azure Speech transcription → OpenAI minutes (example-aware) → per-section QA → `GenerateMinutesDocx`
4. Draft `.docx` lands in `Minutes/`; email notification

### Constraints

- Azure + M365 + Power Automate Premium only
- British English; board-level formality; banned generic phrases
- No secrets in repo; meeting content confidential

### Suggested next step (when unfrozen)

Define a one-page change-control: severity classes (P0 defect vs enhancement), who reviews, and a rollback path for the production flow (v21 docs in repo `Documentation/Flow-Deploy-Import.md`).

---
*Created using initiatives template. Use `/setup-initiative` for new initiatives.*
