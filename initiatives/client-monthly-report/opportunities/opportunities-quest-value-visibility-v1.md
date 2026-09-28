# Opportunities — Quest monthly value visibility

**Topic:** Quest value visibility  
**Version:** v1  
**Date:** 2026-09-28  
**Source documents:** [1-pager](../prd/1-pager-client-monthly-report.md) (approved A, 20 Sep 2026); [PRD v0.1](file:///C:/Github-Repos/10%20Projects/2026-01%20reporting-kpi-automation/Documentation/PRD-Monthly-Client-Service-Report.md); [prior art](../prior-art-github-repos.md); [product map](../../../company-level-context/product-vision-and-strategy/product-map.md)  
**Context sources:** [prodrive-context](../../../company-level-context/prodrive-context.md), [work order](../../../company-level-context/product-vision-and-strategy/product-work-order.md) (#2 = one Quest HTML)  
**Interview snapshots:** none  
**Total opportunities:** 7

Evidence limit: there is no Quest buyer quote and no interview snapshot. Bruce’s signature on option A is an operator decision, not a buyer demand quote. Treat every leaf as reversible.

## Opportunity solution tree (snapshot)

Outcome: Quest’s economic buyer can name the proactive, initiative, and alignment work Pro Drive did in one calendar month.

- Parent: Paid-for work stays invisible when tickets drop
  - Child: Preventative and alignment work never enters the client conversation
    - **Leaf (target):** Bruce can show Quest one month of that work in plain English without rebuilding it from Autotask
  - Child: A ticket list makes the month look like noise
- Parent: The monthly pack is too expensive to repeat
  - Child: Bruce rebuilds hours, SLA, and titles from Autotask screens
  - Child: A model that recounts tickets will publish a wrong SLA or hour total
- Parent: The wider-estate story is scattered
  - Child: PD Client Wide themes and Pro Drive statements sit in chat and docs, off the pack
- Parent (constraint, not the target): Assurix expects a retained service report
  - Child: T130–T133 / T151 need metrics, insight, and a human review on file

## Candidate opportunities (pre-review)

| ID | Parent | Statement | Evidence count | Quotes | Notes |
|----|--------|-----------|----------------|--------|-------|
| O1 | Invisible work | I want Quest to see the preventative work they paid for, but that work never shows up in the monthly conversation | 0 interviews; 1 signed 1-pager; company-context claim that reactive volume has fallen | No Quest quote. 1-pager: clients ask what they are paying for | Demand is company-wide, not Quest-specific |
| O2 | Invisible work | I want a short account of the month, but a raw ticket dump hides the point | 0 interviews; PRD non-goal | PRD: “not a ticket dump” | Reconstructed from a feature complaint |
| O3 | Pack cost | I want to send a credible month, but I have to rebuild hours and SLA from Autotask every time | 0 interviews; PRD persona P1 | PRD persona, not a transcript: “Digging Autotask for hours/SLA” | Bruce has not been timed |
| O4 | Pack cost | I need the numbers on the page to match the system of record, but a model that counts tickets will invent them | Prior-art rule + PRD risk table | Signed rule: agents never invent metrics | Engineering constraint wearing a customer hat |
| O5 | Estate story | I want Quest to see estate-wide improvements that affected them, but those titles live outside the client pack | PRD F4 / US-4; companion doc names `PD Client Wide work` | No buyer quote | Real data exists; desire is inferred |
| O6 | Compliance | I need a retained report with metrics and a review trail for Assurix | PRD names T130–T133, T151 | No audit finding attached | Viability constraint. Do not build for the auditor first |
| O7 | Invisible work / target leaf | When the month is quiet, Bruce wants the Quest buyer to see what Pro Drive did, but rebuilding the story from Autotask makes a sendable pack too slow | O1 + O3 | Same thin evidence as O1 and O3 | This is the leaf to explore |

## Review notes #1

Pending James. Written in one pass on 28 Sep 2026 because the kickoff instruction was to run the process from PRD v0.1, and the opportunity folders were empty.

Default if you do not edit: keep O1–O7, do not merge O4 into O1 (number trust is a separate failure), and do not promote O6 to the target.

## Assessment (sibling comparisons)

### Set A — why the buyer is stuck (O1, O2)

- **Sizing:** One named account (Quest). Frequency is monthly. No count of how often the buyer has asked the question.
- **Market:** A monthly service narrative is table stakes for a managed standard (PRD cites Assurix). The differentiator is showing silent preventative work, not sending a scorecard.
- **Company:** Product map scores Monthly Report High on goal B (retain and expand) and says it does not reduce RTEM. Work order #2 is this pilot. Fits.
- **Customer:** Importance is high if the renewal conversation is real. Satisfaction with alternatives is unknown. The stopped value-add generator is not a customer alternative; it is an internal false start.
- **Winner:** O1. O2 is how a bad report fails O1.

### Set B — why Bruce does not send one (O3, O4)

- **Sizing:** One operator (Bruce) for the pilot, then other accounts only after the value test.
- **Market:** Speed of production is internal. Trust in numbers is customer-facing.
- **Company:** Hosting stays Azure + Microsoft 365 + Copilot. Reuse Insights. Do not rebuild KPI math.
- **Customer:** Bruce signed option A, so he has accepted the job. He has not completed a cycle, so the pain is still a persona.
- **Winner:** O3 is the operator pain. O4 is a solution constraint on whatever drafts the page. Neither replaces O1.

### Set C — story inputs (O5, O6)

- **Sizing:** O5 is one shared account (`PD Client Wide work`) plus statements. O6 is an audit file, not a buyer job.
- **Company:** O6 supports evidence retention. It does not create goal B on its own.
- **Winner:** O5 can ride along inside the Quest page. O6 is a non-functional requirement, not the opportunity.

## Review notes #2

Pending James. Tentative winners above stand until you mark a different leaf.

## Proposed target opportunity

**O7.** Bruce can show Quest one closed month of preventative, helpdesk, and alignment work in plain English, with machine-counted numbers, without rebuilding the month from Autotask.

**Rationale:** That leaf is the signed outcome (buyer can name the work) plus the operator barrier (rebuild cost). O4 and O6 constrain the build. They are not the thing Quest buys.

**Supporting evidence:** Thin. Bruce approved the pilot. No Quest buyer has said this on the record. The value test in the assumptions file is what makes O7 real or kills it.

**Next steps:** Solutions v1 (written alongside this file). Then the three leap-of-faith tests. Do not scale past Quest until the buyer test has a written result.
