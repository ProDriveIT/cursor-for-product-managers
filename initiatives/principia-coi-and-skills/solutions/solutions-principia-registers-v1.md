# Solutions for a current, private conflicts position

**Superseded 22 October 2026.** See `solutions-principia-registers-v2.md`. Fifty employees and a refusal of about $500 a month removes pay-as-you-go Dataverse. Most staff hold a Copilot Business licence.

**Topic:** Principia conflicts register and skills matrix  
**Version:** v1  
**Date:** 2026-10-22  
**Target opportunity:** A2. I need a quiet cycle to count as a review, but I can only update a row that already exists. Constraint A3: other employees cannot read those rows.  
**Source documents:** `opportunities/opportunities-principia-registers-v1.md`; `user-interviews/snapshots/snapshot-client-requirements-brief-2026-10-22.md`; the sponsor brief (solution box).  
**Total ideas considered:** 16, of which 10 are the sponsor's written constraints and 6 are comparison options inside that box.  
**Final selected:** 3. **Recommend:** 1, after the tests. Do not start the build this week.

## Workflow deviation

The generate-solutions skill says the human ideates first, with a minimum of a few ideas and a recommendation of 10 to 15, and the AI waits. A proper Continuous Discovery Habits ideation workshop did not happen. James was not asked for a solo list. This run did not stop.

The sponsor's brief already filled the solution box. For this run only, that box counts as the human input:

- Stay inside the company's Microsoft environment.
- Use Microsoft tools.
- Prefer the existing Microsoft 365 Business Premium licensing, and the brief names Copilot Studio.
- Azure hosting and spend is acceptable when the result is stronger, cheaper, or both, compared with extra per-user licensing (the brief cites Power Automate Premium as the example).
- Update an existing entry.
- Group data so one employee's skills are visible together.
- Employees see only their own skills or conflicts.
- Some fields are free text and some are dropdowns.
- Specified admins see all data.
- Keep the ability to produce reports and dashboards if required.

Those ten lines are constraints, not a workshop. The comparison below stays inside them. It does not open a non-Microsoft path.

## Problem Definition

**Target opportunity statement.** Each in-scope person holds a current conflict position: either an interest edited on its existing row, or an explicit nil return for this cycle. Other employees cannot read those rows. A named admin can.

**Who.** Unknown. Sponsor unnamed. Employees unnamed. Admin unnamed.

**When.** Cycle length unknown. Do not assume a year. The economics section shows a one-active-month scenario because an infrequent campaign changes the bill. It is a scenario.

**Current solutions.** Not observed.

**Impact.** Unmeasured. The harm the privacy sentence points at is colleagues reading outside employment.

**What a good solution must achieve.**

- The employee updates the same conflict row. A second interest is a new row. A second edit is not.
- Once per cycle, the employee files an attestation, and a nil return is a valid attestation.
- Row security holds when the user is not the owner. A screen filter is not the control.
- Named admins, via a group, read all conflict and attestation rows and can export. They do not have to own each row.
- The same app can hold skills later, grouped by employee, without a second app.
- Licence cost lands on Principia. Data stays in Principia's tenant.
- Reports remain possible. A dashboard is not part of the first release.
- Copilot Studio is used only when Principia already pays for Copilot Studio or Microsoft 365 Copilot.

## Ideation Process

**Sponsor box.** 22 October 2026. Ten constraints, listed above. No workshop date, no solo count beyond those ten.

**Comparison pass.** Same day, non-interactive. Options were compared only where they can live in Principia's Microsoft tenant. Categories covered: feature (data store and app type), process (how a review gets filed), interface (Teams, form, chat), and commercial (who is billed, per user assigned versus per active user).

**Not done.** No second round with James. No 15 to 20 free ideas outside the box. Diversity is limited on purpose.

## Idea Evaluation

**First filter.** Does it give A2 (a review, including nil) and A3 (colleagues cannot read the rows), using Microsoft tools in the Principia tenant, without a new Dataverse for Teams environment?

| Idea | Addresses A2 and A3 | Feasibility | Uniqueness | Evidence-based | Filter |
|------|---------------------|-------------|------------|----------------|--------|
| 1. One canvas app, Dataverse, pay-as-you-go on Principia's Azure subscription, embedded in Teams | Yes, if roles are enforced as the signed-in user | Depends on tenant policy allowing pay-as-you-go. Untested. | Ordinary Power Platform pattern. The fit is the meter plus row security. | Prices and the deprecation calendar are published. User behaviour is not. | Keep |
| 2. The same app and tables on Power Apps Premium at £15.40 per user per month, paid yearly, ex VAT | Yes, same security model | Feasible if Principia will assign a licence to every person who must open the app | Standard licence. Predictable bill. Higher published price than pay-as-you-go for this shape. | Price checked on the en-gb pricing page, 22 October 2026. Checkout can differ. | Keep |
| 3. Custom Azure web app (App Service or Static Web Apps) plus Azure SQL, Entra sign-in | Yes, if Pro Drive builds equivalent row security | Pro Drive can build it. Two registers do not justify a custom codebase and a support contract on this brief. | Bespoke. Higher ongoing support. | No Principia requirement that Power Platform is forbidden. | Keep as the fallback only |
| 4. New Dataverse for Teams environment, Private table permission | Privacy model matches A3 until the environment is upgraded or removed. A2 can be built. | Creation ends 15 November 2026. Suspension 15 September 2027. Decommission 30 October 2027 if not upgraded. Upgrade then requires Power Apps, Power Automate, or Copilot Studio licences. Team owners are System Administrators and can see all data. | Looks like the Business Premium path. It is a 24-day trap. | Microsoft Learn, important changes, checked 22 October 2026. | Reject |
| 5. SharePoint list plus a canvas app that filters to the current user | Fails A3. Anyone who can open the list can read every row. Item-level permissions are fragile under sharing links, search, and list-view thresholds, and they become recurring MSP support. | Included with Business Premium for standard connectors. | The default MSP shortcut. | The brief's privacy sentence. Conflicts are sensitive. | Reject |
| 6. Microsoft Forms | Fails the update rule and A2. Each response is a new row. Fails grouping. Fails A3 in any shared workbook destination. | Easy, and the wrong shape. | None. | Brief: update existing entries; group by employee. | Reject |
| 7. A shared Excel workbook | Fails A3. Concurrent edits are fragile. | Already in the tenant. | The likely status quo, unseen. | No row-level security. | Reject |
| 8. Copilot Studio as the system of record | Fails the job. Dropdowns and a matrix are a form. Chat can capture a sentence and upsert the same Dataverse row only when the signed-in user already has a Copilot Studio or Microsoft 365 Copilot entitlement. | Copilot Studio is not included in Business Premium. Credits are metered ($0.01 per credit on Microsoft's published Copilot pricing). | The brief named it. Naming is not a reason to buy it. | Copilot pricing page, as checked for this brief. | Reject as the product. Optional capture on idea 1 only. |
| 9. Power BI for every user, on day one | Does not address A2 or A3. It is a report surface. | Power BI is No on Business Premium and Yes on Microsoft 365 E5. Principia's plan mix is unknown. | Premature. | Service description, as cited in the decision note. | Reject for the firm. Two or three Power BI Pro licences later, if someone asks to publish. |
| 10. Two apps, one for conflicts and one for skills | Can meet the jobs, and doubles the pay-as-you-go meter because the meter is per app. | Same platform as idea 1. | Worse commercial shape. | Learn meter: $10 per active user per app per month. | Reject |
| 11. Buy new Power Apps per-app licences | Same app as idea 2, different SKU. | The fixed per-app licence is being retired for some purchasing channels from January 2026. | Do not plan on it. | Brief instruction, 22 October 2026. CSP confirmation still required. | Reject |
| 12. In-app attestation plus admin export; no automated flow in v1 | Supports A2. Security still depends on idea 1 or 2. | A flow the user starts from the app is covered by the Power Apps meter. An automated cloud flow can bill the Power Automate meter at $0.60 per run. | Process choice, not a separate product. | Learn pay-as-you-go meters, checked 22 October 2026. | Fold into idea 1. Do not add a premium flow. |
| 13. Model-driven app on the same Dataverse environment | Can meet A2 and A3 with the same roles. A second app beside the canvas app would double the meter. | Same licence as idea 1. | Native views and roles. The task's architecture is canvas. No sourced reason here to drop canvas if the app runs as the signed-in user. | Dataverse security is the boundary, not the canvas filter. | Not selected separately. One app only. Canvas stands. |
| 14. Annual email campaign from the admin, outside the app | Process around A2. Does not store the nil return. | Uses tools they already have. | Easy to fake completion if the return is a mailbox. | No cycle is defined. | Later process. The attestation row still has to exist. |
| 15. Skills edited in the same app, behind a read-list decision | Does not by itself meet A2. Protects the meter. | Blocked on who may read skills. | Avoids a second project. | Brief applies one privacy rule to both datasets. | Fold into idea 1. Skill editing stays off until that decision. |
| 16. Pro Drive-hosted app in the Pro Drive tenant | Fails "contained within the company's Microsoft environment." | Would also mix client HR-style data into the MSP tenant. | Breaks the sponsor's first criterion. | Brief, first criterion. | Reject |

## Selected Solutions (x3)

### Solution 1: One canvas app on Dataverse, pay-as-you-go, embedded in Teams

**Type:** Feature, in the client tenant.  
**Approach:** Build one canvas Power App. Dataverse environment billed to Principia's Azure subscription through Power Platform pay-as-you-go. Embed the app in Teams. One app, so a person who opens it counts once on the $10 meter.

**Description.** Four tables. Skill catalogue (admin-owned, employees read). Skill rating (one row per employee per skill, updated in place). Conflict (one row per interest, edited in place). Attestation (one row per employee per cycle, including a nil return). Dataverse auditing on Conflict and Attestation. Employee role: read, write, and delete own rows on skill rating, conflict, and attestation; read on the catalogue; no Excel export. Named admins through an Entra security group: organisation-level read on all rows; edit the catalogue; export allowed. The app runs as the signed-in user. The Dataverse role is the boundary.

Conflicts stay private to the employee and the named compliance admins. Skill ratings are either readable by named resource managers, or those managers are put in the admin group on purpose. If the sponsor insists both datasets stay fully private, the skills store is a personal record. The staffing outcome stays unmet. Do not call it a matrix in that case.

Copilot Studio, if Principia already pays for it or for Microsoft 365 Copilot, may capture a sentence and upsert the same row as the signed-in user. Chat is not the system of record. Do not buy Copilot Studio to replace the form.

**Why selected.** It is the only option that meets the privacy rule, the update rule, the nil-return gap, and the brief's cost test without a custom codebase. Business Premium still supplies Teams, Entra, and SharePoint. It does not supply full Dataverse. The Azure meter is the spend the brief allows. Published figures: $10 per active user per app per month, against £15.40 per assigned user per month on Premium. Confirm CSP sterling before quoting. A UK secondary source that says £7.60 is not the Microsoft list price.

**Delivery.** Feasibility hinges on tenant policy (test F1). User value hinges on people filing a return (test D1). Business value is a supportable register in the client tenant, billed as professional services, off the product work order. Risks: pay-as-you-go blocked; empty adoption; skills privacy left unresolved; audit log storage billed separately at $12 per GB per month when auditing is on (Learn, 22 October 2026). Database and file for this register sit inside the included 1 GB each.

**Disposition.** Research further, then build. The three tests gate the build. This is the one to recommend.

### Solution 2: The same app on Power Apps Premium

**Type:** Commercial variant of solution 1.  
**Approach:** Same canvas app, same tables, same roles, same Teams embed. Assign Power Apps Premium to every person who must open the app. Published price £15.40 per user per month, paid yearly, ex VAT, unlimited apps, Dataverse capacity included. The en-gb page also shows a £9.20 price with a 2,000-seat minimum. Do not use the 2,000-seat price in this quote.

**Description.** The security design does not change. The bill does. Premium is paid for assigned users in quiet months. Pay-as-you-go is not. The pricing page warns that marketing prices can differ from checkout. Re-check Partner Center.

**Why selected.** It is the clean fallback when the Azure link is blocked and Principia will still use Power Platform. It stays inside Microsoft tools and inside the tenant.

**Delivery.** Feasible, and dearer on the published comparison at 25, 50, and 100 people (see the decision note). User value matches solution 1. Risk: buying Premium for a campaign that runs in one month. The page lists 250 MB of Dataverse database capacity on Premium, pooled, which is a different entitlement from the pay-as-you-go 1 GB. Confirm capacity on the quote if this variant is chosen. The register is small either way.

**Disposition:** Hold. Switch to this only if pay-as-you-go fails the tenant check and the sponsor accepts assigned licences.

### Solution 3: Custom Azure web app, only if Power Platform is refused

**Type:** Feature, bespoke.  
**Approach:** App Service or Static Web Apps, Azure SQL, Entra ID sign-in, row security in the application, hosted on Principia's Azure subscription.

**Description.** Stronger security is possible, and Pro Drive can build it. A conflicts register and a skills list do not justify a custom codebase and a support contract unless Principia refuses Power Platform. Revisit only if pay-as-you-go is blocked by tenant policy and Premium is also refused.

**Why selected.** It is the third option that can meet A2 and A3. The Microsoft shortcuts in the filter table fail one or both. Putting this option third means a later request for a custom app has already been weighed.

**Delivery.** Feasible for Pro Drive engineering. Poor fit for two forms. It would compete with the locked product work order for the same people. Risk: a support contract Principia has not asked for.

**Disposition:** Do not start. Research further only after a written refusal of Power Platform.

## Recommendation

Recommend solution 1. Do not create a Dataverse for Teams environment while the 15 November 2026 door is still open. Do not buy Copilot Studio for this. Do not split conflicts and skills into two apps.

## Next Steps

1. Complete the diagnostic assignment and the three assumption tests.
2. If they pass, quote solution 1 after a Partner Center check, then build in Principia's tenant.
3. If pay-as-you-go is blocked, price solution 2.
4. If Power Platform is refused, stop and take solution 3 back to James before any design.
5. No prototype in this run. A prototype before the sponsor session would be a demo. The diagnostic forbids the demo.
