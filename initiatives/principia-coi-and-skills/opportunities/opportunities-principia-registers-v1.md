# Opportunities: Principia conflicts register and skills matrix

**Topic:** Principia conflicts of interest and skills records  
**Version:** v1  
**Date:** 2026-10-22  
**Source documents:** `user-interviews/snapshots/snapshot-client-requirements-brief-2026-10-22.md` only. Synthesis was skipped. See `user-interviews/synthesis/synthesis-skipped-2026-10-22.md`.  
**Context sources:** `company-level-context/prodrive-context.md` sections 1 and 4; `product-vision-and-strategy/product-work-order.md`; `product-vision-and-strategy/product-map.md`; `okrs/README.md` (placeholder, no current OKRs).  
**Total opportunities:** 8 leaves under 2 parents.  
**Evidence grade:** Unverified. One sponsor brief. Zero end users.

## Quality bar this file does not meet

The create-opportunities skill asks for two or more participants, or strong behavioural evidence, behind each opportunity. This file has neither. Every row traces to one written brief. Use the tree to keep the two jobs apart. The research quality bar is unmet. Both user reviews were skipped. The deviation is recorded below.

## Workflow deviation

- **Reviews.** Steps 4 and 6 say to pause for James to merge, split, delete, or rename. This run cannot pause. The candidate table and the sibling winners are provisional. James can still change them. No review notes were invented.
- **Minimum input.** The skill asks for 3 to 5 snapshots, or one synthesis. The discovery rule for fewer than three snapshots is to go straight from the snapshot to opportunities. That is what this file does.
- **Metrics.** The analyze-metrics skill was not run. There is no funnel, cohort, event export, headcount, or baseline. The Opportunity Sizing lens is a gap. Later cost bands at 25, 50, and 100 monthly active users are price scenarios, not a measure of Principia.

## Outcome

Principia can produce, from rows each employee keeps current, a conflicts position for every in-scope person and a skills view grouped by person.

The outcome has no metric. Headcount, cycle length, and "produce for whom" are unstated. It is the sponsor's implied result, not a target James has accepted.

Copilot Studio, Business Premium, and Azure are solutions. They are not in this tree. The brief named them. They are handled in the solutions file.

## Opportunity Solution Tree (Snapshot)

```text
Outcome: Produce a current conflicts position and a person-grouped skills view
├── A. Keep a conflict position current and private
│   ├── A1. Edit an interest that already exists, on the same row
│   ├── A2. Record a review this cycle, including when there is nothing to declare  ← target
│   ├── A3. Stop every other employee reading conflict rows
│   └── A4. Let one named admin see every person's current position, grouped by person
└── B. Keep skills current and usable when staffing work
    ├── B1. Change the level and notes on a skill the employee already has
    ├── B2. Show all of one employee's skills together
    ├── B3. Use a shared list for common skills, and free text where the list does not fit
    └── B4. Let the person who staffs work read skills across people
```

A3 is also a constraint on every conflicts solution. A solution that misses A3 is out, even if it hits A2.

## Candidate Opportunities (Pre-Review)

| ID | Parent | Statement | Evidence count | Quotes | Notes |
|----|--------|-----------|----------------|--------|-------|
| A1 | A | I need to correct an interest I already entered, but a new submission leaves the old row in place as well. | 1 brief, 0 interviews | "Staff must be able to update existing entries, rather than add additional" | Brief text, not speech. Applies to conflicts and to skills. |
| A2 | A | I need a quiet cycle to count as a review, but I can only update a row that already exists. | 1 brief, plus a Pro Drive judgment | The brief has no nil-return line. The update sentence is the whole rule. | Analyst inference. The sponsor did not ask for this. Mark it as such. |
| A3 | A | I need other staff blocked from my outside interests, but a shared list is readable by anyone who can open it. | 1 brief, 0 interviews | "Employees should only be able to see their own skills or conflicts" | The example in the brief is "when they work for other companies." Family interests are not in the brief. |
| A4 | A | I need a named admin to see each person's current conflicts, grouped by person, when they have to produce them. | 1 brief, 0 interviews | "Specified admins should be able to see all data" and the grouping sentence, which is written about skills. | Admins are unnamed. No report is required yet. "dashboards if required." |
| B1 | B | I need to change my level on a skill I already have, but adding another row makes the history the record. | 1 brief, 0 interviews | Same update sentence as A1. | No skill scale is defined. Do not invent one. |
| B2 | B | I need all of one person's skills in one place, but a time-ordered list hides them. | 1 brief, 0 interviews | "you should be able to see all the skills of one employee rather than a random time-ordered list" | This is the clearest skills sentence in the brief. |
| B3 | B | I need a fixed list for common skills and a place to type the rest. | 1 brief, 0 interviews | "Some fields will be free text and some will be drop down" | The lists themselves are not specified. |
| B4 | B | I need the person who staffs work to read skills across the firm, but the brief gives that read to specified admins only and applies the conflicts privacy rule to skills. | 1 brief, 0 interviews | "update a skills matrix" and "Employees should only be able to see their own skills or conflicts" | The word "matrix" is the sponsor's. The staffing need is inferred from that word. It may be wrong. |

## Review Notes #1

Skipped. Non-interactive run. No merge, split, delete, or rename decision from James. Deviation from create-opportunities Step 4.

Provisional structure kept: two parents, because the failure pattern is two jobs bundled. A2 kept separate from A1 so the nil return is visible as a judgment, not smuggled in as a client quote.

## Assessment (Sibling Comparisons)

### Sibling set A: A1, A2, A3, A4

**Sizing.** Unknown. No headcount, no count of past interests, no cycle. A conflicts review is often infrequent. One missing interest can matter more than a weekly edit. That is a reason to be careful, not a size. No number is available. Analyze-metrics had nothing to read.

**Market.** For this client delivery, the status quo competitor is whatever Principia uses now, and that artifact was not shown. A private register an admin can produce is table stakes for the job the sponsor described. It is not a Pro Drive product differentiator. Product map goal B (sell services) only fits if this is a billed statement of work. It is not a new SKU, and it is not on the product map.

**Company.** Locked work order, James Stock, 19 September 2026: EOS Operating Dashboard, then client monthly reports, then self-service travel. Context section 4. This tree does not take product capacity. A small professional-services job in the Principia tenant can sit beside that order. It does not jump it. OKRs: none agreed, so no objective is claimed.

**Customer.** No end user. Satisfaction with the current workaround is unknown. The sponsor wrote the privacy sentence and the update sentence. The sponsor did not write the nil return. A2 is the leaf most likely to be wrong, and the leaf that most changes the data model if it is right.

**Discussion.** A1 and A3 are explicit in the brief. A4 is explicit, with unnamed admins. A2 is the incomplete part of "update an existing entry" when the dataset is a register. Exploring A1 alone ships a log that looks finished when people who have no conflict have never been asked. Exploring A3 alone is a security control with no record of review.

**Winner.** A2, with A3 as a constraint every solution must meet. Reversible. If the sponsor says a silent year is acceptable, drop A2 and target A1.

### Sibling set B: B1, B2, B3, B4

**Sizing.** Unknown, same gap. Skills may change more often than conflicts. That is a hypothesis. It is not a count.

**Market.** A person-grouped skills list is common in consultancies and is often a spreadsheet. The brief gives no reason Principia's list is different. Not a differentiator.

**Company.** Same work-order constraint as set A. Building a second app for skills would double a per-app meter later. That commercial point belongs in solutions. It does not make B more important than A.

**Customer.** The grouping sentence (B2) is the strongest skills line in the brief. The privacy sentence fights the usual reason to keep a matrix (B4). No resource manager is named. B4 may be a misread of the word "matrix."

**Discussion.** B1, B2, and B3 can be met inside one app once someone defines the catalogue and the level scale. B4 decides whether that app is a matrix or a personal record. Until B4 is answered, a skills build can satisfy the brief and still miss staffing, or it can serve staffing and breach the privacy sentence.

**Winner.** B4 is the skills leaf to resolve first, and it is second to A2. Do not explore B4 by building. Resolve it in the sponsor session. B2 remains the requirement to meet if skills are built.

### Parent set: A against B

**Sizing.** Cannot separate them by volume. Both are uncounted.

**Market.** Conflicts carry the harm the brief's privacy sentence is trying to prevent (other employment visible to colleagues). Skills carry the operational use. The brief does not say which harm has already happened.

**Company.** One professional-services engagement can hold both, later, in one app. Discovery order still has to pick a job. Company context does not prefer a skills product. Pro Drive's map does not include either job.

**Customer.** The sponsor listed conflicts first and skills second. That order is weak evidence. The privacy sentence is strong evidence that conflicts are the sensitive set. Zero sessions means the customer factor cannot crown a winner. The tie-break is risk: a leaked conflict is worse than a delayed skills list, and the brief already treats conflicts as private.

**Winner.** Parent A. Explore A2 first.

## Review Notes #2

Skipped. Non-interactive run. No confirmation of the sibling winners. Deviation from create-opportunities Step 6.

## Proposed Target Opportunity

**Target:** A2. I need a quiet cycle to count as a review, but I can only update a row that already exists.

**Constraint that travels with it:** A3. Other employees cannot read conflict rows. Named admins can (A4).

**Why this leaf, and why first.** The update rule in the brief is the right rule for an existing conflict and the right rule for a skill. It is the wrong whole design for a register. If the only write is "edit what is already there," a person who has never had a conflict leaves no evidence they looked. Solutioning starts there because it adds a row type the brief did not name (one attestation per person per cycle, including a nil return) and because it forces the privacy design before any skills screen. Skills (parent B) stay in the same future app so a second app does not double the meter, and skill editing stays off until the sponsor answers B4.

**What this target is not.** It is not a client request. It is a reversible Pro Drive judgment on an incomplete brief. Evidence that would move the target back to A1: the sponsor says, in writing, that non-responses are chased outside the tool and a blank register is acceptable. Evidence that would move the target to B4: the working session shows a current staffing decision blocked by the skills list, and no equivalent conflicts pressure.

**Supporting evidence.** One brief. The update sentence. The privacy sentence. The worked example "when they work for other companies." No quote supports the nil return. Say that in front of the sponsor.

**Next steps.**

1. Run the assignment in `diagnostic-principia-registers.md` before any build.
2. Run the three tests in `assumptions/assumptions-principia-registers-v1.md`.
3. Solution options for A2 are in `solutions/solutions-principia-registers-v1.md`, written in this same run because the task required them. They are not a signal that the reviews happened.
