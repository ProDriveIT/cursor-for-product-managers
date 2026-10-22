# Assumptions: a current private conflicts position

**Topic:** Principia conflicts register and skills matrix  
**Version:** v1  
**Date:** 2026-10-22  
**Target opportunity:** A2. I need a quiet cycle to count as a review, but I can only update a row that already exists.  
**Recommended solution under test:** One canvas Power App on Dataverse, pay-as-you-go, embedded in Teams (solutions v1, solution 1).  
**Evidence grade:** No tests have been run. Nothing in this file is a result.

## Workflow deviation

The identify-test-assumptions skill ends by running tests and moving assumptions across the map. This run stops at test design. There are no results, no map updates, and no pass or fail.

The story map below assumes solution 1 exists. That is a design walk-through, not an observation.

## Story Map Snapshot

- **Actors:** Principia employee (unnamed); Principia sponsor (unnamed); named compliance admin (not yet named); Principia tenant administrator (not yet named); person who staffs work (may not exist as a separate role); Pro Drive consultant.
- **Key steps:**
  1. Sponsor: names the admin and writes who may read skills.
  2. Tenant administrator: confirms an Azure subscription in the Principia tenant can host pay-as-you-go.
  3. Employee: opens one Teams tab.
  4. Employee: edits an existing conflict on that row, or files an attestation that can be a nil return.
  5. Employee: updates one existing skill row, only after step 1 allows it.
  6. Second employee: tries to open the first employee's conflict and gets nothing back.
  7. Admin: opens a view grouped by person and exports.
  8. Principia: receives an Azure bill for active users of one app, including a separate audit-log charge if logs accrue.

## Pre-mortem

Six months after a launch in April 2027, the register is unused or unsafe. The plausible reasons, turned into assumptions:

- The tenant could not link pay-as-you-go, and nobody had agreed Premium. (F1)
- Employees did not file, so the admin exported a blank list and blamed the app. (D1)
- Skills were locked down like conflicts, so anyone staffing work kept a spreadsheet, and the matrix label was false. (E2)
- A SharePoint list or a team-owner admin role let colleagues read conflicts. (Already rejected in solutions. F2 is the build gate that keeps it rejected.)
- Dataverse for Teams was created before 15 November 2026 and now needs the licences the design tried to avoid. (Rejected. Not retested.)
- Two apps doubled the meter and the sponsor stopped paying. (Design rule: one app.)
- Copilot Studio was purchased to replace a form, and staff still needed dropdowns. (F3 kept low importance.)
- The work was staffed as a Pro Drive product and the locked work order slipped. (V2 is a James decision, not a user test.)

## Assumption Log

| ID | Category | Assumption | Evidence | Importance | Evidence known | LoFA |
|----|----------|------------|----------|------------|----------------|------|
| D1 | Desirability | When a named admin asks, employees each save either an updated conflict or a nil attestation for that cycle. | Brief asks staff to enter conflicts and to update entries. No one has been asked. No past cycle exists in the source. | High | Weak | Yes |
| D2 | Desirability | The named admin opens a by-person view at least once in the cycle. | Brief: specified admins see all data, and reports stay possible. No admin is named. No cadence is stated. | High | Weak | No |
| U1 | Usability | An employee can change an existing conflict or skill and save onto the same row, with no second row created. | Brief requires update of existing entries. Dataverse can hold one row per interest and one row per employee per skill. No user has tried it. | High | Medium on the platform, weak on Principia staff | No |
| U2 | Usability | An employee can finish the conflict form when some fields are choices and some are text. | Brief requires both field types. The choice lists are undefined, so this is not testable until the sponsor sets them. | Medium | Weak | No |
| F1 | Feasibility | Principia's tenant administrator can link a Power Platform environment to a Principia Azure subscription and turn on pay-as-you-go. | Brief allows Azure spend under a cost or strength test. It does not say a subscription exists or that policy allows Dataverse. | High | Weak | Yes |
| F2 | Feasibility | With the app running as the signed-in user, Dataverse roles let employees read and write only their own conflict, attestation, and skill-rating rows, and let one Entra group read all rows. | Dataverse security roles support owner scope and organisation scope. This tenant has not been tested. A canvas filter on SharePoint would fail this assumption. | High | Medium | No |
| F3 | Feasibility | The people who would dictate a conflict already have Copilot Studio or Microsoft 365 Copilot. | No entitlement is in the brief. Copilot Studio is not part of Business Premium. | Low | Weak | No |
| V1 | Viability | At Principia's real pattern of active months, one app on the $10 meter costs less than Power Apps Premium at £15.40 per assigned user per month. | Both prices were checked on 22 October 2026. Headcount and active months are unknown. On the published figures the meter stays lower even when every in-scope person opens the app every month, before any currency conversion. CSP sterling can change the comparison. | High | Medium on price, weak on usage | No |
| V2 | Viability | Principia pays for this as professional services, and James keeps it off the locked product work order. | Pro Drive is the MSP. The work order (19 September 2026) names three products, and this is not one of them. No statement of work is in the brief. | High | Weak | No |
| E1 | Ethical | Conflict and attestation rows are visible only to the row owner and the named admin group. | Brief: employees see only their own conflicts. The example given is other employment. No build exists to leak or to hold. | High | Weak until a two-account test | No |
| E2 | Ethical | The sponsor either names people who may read skill rows and may not read conflict rows, or accepts that a fully private skills store is a personal record and that staffing stays outside the app. | Brief applies one privacy rule to both datasets and also calls skills a matrix. Those two sentences conflict. No resource manager is named. | High | Weak | Yes |
| E3 | Ethical | A delete by the employee on their own conflict row is acceptable because auditing keeps the history. | The recommended role includes delete. The brief does not mention delete. Audit logs record deletes only if auditing is already on. | Medium | Weak | No |

V2 stays off the leap-of-faith list because James can decide it without a user test. F2 and E1 stay off the list because the platform pattern is documented and the proof is a build gate (two test accounts, zero leaks), not a discovery unknown. V1 stays off the list because the price sources are in hand. The usage unknown changes the size of the saving. It does not flip the recommendation unless Partner Center shows a sterling meter above £15.40, or F1 fails.

F3 stays off the list because the form does the job without Copilot.

## Assumption Map Summary

Evidence runs from stronger on the left to weaker on the right. Importance runs from high at the top to low at the bottom.

**Top right, weak evidence and high importance (leap of faith, max 3):** D1, F1, E2.

**Top, high importance, not selected:** D2 (follows D1), V1 (prices known, usage unknown, comparison holds on published rates), V2 (James's commercial call), E1 and F2 (prove in a trial build, do not discover by survey).

**Middle:** U1, U2, E3.

**Bottom right:** F3. Weak evidence, and low importance, because buying Copilot Studio is already rejected.

**Notable cluster:** D1, E1, and E2 are all privacy-and-participation. They are split so each test has one question. Passing E1 in a lab does not mean employees will file (D1) or that skills may be shared (E2).

## Test Cards (per LoFA)

### D1. Employees file a conflict update or a nil return

- **Assumption:** When a named admin asks, employees each save either an updated conflict or a nil attestation for that cycle.
- **Simulation:** A one-page sheet in Word or on paper. No Power App. No demo.
- **Method:** The sponsor names 5 employees. Each person returns one sheet: either one current interest (organisation, role, and whether it is ongoing) or the sentence "I have no undeclared conflicts." The four colleagues on the list do not receive each other's sheets.
- **Audience:** Principia employees named by the sponsor. Not Pro Drive staff. Not volunteers James picks.
- **Sample and window:** 5 named employees. 5 business days to return the sheet. The window sits inside 10 business days of 22 October 2026 and closes on 5 November 2026.
- **Success criteria:** 4 of 5 named employees return a completed sheet. 0 of 5 sheets are shared with the other named employees.
- **If the sponsor will not name 5 people:** Record 0 of 5 named. That is a fail. Do not replace them with a convenience sample.
- **Pass:** Keep the attestation row in the design and continue to F1 and E2.
- **Fail (3 or fewer sheets, or 0 of 5 named):** Do not build. The gap is participation. An app will not chase people who ignore a one-page sheet.

### F1. Pay-as-you-go is allowed on Principia's Azure subscription

- **Assumption:** Principia's tenant administrator can link a Power Platform environment to a Principia Azure subscription and turn on pay-as-you-go.
- **Simulation:** A policy check. Do not create the production environment. Do not create a Dataverse for Teams environment.
- **Method:** One working session in the Power Platform admin centre and Azure. The administrator writes the three answers down.
- **Audience:** Principia tenant administrator (the role; the person is unnamed).
- **Sample and window:** 1 administrator. Closes 5 November 2026, before the 15 November 2026 Dataverse for Teams creation stop. That date is a reason to avoid the Teams environment, not a reason to rush one into existence.
- **Success criteria:** 3 of 3 confirmations, in writing: (1) an Azure subscription in this tenant can take the pay-as-you-go link, (2) policy allows a Power Platform environment with Dataverse, (3) the administrator will not require Dataverse for Teams.
- **Pass:** Keep solution 1 as the licence path. Quote only after Partner Center is re-checked.
- **Fail (any of the 3 is no, or no administrator will answer):** Stop the pay-as-you-go quote. Price Power Apps Premium (solution 2). If the answer is that Power Platform itself is refused, stop and take the custom Azure option back to James. 0 of 1 administrators identified is a fail.

### E2. Skills read list is allowed to differ, or the matrix claim is dropped

- **Assumption:** The sponsor either names people who may read skill rows and may not read conflict rows, or accepts that a fully private skills store is a personal record and that staffing stays outside the app.
- **Simulation:** A forced choice in the same sponsor session as the diagnostic assignment. No prototype.
- **Method:** The sponsor ticks one of the two statements and signs the note. They do not leave both open.
- **Audience:** The Principia sponsor (unnamed). If they name a person who staffs work, that person may sit in, and the sponsor still makes the tick.
- **Sample and window:** 1 sponsor. Same window, closing 5 November 2026.
- **Success criteria:** 1 of 1 written choices, and the choice is exactly one of these: (1) named people who staff work may read skill rows and may not read conflict rows, or (2) skill rows stay as private as conflict rows, the store is a personal record, and staffing stays outside this app.
- **Pass on (1):** Build both tables in the one app. Grant skill read to that named group. Keep conflicts to the employee and the compliance admin group.
- **Pass on (2):** Build the conflicts and attestation tables. Leave skill editing off, or ship it only as a personal record and say so in the handover.
- **Fail:** The sponsor requires a firm-wide skills matrix and requires that no one but the employee can see skill rows. Tell them plainly that the staffing outcome is unmet. Do not label the table a matrix. 0 of 1 written choices is also a fail, and skill editing stays off.

## Build gates (not leap-of-faith tests)

Run these before go-live. They do not replace D1, F1, or E2.

- **F2 and E1.** Two test accounts in a non-production environment. Account A creates one conflict and one nil attestation. Account B, a standard employee, gets 0 rows from A through the app, through search, and through export. 0 Excel exports succeed for account B. One account in the admin group sees 2 of 2 of A's rows. The app connection is the signed-in user, not a shared admin connection.
- **E3.** Ask the sponsor, before go-live, whether employees may delete a conflict. Until they answer, keep delete in the role as designed and turn auditing on first, so a delete is logged. If they forbid delete, remove it before go-live.

## Results and Decisions

- **Outcomes:** None. The sheets have not been sent. The tenant has not been checked. The sponsor has not ticked a choice.
- **Map updates:** None. D1, F1, and E2 stay in the weak-evidence, high-importance corner.
- **Decisions:** No build, no environment, and no client quote until the three tests have results. A pass on all three supports solution 1. A fail on F1 moves the licence path, not the data model. A fail on D1 stops the project. A fail on E2 stops the matrix claim and can still leave the conflicts register standing.

## Next Steps

- [ ] James books the sponsor session in the diagnostic and runs D1, F1, and E2 inside the window that closes 5 November 2026.
- [ ] Record results in a v2 of this file. Do not edit v1 into a fake pass.
- [ ] If D1 fails, close the initiative and tell the sponsor the brief is not demand.
- [ ] Share the decision note with the consultant who would build it, after the tests, not before.
