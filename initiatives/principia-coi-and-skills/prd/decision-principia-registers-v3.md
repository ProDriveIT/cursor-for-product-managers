# Keep the two lists. Close three gaps before anyone else can open a row

**Status:** v3 decision. Replaces the release rules in `decision-principia-registers-v2.md`. Not an approved PRD. Not a quote.  
**Date:** 23 October 2026  
**Client:** Principia Advisory, 50 employees  
**Decision owner:** James Stock  
**Input:** Deep research returned 22 October 2026. It found no Microsoft limit that forces Dataverse, Power Apps Premium, Azure, or Power BI. Principia's tenant was not opened. No acceptance test has been run.

Build the agreed shape. Do not publish it to all 50 until the tests in this note pass.

- Two SharePoint lists, Skills and Conflicts, in Principia's tenant.
- One Power Apps screen in Teams. It shows the signed-in person's rows and saves back to the same row.
- One standard-connector flow sets item permissions.
- Admins use the list, grouped by person, and Excel export.
- Copilot Studio is a separate release, and only for people whose Copilot Business add-on is confirmed.

## What the research changes

### 1. The list must be closed before the flow runs

A new SharePoint item inherits the list's permissions until the flow stops sharing it. If staff can read the list, a colleague can open that item in the gap.

Employees get a list permission that can add an item and cannot read the list. The flow then grants the creator access to that item only. Site owners keep Full Control. They are not read-only auditors. Name them before go-live.

Test Account B against Account A's new row in the form, by direct link, in search, and in the agent, both during the flow and after it. If B can open A's row in that gap, create the item through an owner-connection flow that sets the item permissions before the form shows the row. Check the caller's identity inside that flow. Stay on SharePoint. That result is not a reason to buy Dataverse.

### 2. Staff can edit a conflict. They cannot delete it

SharePoint Edit includes delete. A conflicts row that can be removed is a hole in the register. Grant a custom item role: edit, no delete, no share. Status Ended and Last reviewed are how a row closes.

Add delete only if the sponsor writes that a mistaken row may be removed. Version history is not a substitute for that decision, and waiting for the letter is not a reason to ship Edit.

### 3. "Nothing to declare" means there is no current interest

If the person already has a Current conflict, that button does not appear. They confirm the interests on the form, and Save stamps Last reviewed on those rows. It does not clear them and it does not add a nil row on top.

The nil row is used only when they have no Current interest. One row, updated date. The wording on the screen has to say that. `Current`, `Ended`, and `Nothing to declare` are still our labels, not a Principia policy.

## Copilot stays a second release

Publish the agent only after the form's tests pass, and only when a tenant admin shows the assigned SKU is Microsoft 365 Copilot Business. Copilot Chat from Business Premium meters custom agents. If the SKU is wrong, leave the agent unpublished.

The agent uses Authenticate with Microsoft and the employee's own tool credentials. A maker connection that can read the lists is a fail. In Teams it is a 1:1 chat with the agent. Group chats and channels cannot use SharePoint as that user. Microsoft documents this as a limit, not a setting.

## Licence check

The canvas app must show licence designation Standard. That badge is not enough. Open every linked flow. A premium connector in a flow does not change the badge, and it still needs a premium right. No Dataverse, no custom connector, no on-premises gateway, no Managed Environment, no pay-as-you-go, no Power BI.

## One document to ask for

Principia's website and customer privacy notice, August 2026, is for Principia Advisory SARL and covers website visitors and customers. It limits access to people with a business need to know. Retention periods for that notice sit in a records management policy, requested from dpm@principia-advisory.com.

The notice does not mention staff skills or conflicts, and it names no regulator for this register. Ask the DPM whether that policy covers employee conflicts and skills. Quote the clauses that do. If it does not, record that and move on. Do not treat the customer notice as the rule for this register.

https://www.principia-advisory.com/wp-content/uploads/2026/08/Principia-Privacy-Policy-v3.pdf

## Release

The form can go to the five-person pilot without the agent. Four of five people saving one skill and either one interest or a nil declaration, after the privacy tests pass, is enough to invite the other 45. Zero of five stops the rollout. The agent has its own go-ahead: SKU, 1:1 chat, and the same privacy test through the agent.

No dashboard, no staffing reader, and no extra licence until a named person asks.

This remains client work in Principia's tenant. It does not move EOS Operating Dashboard, client monthly reports, then self-service travel.

## Sources checked 23 October 2026

- Item permission actions, including a custom role id: https://learn.microsoft.com/en-us/sharepoint/dev/business-apps/power-automate/guidance/manage-list-item-file-permissions
- Permission levels, including Edit and Delete: https://learn.microsoft.com/en-us/sharepoint/understanding-permission-levels
- Teams agents that need the user's SharePoint access work in 1:1 chat, not in channels or group chats: https://learn.microsoft.com/en-us/microsoft-copilot-studio/publication-add-bot-to-microsoft-teams
- App licence designation, and the gap where a premium flow leaves the app marked Standard: https://learn.microsoft.com/en-us/power-apps/maker/canvas-apps/license-designation
- Principia website and customer privacy notice, August 2026: https://www.principia-advisory.com/wp-content/uploads/2026/08/Principia-Privacy-Policy-v3.pdf
