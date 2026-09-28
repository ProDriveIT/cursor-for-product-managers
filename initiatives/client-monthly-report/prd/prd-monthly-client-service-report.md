# PRD: Monthly client service report (Quest pilot)

**Initiative:** client-monthly-report  
**Version:** 0.2 working copy (28 Sep 2026)  
**Status:** Draft. Ingested from engineering PRD v0.1. Spine choice is unsigned.  
**Source:** `Documentation/PRD-Monthly-Client-Service-Report.md` in `2026-01 reporting-kpi-automation` (v0.1, 28 Sep 2026)  
**Owner:** James Stock (ops). Operator: Bruce Penson (vCIO). TAM: Danny Bray.  
**Selected solution:** Solution 1 in [solutions v1](../solutions/solutions-quest-value-visibility-v1.md), fenced by [decision-prd-v0.1-spine.md](../decision-prd-v0.1-spine.md)  
**Audience:** James and whoever extends Insights. A junior engineer should be able to build the facts path from this page.

This page is the product spec for the Quest cycle. It does not replace the engineering PRD. Where they disagree, the [decision note](../decision-prd-v0.1-spine.md) wins until James signs it.

## 1. Introduction

Quest’s buyer cannot see most of the managed service. Preventative work, alignment, and estate fixes do not show up as tickets they feel. Bruce currently rebuilds that month from Autotask. A model that is handed raw exports will invent hours and SLA percentages.

The pilot produces one client-facing report for Quest Fund Placement for one closed calendar month:

1. Azure Automation counts the month and writes `facts.json`.
2. One drafter writes the Quest layout into a Review folder. Tiles are copied from `facts.json`.
3. Bruce approves. A human sends. The issued file and the facts file are kept.

Goal: Bruce spends the review on wording. The buyer can name two pieces of non-break-fix work after they see the report. Work order #2 exits on that report, not on a multi-client rollout.

## 2. Goals

| Goal | Target |
|------|--------|
| Facts without a model | One complete `facts.json` for Quest for the chosen closed month |
| Number lock | Every tile figure in the draft equals the same field in `facts.json` (6 of 6 on the test card) |
| Bruce gate | 1 of 1 sends has an approval record before the client receives it |
| Time to draft | Review file exists within 1 working day after facts land |
| Buyer outcome | Named Quest buyer states 2 non-break-fix items from the report |
| Cost | 0 LLM calls on the Azure facts path |

Coverage of all `INSIGHTS_CLIENT_ENABLED` accounts is a later phase. It is not a goal of this PRD.

## 3. User stories

**US-1 Facts without AI**  
As ops, I want Azure to emit `facts.json` for Quest so the drafter never recounts tickets.

- August (or the chosen month) includes ticket count, hours, incident count, first-response SLA %, resolution SLA % (or a documented field name if the export differs), title list, and PD Client Wide titles.
- The run reads `kpi-results-month-js-*.json`, not the week pattern.
- `run-summary-insights-*.json` records LayoutVersion and RulesVersion.

**US-2 Narrative draft**  
As Bruce, I want a Quest-layout draft in Review so I edit judgment, not math.

- Draft tiles equal `facts.json`.
- Exec summary, What we did, and at most 3 insight cards are present.
- The draft names no end user.
- Looking ahead is omitted on this first cycle (see Non-goals). If James signs decision B, a date appears only when Meeting Tracker / LCI has one. A missing date is left blank.

**US-3 Bruce gate**  
As Pro Drive, no client send happens until Bruce approves.

- The drafter writes only under `Review/`.
- An Approved state exists before any send step runs. The mechanism is an open question (folder move, content type, or checklist).

**US-4 Estate story**  
As a Quest reader, I see wider-base improvements when that month has them.

- Across wider base bullets use `PD Client Wide work` titles and/or the curated Pro Drive statements for that month. If neither has content, the section says so in one plain line. It does not invent themes.

## 4. Functional requirements

1. The system must write one `facts.json` per client per calendar month from the rolling-180 time-entry spine, filtered to that month and that Autotask account.
2. The system must set `accountName`, `monthLabel`, `issuedDate`, `accountManagerName`, `ticketCount`, `incidentCount`, `hoursLogged`, `helpdeskSlaEligibleCount`, `firstResponseSlaMetPercent`, `resolutionSlaMetPercent`, `ticketTitles`, `pdClientWideTitles`, `rulesVersion`, and `runId`.
3. The system must allow `preparedFor` to be null until the contact source is chosen.
4. The system must count tickets that have time logged in the month. Closure date alone must not define the month.
5. The system must use the category maps already locked in `KPI-Functions.psm1` (reactive, proactive, jobs, alignment). Incident count uses Ticket Type when that column is on the export.
6. The system must compute helpdesk SLA on the SLA-eligible set only, and must show the percent as a number, not as colour alone.
7. The system must list distinct ticket titles with time in the month. That list is drafter input. It is not a client-facing dump.
8. The system must list titles for account `PD Client Wide work` with time in that month.
9. The system must place facts at `Monthly Packs/{Client}/{yyyy-MM}/facts.json` on `https://prodrive365.sharepoint.com/sites/Files` (KPI Insights tree). An optional skeleton HTML may sit beside it with tiles already filled.
10. The system must run `Generate-Insights` against the month KPI blob pattern `output/kpi-results-month-js-*.json`.
11. The drafter must produce one Quest layout with: header, executive summary, tiles, What we did, Insights (at most 3 cards: Done / In effect / Next), Across wider base, footer. Looking ahead is out of the first Quest cycle unless decision B is signed.
12. The drafter must copy tile figures from `facts.json`. It must not recount titles to “check” a total.
13. The drafter must write the draft only under that month’s `Review/` folder.
14. The system must block the send path until an Approved marker is set by Bruce.
15. The system must keep the issued HTML or PDF and the month’s `facts.json` for Assurix evidence (T130–T133, T151).
16. The system must not name Quest end users in the narrative.
17. UK English. Brand name Pro Drive.
18. Setting `INSIGHTS_CLIENT_ENABLED` to false must stop this pack without changing scorecards.

### Facts contract

```json
{
  "accountName": "Quest Fund Placement",
  "monthLabel": "August 2026",
  "issuedDate": "2026-09-27",
  "accountManagerName": "Bruce Penson",
  "preparedFor": null,
  "ticketCount": 30,
  "incidentCount": 7,
  "hoursLogged": 19.2,
  "helpdeskSlaEligibleCount": 23,
  "firstResponseSlaMetPercent": 100,
  "resolutionSlaMetPercent": 100,
  "ticketTitles": ["..."],
  "pdClientWideTitles": ["..."],
  "rulesVersion": "7+",
  "runId": "..."
}
```

The numbers above are the PRD’s illustration for Quest August 2026. They are not verified. A2 in the assumptions file is the check. Autotask account label on the 1-pager is `Quest Fund Placement Ltd`; the facts file must use the account name the month job already keys on, and the report header must show the client-facing name.

## 5. Non-goals (this cycle)

- A second client, or every `INSIGHTS_CLIENT_ENABLED` account.
- Auto-email, even with an approve button (PRD A1).
- Multi-month trend tiles (A2).
- A client portal deep link (A3).
- Azure OpenAI inside the runbook (A4), unless Cowork and the Reporting Agent both cannot draft.
- A Logic App fan-out to all clients (A5).
- Stitching Huntress, Mimecast, or Inforcer PDFs into the pack.
- A new Teams or SharePoint list for TAM / vCIO dates.
- Feeding the full rolling-180 Excel to the drafter.
- Looking-ahead dates on the first Quest send, unless James signs decision B.
- Reviving `Generate-ClientValueAddReport.ps1`.
- Replacing weekly KPI scorecards.

## 6. Design considerations

Quest layout is the UI. One template. Tiles are authoritative; prose explains them. At most three insight cards. No ticket IDs on the client page unless Bruce types one in. Semantic headings. The settled sample named in the engineering PRD is Quest Fund Placement, August 2026 (`Quest-August-2026-service-report.html` / `.pdf`). That file was not in the automation repo when this spec was written. Do not redraw the chrome. Brief: [design-brief-quest-monthly-report.md](../design/design-brief-quest-monthly-report.md).

## 7. Technical considerations

| Layer | Choice |
|-------|--------|
| Facts | Azure Automation `aa-kpi-automation-prod`, resource group `rg-kpi-automation-prod`, `Generate-Insights` + `Insights-Rules` (`Get-ClientMonthlyActivity`) |
| Storage | Blob `stkpiautoprod` / `autotask-reports`, then copy facts to SharePoint |
| Narrative | One of: Copilot Cowork (PRD) or Reporting Agent (signed canonical path). Not both. |
| Site | `https://prodrive365.sharepoint.com/sites/Files` |
| Dates | Meeting Tracker / LCI only, and only after decision B |
| Identity | Managed identity for blob. Least privilege for the drafter. No credentials in repo. |

Dependencies: a month KPI JSON exists; Insights-Rules is published; the drafter is allowed to read the library.

Known risks: week vs month blob pattern; resolution SLA column name (`SLA Resolution Met` vs resolution-plan fields); drafter drift; Bruce skipping review.

Rollback: `INSIGHTS_CLIENT_ENABLED = false`. Pause the drafter schedule on its own. Scorecards stay.

## 8. Success metrics

Measured on the Quest pilot, not on a portfolio average.

| Metric | Target |
|--------|--------|
| Facts completeness | 1 of 1 Quest facts file for the chosen month, required fields present |
| Number match | 6 of 6 tile fields equal `facts.json` |
| Bruce edit time | 15 minutes or less on the observed sitting |
| Time to Review | 1 working day or less after facts land |
| Send gate | 1 of 1 client sends has an approval record |
| Buyer recall | 2 non-break-fix items named by the buyer |
| LLM calls on the facts path | 0 |
| Assurix file | Issued report + facts retained for that month |

Tracking: `run-summary-insights-*.json`; SharePoint folder time and Approved marker; James’s notes from the Bruce session and the buyer conversation.

## 9. Open questions

Reply with the letter. Unanswered items stay null in the build. Do not guess.

1. **Drafter for the first Quest cycle?**  
   A. Cowork only (PRD v0.1)  
   B. Reporting Agent only (canonical path), reading `facts.json`  
   C. Cowork first, Reporting Agent if Cowork cannot read the library (recommended)

2. **Looking ahead on the first send?**  
   A. Omit until a Bruce-approved draft exists (recommended; matches the 20 Sep scope lock)  
   B. Include now, date only if Meeting Tracker has one  
   C. Include now and allow Bruce to type a date

3. **Prepared-for contact**  
   A. Autotask contact  
   B. SharePoint list  
   C. Bruce types it each month  
   D. Leave null on the first send

4. **Resolution SLA column** on the rolling-180 export  
   A. `SLA Resolution Met`  
   B. The resolution-plan field used in engineer KPIs  
   C. Not on the export; ship first-response SLA only and say so on the page

5. **When the drafter runs**  
   A. First working day, fixed schedule  
   B. When `facts.json` appears (Power Automate / SharePoint)  
   C. Bruce starts it by hand for the pilot

6. **Approved state**  
   A. Move the file to `Approved/`  
   B. SharePoint content approval  
   C. A checklist file Bruce marks in the month folder

7. **Draft file Bruce opens**  
   A. HTML (Quest sample is HTML, then PDF)  
   B. Word  
   C. PDF only

8. **Who counts as in scope after the pilot**  
   A. Autotask accounts with seats  
   B. AM-owned managed-service accounts flagged `INSIGHTS_CLIENT_ENABLED`  
   C. Do not decide until the Quest buyer test passes (recommended)

9. **Quest buyer for the recall test**  
   A. The contact in the August sample (PRD example: Sergio)  
   B. Someone else (name them)  
   C. Not named yet; block the value test, not the facts build
