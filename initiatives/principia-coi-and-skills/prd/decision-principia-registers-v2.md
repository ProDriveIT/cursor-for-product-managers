# A Power Apps form in front of two SharePoint lists

**Status:** v2 decision. Replaces the "no canvas app" line in `decision-principia-registers-v1.md`. Not an approved PRD. Not a quote.  
**Date:** 22 October 2026  
**Client:** Principia Advisory, 50 employees  
**Decision owner:** James Stock

Staff open one form in Teams. The form shows the skills and conflicts they already have, and Save writes back to the same row. The store is still two SharePoint lists. The permission flow is unchanged. Copilot remains a second door for people who already have Copilot Business.

No Dataverse. No Azure meter. No Power Apps Premium.

## Why the form was missing, and why it belongs

v1 left staff in the list grid, to keep the build to lists and a flow. That cut the part people touch. A grid invites a new row. The brief asks them to update the row they already have, and to see one person's skills together.

The $500 bill was a Dataverse app. A canvas app whose only connection is SharePoint is a standard app. Business Premium includes Power Apps for that. Microsoft's licence designation for an app that uses only standard connectors is Standard, and the end user needs the Power Apps for Microsoft 365 right they already have. SharePoint is a standard connector.

Before anyone is invited, open the app details and read the licence designation. It must say Standard. A premium connector, a custom connector, Dataverse, or an on-premises gateway flips it to Premium, and that is the $10 meter again at 50 people. Leave the environment out of Managed Environments. Microsoft's enforcement pass from February 2027 is aimed at managed environments, model-driven apps, and Dynamics-licensed apps used outside that Dynamics environment. A standard SharePoint form stays on the Business Premium right. If the designation comes back Premium, remove whatever caused it and republish. Do not buy Premium to save the form.

## What staff see

One screen in a Teams tab. Two groups on that screen.

**Your skills.** Each skill they already have is a row with the level dropdown and the notes field. Save updates that SharePoint row. Add offers only skills they do not already have. The unique key on the list is the backstop if two saves race.

**Your conflicts.** Each interest is a row they can edit. One action, "Nothing to declare", updates their existing nil row and sets Last reviewed to today. It does not insert a second nil row.

The form runs as the signed-in person. It shows the rows SharePoint already allows them to open. Hiding a row in the gallery is convenience. The flow that stops sharing and grants access is the control.

Admins are not given a second product. They open the list, grouped by person, and export to Excel when they need a pack. Build an admin screen in the form only after an admin asks to avoid the list.

## What stays from v1

Two lists, Skills and Conflicts, with the columns in v1. Site owners are the named admins. The flow grants each new row to its creator and to the owners. Item sharing stays off. About 1,000 skill rows at 20 skills each, against a 5,000 unique-permission guidance line.

The Copilot Studio agent, for Microsoft 365 Copilot Business users only, updates the same rows and runs as that user. People without that add-on use the form. They are not sent to the agent, and they are not left in the grid.

Microsoft Forms is the wrong front door. Each response is a new item. The person never sees the skill they already saved. A flow behind Forms can try to find and patch the old row, and the staff experience is still "submit again" rather than "change this one."

## Check before the invite

Licence designation reads Standard.

Two test accounts. A saves a skill and a conflict in the form. B sees neither row in the form, in search, or in the agent. An owner sees both, grouped under A. A second save on the same skill changes the level and leaves one row.

Then five employees use the form for real. 4 of 5 completing one skill and either one interest or "Nothing to declare" is enough to invite the rest. 0 of 5 is a stop.

## Sources checked 22 October 2026

- Standard connectors, including SharePoint, need no special Power Apps licence: https://learn.microsoft.com/en-us/power-apps/maker/canvas-apps/connections-list
- Licence designation Standard means Power Apps for Microsoft 365 is enough: https://learn.microsoft.com/en-us/power-apps/maker/canvas-apps/license-designation
- Power Apps Basic with Microsoft 365 covers standard connectors and not premium connectors: https://www.microsoft.com/licensing/guidance/Power-Platform
- February 2027 enforcement scope (managed environments, model-driven apps, Dynamics context): https://learn.microsoft.com/en-us/power-platform/admin/powerapps-licensing-faq
- List columns, permission flow, and Copilot rights: `decision-principia-registers-v1.md`
