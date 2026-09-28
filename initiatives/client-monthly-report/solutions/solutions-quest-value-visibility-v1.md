# Solutions for Quest monthly value visibility

**Topic:** Quest value visibility  
**Version:** v1  
**Date:** 2026-09-28  
**Target opportunity:** O7. Bruce can show Quest one closed month in plain English, with machine-counted numbers, without rebuilding it from Autotask.  
**Source documents:** [opportunities v1](../opportunities/opportunities-quest-value-visibility-v1.md), [1-pager](../prd/1-pager-client-monthly-report.md), PRD v0.1, [decision note](../decision-prd-v0.1-spine.md)  
**Human ideas on record:** 2 sessions (below). AI did not invent the leading option.  
**Total ideas:** 12  
**Final selected:** 3

## Problem definition

- **Target:** O7, as above.
- **Who:** Bruce (vCIO, Quest operator). Reader: Quest economic buyer (name still open; PRD uses Sergio as an example). Ops: James. TAM context: Danny, not a Phase 1 author.
- **When:** The first working window after a calendar month closes.
- **Current solutions:** Autotask screens; branded Insights `client-pack-*.html` (WIP-027, not yet confirmed for a Quest month); archived value-add PowerShell (dead).
- **Impact:** Work order #2 stays open. Low reactive volume keeps reading as low service until one external report exists.
- **Success criteria:** One Quest month. Tiles match the facts file on every figure. Bruce approves. A named buyer, after send or a walkthrough, states two pieces of non-break-fix work from that month. No second client in this pass.

## Ideation process

### Individual sessions

| Date | Who | Count | What they committed to paper |
|------|-----|-------|------------------------------|
| 2026-09-19 to 20 | James, then Bruce | 4 options, A selected | Reporting Agent Phase 1 on the Insights HTML pack. Bruce approves. Phase 2 narrative list and meeting footer wait. Options B (interview the buyer first), C (defer), D (revive the archived generator) were rejected. |
| 2026-09-28 | PRD v0.1 author (ops / Insights, WIP-027) | 1 pipeline | Azure writes `facts.json`. Copilot Cowork drafts the Quest layout. Bruce reviews. Looking ahead reads Meeting Tracker in the first version. |

A fresh solo list was not requested before this file. Those two documents are the human rounds. Stopping to ask for ten more ideas would ignore a signed choice and a same-week spec.

### Collaborative additions (28 Sep)

Added to force categories the two human docs do not cover:

1. Pre-filled skeleton only. Azure writes tiles into the Quest HTML. Bruce types the three insight cards. No model.
2. Azure OpenAI inside Automation for the prose (PRD A4).
3. Live SLA link in a portal and no monthly narrative (PRD A3).
4. Quarterly pack only. Skip the monthly send.
5. Bruce records a short spoken walkthrough. No PDF.
6. One email: three numbers and one paragraph. No Quest layout.
7. Vendor PDF stitch (Huntress, Mimecast, Inforcer) into the same file.
8. New SharePoint list for TAM dates.

**Total ideas generated:** 12 (4 historical options + 1 PRD pipeline + 7 additions). Option D and ideas 7–8 fail the signed constraints and drop before scoring.

## Idea evaluation

Initial filter: must let Bruce show Quest one month of real work with trustworthy numbers, on Azure + Microsoft 365 + Copilot, without a new date store and without auto-send.

| Idea | Addresses O7 | Feasibility | Uniqueness | Evidence-based |
|------|--------------|-------------|------------|----------------|
| Reporting Agent on `client-pack` HTML (signed A) | Yes | Pack file for Quest is unproven | Low; already the canonical path | Bruce signed it. Pack existence untested |
| `facts.json` + one drafter + Quest layout (PRD, drafter undecided) | Yes | Facts fields extend `Get-ClientMonthlyActivity`. Cowork SharePoint read is unproven | Medium; number lock is tighter than HTML-in, prose-out | PRD sample claims Quest August HTML/PDF. `facts.json` not reproduced |
| Skeleton, Bruce writes cards, no model | Partial; slower, but numbers stay honest | High if facts exist | Low | Matches “AM edits judgment, not math” if the model is the risky part |
| Azure OpenAI in the runbook | Yes, with more number-drift risk | Extra spend the PRD deprioritises | Low | Fallback only |
| Portal SLA, no narrative | No; does not answer “what did you do?” | Unknown | Low | PRD lists it as post-MVP |
| Quarterly only | Weak; the pain is monthly perception | High | Low | Conflicts with work order #2 |
| Spoken walkthrough, no page | Partial; nothing to retain for Assurix | High | Medium | No demand evidence |
| Three-number email | Partial; too thin for preventative themes | High | Low | PRD design says one Quest layout |

## Selected solutions (3)

### Solution 1: Facts file, one drafter, Quest layout, Bruce gate

**Type:** Process + feature  
**Approach:** Build now for the facts contract. Prototype the drafter on one client.  
**Description:** Azure emits `facts.json` for Quest for one closed month. One drafter (Cowork if it can read the library; otherwise the Reporting Agent) writes the Quest sections into `Review/`. Tiles are copied, not recomputed. Bruce approves, then a human sends.  
**Key features:** Calendar-month filter, locked tiles, title inventory for the drafter, PD Client Wide titles, Review-only output, approval marker before send.  
**User experience:** Bruce opens one folder, checks tiles, edits cards, sends.  
**Why selected:** This is PRD v0.1 with the signed scope fence from the [decision note](../decision-prd-v0.1-spine.md). It serves O7 and keeps a single number source.  
**Build now / test / research:** Build the facts path now. Test the drafter on Quest only.  
**Risks:** Week-pattern vs month-pattern; resolution SLA column name; Cowork inventing a percent; Bruce skipping review. Looking ahead stays out of this solution until the first approved draft exists.

### Solution 2: Facts-filled skeleton, Bruce writes the prose

**Type:** Process  
**Approach:** Prototype and test if Solution 1’s drafter changes a tile or cannot read SharePoint.  
**Description:** The same `facts.json` fills the Quest tiles and leaves insight cards blank. Bruce writes up to three cards from the title list. No Copilot call on the pilot month.  
**Why selected:** It still hits O7 if the model is the thing that fails. It is the honest fallback already named in the PRD (“facts + AM-written prose”).  
**Risks:** Bruce’s edit time blows past 15 minutes and the pilot feels like the manual pack it replaced.

### Solution 3: Stay on the signed Reporting Agent and HTML pack

**Type:** Process  
**Approach:** Research further only if Quest `facts.json` cannot be produced.  
**Description:** Confirm `client-pack-*.html` for Quest for one `YYYY-MM`. Bruce runs the Reporting Agent. Numbers are whatever the pack already rendered.  
**Why selected:** It is the path Bruce already approved. It is the fallback if the facts contract slips, not a second build to run in parallel.  
**Risks:** The pack HTML is a weaker lock than `facts.json` if the agent paraphrases figures. The 1-pager already says to stop if the pack cannot be produced.

## Next steps

1. James marks A, B, or C on the [decision note](../decision-prd-v0.1-spine.md).
2. Run the three tests in [assumptions v1](../assumptions/assumptions-quest-value-visibility-v1.md). Facts match is the kill switch.
3. Parent tasks are in [tasks](../tasks/tasks-monthly-client-service-report.md). Sub-tasks wait for “Go”.
