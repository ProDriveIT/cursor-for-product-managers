# Build one pay-as-you-go Power App for Principia's registers

**Superseded 22 October 2026.** Principia has 50 employees, and about $500 a month is not justified. Decision v1 replaces this note: `decision-principia-registers-v1.md`. Keep this file as the record of the Dataverse option that failed the cost test.

**Status:** v0 decision for Pro Drive consultants. Not an approved PRD. Not a quote.  
**Date:** 22 October 2026  
**Client:** Principia Advisory  
**Decision owner:** James Stock  
**Audience:** The Pro Drive consultant who would deliver this in the Principia tenant.  
**Evidence grade:** One unverified sponsor brief. No end-user interviews. No headcount. No named admin. No regulatory citation.

Build one canvas Power App in the Principia tenant. Store the data in Dataverse. Bill that environment to Principia's Azure subscription through Power Platform pay-as-you-go. Embed the single app in Teams.

Start the build only after three checks pass: the tenant can link pay-as-you-go, named employees file a conflict or a nil return on a one-page sheet, and the sponsor writes who may read skills. The tests are in `assumptions/assumptions-principia-registers-v1.md`. The window closes 5 November 2026. Re-check Partner Center, and the CSP sterling price, before you send a client number. The figures below were checked on 22 October 2026 and can move.

This is professional services in the client's tenant. It is not a Pro Drive product. It does not change the locked work order of 19 September 2026: EOS Operating Dashboard, then client monthly reports, then self-service travel.

## Why this shape

The sponsor asked for two things: a conflicts register (the example given is staff who work for other companies) and a skills matrix. Staff must update an existing entry. One employee's skills must sit together. Employees see only their own rows. Specified admins see all. Some fields are text and some are dropdowns. Reports must remain possible. The toolbox is Microsoft, Business Premium first, Copilot Studio named, and Azure allowed when it is stronger or cheaper than extra per-user licences.

Business Premium includes SharePoint, Teams, and Power Apps / Power Automate for Microsoft 365 (standard connectors and Microsoft 365 data). It does not include Power BI. A Dataverse app uses a premium connector, so a Business Premium user is counted on the pay-as-you-go meter when they open it. Copilot Studio is not an entitlement of Business Premium. A SharePoint list behind a canvas filter fails the privacy rule: anyone who can open the list can read every row. Conflicts of this kind are sensitive. The brief's example is other employment. Treat any later family-interest field the same way. Do not bet the register on list item permissions. They can be made to work at a 50-person scale, and they break under sharing links, search, and list-view thresholds. They also become a recurring support cost.

Dataverse roles are the control that matches the privacy ask. Pay-as-you-go is the Azure spend the brief allows. It is metered per active user of one app, so an infrequent review does not buy a licence for every quiet month. Premium at £15.40 per user per month, paid yearly, remains the fallback if the Azure link is blocked.

The architecture in the discovery task is accepted. Nothing sourced on 22 October 2026 rejects it. One sourced refinement changes the cost note, not the design: when auditing is on, log storage is billed at $12 per GB per month and is not covered by the included 1 GB of database and 1 GB of file. Microsoft Learn states that log storage is billed when auditing is on. Turn auditing on anyway. Budget a small log charge. The conflicts history is the point.

## Data model

One Dataverse environment. Four tables. The app writes as the signed-in user.

### Skill catalogue

Admin-owned. Every employee can read it. It is the lookup behind skill dropdowns.

| Column | Type | Notes |
|--------|------|--------|
| Skill name | Text, required | The label the employee picks |
| Category | Choice | Option list not specified. Do not invent one |
| Active | Yes/no | Inactive skills stay on old rows and drop off the dropdown |

### Skill rating

One row per employee per skill. The app updates that row (an upsert). A second save must not insert a second row. Owner is the employee.

| Column | Type | Notes |
|--------|------|--------|
| Employee | User, owner | The signed-in employee |
| Skill | Lookup to catalogue | Required |
| Level | Choice | The scale is an open question. Do not invent beginner, intermediate, expert, or a 1 to 5 score |
| Notes | Text | Free text |
| Last reviewed | Date | Set on every save |

Unique pair: employee + skill.

### Conflict

One row per interest. The employee edits that row in place. A genuinely new interest is a new row. A correction is not.

| Column | Type | Notes |
|--------|------|--------|
| Employee | User, owner | The signed-in employee |
| Type | Choice | The brief gives one example, other employment. It does not give the list. Do not invent types |
| Status | Choice | Option list not specified. An ended interest keeps its row and gains an end date. It is not a new row |
| Organisation | Text | Free text |
| Role | Text | Free text |
| Description | Text | Free text |
| Start | Date | |
| End | Date | Blank while the interest is current |

### Attestation

One row per employee per review cycle. This includes a nil return: "I have no undeclared conflicts."

The brief's update rule is right for a skill and for a conflict that already exists. It is incomplete for a register. A cycle of silence is not evidence the person reviewed it. The attestation row is a Pro Drive addition. Put it in front of the sponsor before you build it. If they reject it, drop the table and record that a blank person is an unknown, not a clear person.

| Column | Type | Notes |
|--------|------|--------|
| Employee | User, owner | The signed-in employee |
| Cycle | Text | Until the sponsor defines the cycle. Do not assume "annual" |
| Nil return | Yes/no | Yes means the person declares nothing outstanding |
| Statement | Text | The nil sentence, or a pointer to the conflict rows they confirm |
| Submitted on | Date | |

Unique pair: employee + cycle.

### Auditing

Turn on Dataverse auditing for Conflict and Attestation before the first user can write. A delete or an edit is then in the log. Skill catalogue changes can be audited too. Skill rating is lower sensitivity. Audit it if the log cost stays small. Do not audit the tenant at large "to be safe."

### How the screens group rows

Default admin views group by employee, then by skill or by conflict. They do not default to a time-ordered feed. The brief's grouping sentence is about skills. Use the same grouping for conflicts so the admin sees one person's position together.

## Permission model

Full Dataverse security roles. This is not the Dataverse for Teams permission set (Private, Collaborate, Full access, Reference). Those Teams permissions are a real match for "see my own rows," and team owners are System Administrators who can see all data. That admin boundary is wrong for a conflicts register, and new Teams environments cannot be created from 15 November 2026. Use standard Dataverse roles instead.

The canvas app runs as the signed-in user. A filter in the app is not a security boundary.

| Role | Who | Conflict, attestation, skill rating | Catalogue | Export |
|------|-----|--------------------------------------|-----------|--------|
| Employee | Each in-scope person | Read, write, and delete own rows only | Read | No |
| Compliance admin | Members of one Entra security group | Organisation-level read on all rows. They do not need to own the row | Edit | Yes |
| Resource manager | Only if the sponsor names them under check E2 | Read on skill rating rows. No read on conflict or attestation | Read | No, unless the sponsor puts them in the admin group on purpose |

Create the Entra group in the Principia tenant. The group name is an open question. Put named people in it. Do not grant organisation-level read to every Teams owner, every SharePoint site owner, or the whole firm.

"Organisation" here means the Dataverse access level Microsoft names Organization: the role can see rows it does not own. It does not mean a second company.

Delete stays in the employee role for now, because that is the role as designed, and auditing has to be on first. Confirm with the sponsor before go-live. If they want history that employees cannot erase, remove delete and keep status plus the audit log.

## The privacy rule does not fit both jobs

The brief uses one sentence for both datasets: employees see only their own skills or conflicts.

Keep conflicts private to the employee and the named compliance admins.

A skills matrix that only the employee and a compliance admin can see cannot be used to staff work. Take one of these two paths, in writing, from the sponsor:

1. Named resource managers may read skill ratings. They may not read conflicts. Or those managers are added to the admin group on purpose, knowing they will also see conflicts.
2. Skills stay as private as conflicts. The store is a personal record. Staffing stays outside this app. Do not call it a matrix in the handover.

If the sponsor demands both a firm-wide matrix and full privacy, say plainly that the staffing outcome is unmet. Leave skill editing switched off until the written choice exists. You may create the skill tables in the same environment so a later decision does not force a second app.

## What not to build

- **Microsoft Forms.** Each response is a new row. That fails update-in-place and fails grouping by employee.
- **A shared Excel workbook.** No row-level security. Concurrent edits are fragile.
- **A SharePoint list with a Power App that only filters to the current user.** The list remains readable. Item-level permissions are the wrong bet for a conflicts register.
- **A new Dataverse for Teams environment.** Creation ends 15 November 2026, 24 days after this brief. Environments that are not upgraded to Dataverse are suspended on 15 September 2027 and decommissioned on 30 October 2027. After an upgrade, users need Power Apps, Power Automate, or Copilot Studio licences. Team owners can see all data. Building one now buys the licences the path was meant to avoid.
- **A bespoke Azure web app** (App Service or Static Web Apps, plus Azure SQL). Stronger security is possible, and Pro Drive can build it. Two registers do not justify a custom codebase and a support contract unless Principia refuses Power Platform. Reopen it only if pay-as-you-go is blocked and Premium is refused.
- **A second app for skills.** The meter counts once per app. Two apps double the active-user charge.
- **New Power Apps per-app licences.** That fixed licence is being retired for some purchasing channels from January 2026. Do not plan on buying it. The pay-as-you-go meter is the usage-based path to quote.
- **Copilot Studio as the product.** Use it only if Principia already pays for Copilot Studio or for Microsoft 365 Copilot. It may capture a sentence and upsert the same Dataverse row as the signed-in user. Chat is not the system of record. Dropdowns and a matrix are a form. Do not buy Copilot Studio to replace the form. Copilot Credits on the pay-as-you-go meter are published at $0.01 per credit. There is no usage figure to turn that into a bill.
- **Power BI for the firm.** Business Premium does not include Power BI. Microsoft 365 E5 does. Do not assume Principia is on E5.
- **A premium Power Automate flow in v1.** The admin asks people to open the Teams tab. A flow the user starts inside the app is covered by the Power Apps meter. An automated cloud flow can bill $0.60 per run on the Power Automate pay-as-you-go meter. Leave that out until someone asks and the cost is accepted.
- **A Power Apps Developer Plan environment as production.** Unmanaged developer environments stop being creatable on 15 November 2026 as well, and they are not the production licence.
- **A Pro Drive-hosted copy.** The data stays in Principia's tenant.
- **A product SKU, a roadmap item, or a work-order change.** James has not reordered the three locked products.

## Licensing and cost bands

Headcount is unknown. The bands are scenarios at 25, 50, and 100 monthly active users. They are not an estimate of Principia's size. Prices exclude a currency conversion. Do not treat dollars and pounds as interchangeable. Premium on the en-gb page is ex VAT. Confirm VAT on the Azure invoice in the quote. The pricing page says marketing prices can differ from checkout.

**Pay-as-you-go, one app.** Microsoft Learn: $10 per active user per app per month. An active user is someone who opens that app at least once in the month. Repeat opens in the same month are not charged again. A person with a Power Apps per-user licence is not counted on the meter. A person with Power Apps for Microsoft 365 is not counted on an app that uses only standard connectors, and is counted when the app uses premium connectors. This app uses Dataverse, which is premium, so Business Premium users are on the meter when they open it.

**Power Apps Premium.** £15.40 per user per month, paid yearly, ex VAT, unlimited apps. The licence is assigned every month of the term, including months the person never opens the app. The £9.20 price on the same page needs a 2,000-seat minimum. Do not use it here.

**Do not quote £7.60.** A UK secondary source (Strategy365) says £7.60 per active user per app per month. That is not the Microsoft list price. CSP sterling for the $10 meter must be confirmed in Partner Center.

| In-scope people (scenario) | One app, active every month | One app, active in a single month of the year | Premium assigned for the whole year |
|----------------------------|-----------------------------|-----------------------------------------------|-------------------------------------|
| 25 | $250 per month, $3,000 per year | $250 in that month, $0 on the app meter in months with no opens | £385 per month, £4,620 per year |
| 50 | $500 per month, $6,000 per year | $500 in that month | £770 per month, £9,240 per year |
| 100 | $1,000 per month, $12,000 per year | $1,000 in that month | £1,540 per month, £18,480 per year |

The single-month column is a scenario. The brief does not say the review is annual. If it is a once-a-year conflicts campaign, most months have few active users, and pay-as-you-go drops toward zero in the quiet months. Skills edits would add active users in other months. That frequency is unknown. Premium does not drop in quiet months.

Two apps at 25 active users, both opened in the same month, cost $500.

**Capacity.** A pay-as-you-go environment includes 1 GB of Dataverse database and 1 GB of file. This register is choices, short text, users, and dates. It sits inside that 1 GB. Database above 1 GB is $48 per GB per month. No file columns are planned, so file storage should stay inside the included 1 GB. File above 1 GB is $2.40 per GB per month on the same Learn page. Audit log storage is a separate meter at $12 per GB per month, billed when auditing is on. The included 1 GB applies to database and to file. Learn's worked example prices 0.2 GB of log at $2.40 and labels the example illustrative, so the meter is fractional and a contract price can differ. A text register should stay well under 1 GB of logs for a long time. Re-check the meter before the quote.

If you fall back to Premium, the en-gb pricing page shows a different Dataverse entitlement (250 MB database on the plan comparison, pooled at tenant level). Confirm that figure on the quote. Do not copy the pay-as-you-go 1 GB onto a Premium order.

## Reporting path

Ship grouped admin views in the app, by employee, and Excel export for the admin role only. That meets "retain the ability to produce reports."

Add Power BI Pro only for the two or three people who will publish a dashboard, and only when they ask. Do not licence the firm for Power BI. Do not buy it on day one against "if required."

## Support

When the environment exists, write the environment URL, the solution name, the Entra group, and the two security roles into the Principia client records Pro Drive already keeps. Support it as a client app. Do not move the data into a Pro Drive tenant to make support easier.

Makers need a way to edit the app. Viewers need the employee role or the admin role. Do not give every employee the System Administrator role on the environment.

## Open questions

These were left open on purpose. A blank stays blank.

- Who is the sponsor, and what is their title?
- Who are the named compliance admins, and what is the Entra group called?
- How many people are in scope? How many are employees versus contractors?
- Is there a regulator, a client contract, or an internal policy that requires the register? If yes, what is the citation? If no, say no.
- Where do conflicts and skills live today, and who last updated them?
- What is the conflict type list, and what is the status list?
- What is on the skill catalogue, and what is the level scale?
- Does anyone who staffs work, other than the compliance admins, need to read skills?
- How long is a review cycle, and who chases a missing attestation?
- May an employee delete a conflict row, or only close it?
- Which Azure subscription will take the pay-as-you-go link, and does policy allow Dataverse?
- Does anyone at Principia already have Microsoft 365 Copilot or Copilot Studio?
- Has anyone asked for a dashboard, and who would publish it?
- What sterling rate, VAT treatment, and billing account should the quote use?
- Is there a signed statement of work, or is this still a brief?

## Sources

The Dataverse for Teams retirement page, the pay-as-you-go meter page, and the en-gb Power Apps pricing page were re-opened on 22 October 2026. The Power BI service-description row, the Dataverse for Teams permission model, the Copilot pricing statement, and the Strategy365 £7.60 figure are the figures supplied with this brief, also dated 22 October 2026. Re-check every item, and Partner Center, before a client quote.

- Microsoft 365 plan options, Power BI row: Business Premium is No, Microsoft 365 E5 is Yes. https://learn.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-plan-options
- Dataverse for Teams table permissions, including Private (create and see or edit own rows) and team owners as System Administrators. https://learn.microsoft.com/en-us/power-apps/teams/dataverse-for-teams-table-permissions and https://learn.microsoft.com/en-us/power-platform/admin/about-teams-environment
- Dataverse for Teams deprecation. Creation ends 15 November 2026. Suspension 15 September 2027. Decommission 30 October 2027. After upgrade, users need Power Apps, Power Automate, or Copilot Studio licences. https://learn.microsoft.com/en-us/power-platform/important-changes-coming
- Power Apps Premium, en-gb page: £15.40 per user per month, paid yearly, ex VAT. https://www.microsoft.com/en-gb/power-platform/products/power-apps/pricing
- Pay-as-you-go meters: $10 per active user per app per month; 1 GB database and 1 GB file included; database $48 per GB per month above that; log storage $12 per GB per month when auditing is on. https://learn.microsoft.com/en-us/power-platform/admin/pay-as-you-go-meters
- Copilot Studio is not an entitlement of Business Premium. Pay-as-you-go Copilot Credits are published at $0.01 per credit. https://www.microsoft.com/en-us/copilot/pricing/business
- Secondary sterling figure, not a Microsoft list price: https://www.strategy365.co.uk/microsoft-retires-the-power-apps-per-app-plan/

## Workflow deviation

This note was written in a non-interactive discovery run, in the same pass as the diagnostic, the snapshot, and the untested assumptions. The create-prd skill was not used. The sponsor did not review it. A consultant can use it to prepare the session and, after the three checks, to build. They cannot use it as evidence that Principia has asked for a nil return or agreed a price.
