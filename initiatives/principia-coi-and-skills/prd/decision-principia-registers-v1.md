# Two SharePoint lists, then a Copilot agent on licences Principia already has

**Superseded 22 October 2026.** The lists stay. The "no canvas app" line does not. Staff get a Power Apps form in front of the lists. See `decision-principia-registers-v2.md`.

**Status:** v1 decision. Replaces `decision-principia-registers-v0.md`. Not an approved PRD. Not a quote.  
**Date:** 22 October 2026  
**Client:** Principia Advisory, 50 employees  
**Decision owner:** James Stock  
**New facts:** About $500 a month is not justified. Most staff hold a Copilot Business licence.

Build two Microsoft Lists in Principia's tenant, on a site their admins own. One list for skills. One list for conflicts. Staff open the list and edit the row that is already there. A short Power Automate flow, using the SharePoint connector included with Business Premium, gives each new row to that employee and to the named admins, and takes it away from everyone else. Admins use a view grouped by person and can export to Excel.

Add one Copilot Studio agent in Teams for the staff who already have Microsoft 365 Copilot Business. The agent updates those same rows as the signed-in person. The lists are the record. The agent is a second door, on a licence Principia already pays for.

No Dataverse. No Azure meter. No Power Apps Premium. No canvas app. No second environment.

This stays professional services in the client tenant. It does not move the locked work order.

## Why the earlier recommendation is withdrawn

Pay-as-you-go Dataverse is $10 per person who opens the app in a month. At 50 employees that is $500 in any month they use it. That fails the budget James set on 22 October 2026. Power Apps Premium at £15.40 per user per month is £770 a month for the same 50, and it is dearer still. Both were the right security product for a firm that will pay. This firm will not.

Dataverse for Teams stays withdrawn as well. New environments cannot be created from 15 November 2026.

## What to build

One SharePoint site. Two lists. One flow. One Teams tab for the lists. One agent, published only to people who hold Copilot Business.

### Skills

One row per employee per skill. A later change edits that row.

| Column | Type | Who sets it |
|--------|------|-------------|
| Employee | Person | The flow writes the person who created the row. Staff do not pick a colleague. |
| Skill | Choice | Admins edit the choice list when a skill is added. |
| Level | Choice | The sponsor supplies the scale before go-live. Leave the column empty of invented levels. |
| Notes | Multiple lines of text | The employee |
| Skill key | Single line of text, unique | The flow writes email plus skill. A second row for the same pair fails, and the flow removes it. |

### Conflicts

One row per interest. A correction edits that row. A new interest is a new row.

| Column | Type | Notes |
|--------|------|-------|
| Employee | Person | Set by the flow from the creator, as on Skills |
| Type | Choice | Include one value, "Nothing to declare", so a quiet cycle is a row they update |
| Organisation | Single line of text | Blank on a nil row |
| Role | Single line of text | Blank on a nil row |
| Detail | Multiple lines of text | |
| Status | Choice | Current, Ended |
| Start | Date | |
| End | Date | Blank while current |
| Last reviewed | Date | The employee sets this when they confirm the row |

Each person keeps a single "Nothing to declare" row and updates Last reviewed. That is the nil return. It does not need its own list.

### Permissions

Named admins are the site owners. They see every row.

Staff can add a row. They cannot read the list as a whole. When a row is created, the flow stops sharing it and grants edit to the creator and read to the owners. Turn off sharing of individual items so a member cannot invite a colleague.

The SharePoint list setting "read items that were created by the user" is a filter for people with ordinary rights. It is not the control. The flow's grant and stop-sharing steps are the control, because search follows real item permissions.

Fifty people stay well inside SharePoint's guidance of 5,000 unique permission scopes on a list. A skills list at 20 skills each is about 1,000 rows. Revisit the design if one list approaches 4,000 rows with their own permissions.

### Copilot

Confirm the SKU in the tenant before the agent is published. "Copilot Business" here means the Microsoft 365 Copilot Business add-on. On Microsoft's pricing page that add-on includes agent creation in Copilot Studio for the Copilot Chat and Standard harness. Microsoft's Copilot Studio licensing guide includes employee-facing agent use, and the SharePoint tools those agents call, when the person using the agent has a Microsoft 365 Copilot user licence and the agent runs as that person. Microsoft caps that at a fair-use limit it can change. Publishing is to Teams, SharePoint, and Microsoft 365 Copilot, which is the channel those rights cover.

Copilot Chat that comes with Business Premium is a different, smaller right. Custom agents there are metered. Staff without Copilot Business use the list. Do not hand them the agent.

The agent's SharePoint connection runs as the signed-in user. A shared connection owned by an admin would let any caller read every conflict. That is a build rule, not a later hardening task.

The agent can say "set my Excel level to the next choice" or "I have started working for another firm." It reads and updates the lists. It does not become a second database.

### Reporting

The admin view groups by Employee. Export to Excel is there for the owners. An owner who has Copilot Business can ask Copilot in Excel about that export. Power BI stays off the first release. Business Premium does not include it, and nobody has asked for a dashboard.

## What this leaves out

- A canvas Power App. The list form already edits a row.
- A skill catalogue list. Choice columns are enough until the dropdown is too long to use.
- A fourth table for attestations.
- Dataverse, pay-as-you-go, Premium, and a custom Azure app.
- An agent for the staff who do not have Copilot Business.
- Power BI.

## Privacy on skills

The brief asks for the same privacy on skills and on conflicts. Build it that way. If someone who staffs work needs to read skills, add that person, or one SharePoint group, to the grant step on the Skills list only. Do that when they ask. Do not hold the lists for a workshop.

## Check before staff are invited

Two test accounts. Account A creates one skill and one conflict. Account B sees none of A's rows in the list, in search, and in the agent. An owner sees both of A's rows, grouped under A. The duplicate skill key rejects a second row for the same skill.

Then ask five employees to enter one skill and either one interest or a "Nothing to declare" row. If those five will not do it, stop before you announce it to all 50. An empty list is a cheap failure. A Dataverse app would have been an expensive one.

## Sources checked 22 October 2026

- Pay-as-you-go meter, $10 per active user per app per month: https://learn.microsoft.com/en-us/power-platform/admin/pay-as-you-go-meters
- Power Apps Premium, £15.40 per user per month: https://www.microsoft.com/en-gb/power-platform/products/power-apps/pricing
- Copilot Business add-on and included Copilot Studio for internal agents: https://www.microsoft.com/en-us/copilot/pricing/business
- Copilot Studio rights with a Microsoft 365 Copilot user licence, including tools the agent calls, fair use, user's own identity: https://www.microsoft.com/licensing/guidance/Microsoft-Copilot-Studio
- SharePoint connector is standard, including grant access on an item: https://learn.microsoft.com/en-us/connectors/sharepoint/
- Grant and stop sharing require a list owner connection: https://learn.microsoft.com/en-us/sharepoint/dev/business-apps/power-automate/guidance/manage-list-item-file-permissions
- Dataverse for Teams creation ends 15 November 2026: https://learn.microsoft.com/en-us/power-platform/important-changes-coming

Confirm the Copilot Business SKU and the fair-use position in Partner Center before telling Principia the agent is free to run.
