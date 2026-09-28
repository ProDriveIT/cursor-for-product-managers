# Assumptions — Quest monthly value visibility

**Topic:** Quest value visibility  
**Version:** v1  
**Date:** 2026-09-28  
**Target opportunity:** O7. Bruce shows Quest one closed month in plain English, numbers from the machine, no Autotask rebuild.  
**Leading solution:** Solution 1 in [solutions v1](../solutions/solutions-quest-value-visibility-v1.md)

## Story map snapshot

- **Actors:** Azure Automation (facts), drafter (Cowork or Reporting Agent), Bruce (vCIO), Quest buyer (unnamed), James (ops). Danny is off this map until Phase 2.
- **Key steps:**
  1. James — month KPI snapshot exists; job writes Quest `facts.json`.
  2. Drafter — writes Quest layout under `Review/` with tiles copied from facts.
  3. Bruce — opens the draft, checks tiles, edits cards, marks Approved, sends or walks the buyer through it.
  4. Quest buyer — reads or hears the month and can say what Pro Drive did.
  5. James — keeps the issued file and the facts file for the month.

Critical moments: step 1 (wrong month or wrong SLA column), step 2 (model rewrites a number), step 4 (buyer still cannot name the work).

## Assumption log

| ID | Category | Assumption | Evidence | Importance | Evidence known | LoFA |
|----|----------|------------|----------|------------|----------------|------|
| A1 | Desirability | After one Quest report, the named buyer states two pieces of work from that month that are not break-fix tickets | Company-wide claim only. No Quest quote. Bruce signed the pilot | High | Weak | Yes |
| A2 | Feasibility | Quest August 2026 `facts.json` matches a manual count on ticket count, incident count, hours, eligible helpdesk count, first-response SLA %, and resolution SLA % | PRD says a Quest August HTML/PDF sample exists. Facts reproduction is the P1 gate and is not done | High | Weak | Yes |
| A3 | Usability | Bruce finishes one Review draft in a single sitting of 15 minutes or less, changes no tile number, and leaves exec summary, What we did, and at most three cards in place | PRD target. No observed session | High | Weak | Yes |
| A4 | Viability | Bruce will complete the approve step for Quest rather than asking James to send it | Bruce signed option A on 20 Sep | High | Medium | No |
| A5 | Feasibility | The chosen drafter can read the KPI Insights library and write only under `Review/` | PRD assumption. Not demonstrated | High | Weak | No (covered by A3’s session; if the draft never appears, A3 fails) |
| A6 | Ethical | The draft names no Quest end user | PRD Quest rule. Unchecked against a real draft | High | Weak | No (inspect during A3; fail the session if a person is named) |
| A7 | Viability | Bruce’s approval is recorded before any client send | Policy in 1-pager and PRD. No tool enforces it yet | High | Medium | No |
| A8 | Feasibility | Looking-ahead dates already exist in Meeting Tracker for Quest | Not in scope for the first send under the decision note | Low for v1 | Weak | No |
| A9 | Desirability | A thin proactive month can be described without puffery and still be worth sending | PRD risk note. No sample judged by Bruce | Medium | Weak | No |

## Assumption map summary

- **LoFA (max 3):** A1, A2, A3. All three sit in weak evidence and high importance.
- **Left of those:** A4 and A7. Bruce already accepted the gate in writing. Still watch for skip-under-pressure, but do not block the facts build on another signature.
- **Notable cluster:** A5 and A6 are checked inside the A3 session. A separate Cowork licence test is wasted if facts are wrong.
- **Deprioritised:** A8 until the first approved draft exists.

## Test cards (per LoFA)

### A2 — Facts match (run this first)

- **Assumption:** Quest August 2026 facts match a manual count on six fields.
- **Simulation:** One account, one month, no drafter in the loop.
- **Method:** Filter the rolling-180 spine to Quest Fund Placement Ltd and August 2026. Count by hand or with a checked script. Diff against `facts.json`.
- **Audience:** James / Insights ops. Not the client.
- **Sample and window:** 1 client, 1 month, 6 fields, done before any Cowork prompt is trusted.
- **Success criteria:** 6 of 6 fields match (`ticketCount`, `incidentCount`, `hoursLogged`, `helpdeskSlaEligibleCount`, `firstResponseSlaMetPercent`, `resolutionSlaMetPercent`). A column-name bug counts as a pass only if the correction is written down and the regenerated file then matches 6 of 6.
- **Fail:** Any unexplained difference. Stop the pilot. Do not draft prose on bad tiles.
- **Next if pass:** Run A3. **Next if fail:** Fix the rule or kill Phase 1. Do not switch to Solution 3 hoping HTML hides the same bug.

### A3 — Bruce can review

- **Assumption:** One sitting, 15 minutes, zero tile edits, required sections present, no end-user names.
- **Simulation:** The real Review file for the month that passed A2. James watches. James does not drive the mouse.
- **Method:** Timed observation. Note each place Bruce stops, each number he challenges, each name that appears.
- **Audience:** Bruce Penson.
- **Sample and window:** 1 operator, 1 draft, 1 sitting, within 5 working days of the file landing.
- **Success criteria:** Clock stops at or under 15 minutes; tile corrections = 0; sections present = exec summary, What we did, and 3 or fewer insight cards; end-user names = 0.
- **Fail:** He corrects a figure, he cannot find the file, or he asks for a hand-built HTML. Switch the next attempt to Solution 2 (he writes the cards) or Solution 3 if the drafter never produced a file.
- **Next if pass:** Book the buyer moment for A1. **Next if fail:** Do not send.

### A1 — Buyer can name the work

- **Assumption:** The named Quest buyer states two non-break-fix items from the report.
- **Simulation:** The approved report, either sent or walked through in a live meeting. Not a hypothetical slide.
- **Method:** Within 48 hours, write down the buyer’s words. Prompt allowed: “What did we do for you this month?” No list read-back from Bruce before they answer.
- **Audience:** One named Quest economic buyer. The name is still an open question. Do not substitute Bruce’s opinion for theirs.
- **Sample and window:** 1 person, 1 report, the meeting or the week after send.
- **Success criteria:** 2 specific work items that are not break-fix, spoken or written by that buyer. “Looks professional” is not a pass.
- **Fail:** They still ask what they are paying for, or they can only cite ticket volume. Then the layout failed O7 even if the pipeline worked. Revisit the three cards before any second client.
- **Next if pass:** Phase 1 exit is met. Looking ahead and a second client become a new decision. **Next if fail:** Stay on Quest. Do not scale.

## Results and decisions

No test has been run. Map is unchanged. The 20 Sep signature supports A4 only.

## Next steps

- [ ] James picks A, B, or C on the decision note
- [ ] Name the Quest buyer for A1
- [ ] Run A2 before any narrative job
- [ ] Share this page with Bruce before the observed session
