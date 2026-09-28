# Tasks: Monthly client service report (Quest pilot)

**Source PRD:** [prd-monthly-client-service-report.md](../prd/prd-monthly-client-service-report.md)  
**Status:** Parent tasks only. Sub-tasks are not written. Reply **Go** to expand.  
**Repo for the work:** `2026-01 reporting-kpi-automation` (not this PM workspace).  
**Branch:** create it in that repo when task 0.0 starts. Do not branch this notes repo for the Azure change.

Scale (PRD phase P5, all Insights clients, Logic App distribute) is out of this list.

## Relevant Files

- `Runbooks/Modules/Insights-Rules.psm1` — `Get-ClientMonthlyActivity` and the HTML helper. Hours total, resolution SLA, and the title dump land here.
- `Runbooks/Generate-Insights.ps1` — month job, blob pattern, SharePoint drop, run summary versions.
- `Runbooks/Modules/KPI-Functions.psm1` — locked category maps. Do not fork them.
- `Documentation/PRD-Monthly-Client-Service-Report.md` — engineering PRD v0.1.
- `Documentation/Monthly-Client-Service-Report.md` — companion scope note. Header already points at facts → Cowork; body still describes `client-pack-*.html`. Reconcile when the drafter choice is signed.
- `Documentation/Cutover-Checklist.md` — release checks for the month job.
- Tests live next to the runbook modules if that repo already has Pester coverage. Add or extend those tests for the six fact fields. Do not invent a second test project.

### Notes

- Facts path: 0 LLM calls.
- One drafter only, after question 1 on the PRD is answered.
- Looking ahead stays off the first template until question 2 is answered.

## Tasks

- [ ] 0.0 Create feature branch
- [ ] 1.0 Lock the Quest facts contract and record the open PRD answers
- [ ] 2.0 Emit Quest `facts.json` for one closed month from Azure
- [ ] 3.0 Copy that file into SharePoint Monthly Packs under Review rules
- [ ] 4.0 Produce one Quest-layout draft whose tiles match the facts file
- [ ] 5.0 Bruce approves and one Quest report is sent or walked through

Parent task 1 is product and ops. Tasks 2 and 3 are the kill switch (assumptions test A2). Task 4 waits on questions 1, 5, 6, and 7. Task 5 waits on a named buyer only for the recall note, not for the send itself.
