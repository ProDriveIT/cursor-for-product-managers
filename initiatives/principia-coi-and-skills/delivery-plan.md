# Delivery plan: Principia interests and skills

**Date:** 27 October 2026  
**Status:** Agreed design. Possible on Microsoft 365 Business Premium. Client sign-off is still open. Do not publish to all 50 until the tests below pass.  
**Client letter:** `prd/client-proposal-registers.md`  
**Reply to Catherine:** `prd/reply-to-catherine-2026-10-27.md`  
**Example screens:** `prototype/mock-up.html` and `prototype/principia-form-examples.zip`

## What we are building

Two forms in Teams, in Principia's tenant. One for outside interests. One for skills. Staff open only the form they need. Each save updates the entry that is already there.

This is not Microsoft Forms. A Microsoft Form stores a new response on every submit.

The records stay in two SharePoint lists. Named people download a CSV copy for their own Excel pivots. That file is not linked to the lists.

## Licensing

Microsoft 365 Business Premium includes Power Apps and Power Automate cloud flows. SharePoint and Excel Online (Business) are standard connectors. Two screens, choice questions, a details box, and free text stay inside that entitlement. There is no new Microsoft subscription and no monthly fee.

Do not add a premium connector, a custom connector, Dataverse, an on-premises gateway, or a Managed Environment. Any of those can require a paid Power Apps licence even if the app still shows Standard. Check the app badge and open every linked flow.

Copilot chat is not part of Business Premium. Turn it on only after a tenant admin confirms the paid Copilot add-on on those users, and only as a private Teams chat using that person's own login. If the check fails, leave the chat off. The forms still stand.

## Forms

**Outside interests.** One entry per company. Fields: company, role, status (Current or Ended), last updated, notes. Update changes that entry. Add creates a new company. People mark an interest ended. They cannot delete it. "Nothing to declare" appears only when they have no current interest.

**Skills.** One answer per question. Question types:

- Choice only
- Free text
- Choice plus details, shown only for the answer that needs it (Catherine's example: No, Would like to, Yes, and details when the answer is Yes)

Saving again updates that answer. The question list is not final. Build the form after Principia sends the wording.

## Who sees what

Each person sees only their own entries. Two or three named people see everyone's. They are site owners in practice, with full control, not read-only auditors. Name them before go-live.

The list must not let staff read every row before the permission step runs. Staff can add. They cannot read the list as a whole. Then grant the creator access to their own item, with edit and without delete. Test a second account during that step and after it, in the form, by a direct link, and in search. If the second account can open the row in the gap, create the item in a flow that sets the permissions before the form shows it. Stay on SharePoint.

## Spreadsheet

Named people use **Export to CSV**, or a file we generate the same way. Microsoft states that CSV is not connected to the list. Do not use **Export to Excel**. That download is a connection file (`query.iqy`) and Excel can refresh it from the live records.

Prepare a view with only these headings, in this order, every time:

- Skills: Name, Question, Answer, Details, Last updated. One row per answer.
- Interests: Name, Company, Role, Status, Last updated, Notes. One row per company.

They paste each file onto its own data tab and refresh the pivots. The first time, they build the pivots. After that they do not clean or rename columns. A new skill question adds rows. It does not change the sheet. Fifty people sits under the 30,000-row CSV limit.

## Time and money

Two to three working days of Pro Drive time once an administrator has given access. Quote the fee after internal sign-off, before any build. Copilot, if they ask later and the licence check passes, is one further working day. No pound figure is in the client letter. There is no day rate in this pack.

## Not in this build

Dataverse, pay-as-you-go, Power Apps Premium, a live Excel link, a dashboard, Power BI, and the Copilot chat until the licence is confirmed.

## Before anyone else is invited

1. Licence designation reads Standard, and every linked flow uses only standard connectors.
2. Account B sees none of account A's rows in the form, by direct link, and in search, including in the moment after create.
3. A second save on the same skill or the same company keeps the same record.
4. A duplicate skill question for the same person is rejected.
5. "Nothing to declare" is absent when a current interest exists.
6. The CSV headings match the lists above.

Then five people try the form they need. Four of five completing it is enough to invite the rest. Zero of five stops the rollout.
