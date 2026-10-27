# Research findings on the Principia registers

**Returned:** 22 October 2026  
**Reviewed:** 23 October 2026  
**Scope:** Microsoft documentation and Principia's public privacy notice. The tenant, the current files, and the licence assignments were not opened. No test was run.

## Held

The two SharePoint lists, the Teams form, the standard-connector permission flow, the grouped admin view, and the optional Copilot agent remain possible on Business Premium. Pay-as-you-go at $500 a month for 50 people, and Power Apps Premium at £770 a month, stay refused. Power BI stays out.

About 1,000 skill rows with their own permissions sits under the 5,000 recommended unique scopes per list. The 50,000 figure is the technical ceiling, not the target. The 5,000 list-view threshold is a query limit, not the maximum size of a list.

`Patch` on the existing record keeps the SharePoint item id. A new skill is the only path that creates a new id. The unique skill key still rejects a duplicate if the dropdown fails.

## Accepted, and tightened in decision v3

- Items inherit the list permissions until the flow finishes. The build closes the list to employee read before that gap, then tests it. A failed test moves creation into an owner flow. It does not move the store to Dataverse.
- Edit includes delete. The employee role ships without delete. Principia can add delete in writing.
- Site owners have Full Control. The decision will not call them read-only.
- "Nothing to declare" beside a Current interest is ambiguous. The form shows that action only when no Current interest exists.
- The agent authenticates the user and uses that user's credentials. In Teams it is a 1:1 chat. Channels and group chats do not get SharePoint as that user.
- A Standard badge on the app does not prove the flows are standard. Inspect the flows.
- The form and the agent have separate release decisions.

## Not evidence

The public notice at https://www.principia-advisory.com/wp-content/uploads/2026/08/Principia-Privacy-Policy-v3.pdf is the website and customer notice for Principia Advisory SARL. It points retention detail to a records management policy via dpm@principia-advisory.com. It does not set fields, readers, or retention for staff skills or conflicts, and it names no regulator for this register.

Skill names, level scale, conflict types, the sponsor, the site owners, the current workaround, the review cycle, and the Copilot SKU are still unknown. Do not fill them from general practice.
