# Solutions after a 50-person cost ceiling

**Topic:** Principia conflicts register and skills matrix  
**Version:** v2  
**Date:** 2026-10-22  
**Replaces:** `solutions-principia-registers-v1.md` for the recommendation. v1 stays as the Dataverse comparison.  
**New inputs:** 50 employees. About $500 a month is not justified. Most staff hold a Copilot Business licence.  
**Recommend:** Two SharePoint lists, one included flow, one Power Apps form in Teams as the staff door, one Copilot Studio agent for licensed staff. The form was added in `prd/decision-principia-registers-v2.md` after v1 left people in the grid. The form uses only the SharePoint connector, so it stays on Business Premium.

## What changed

v1 recommended one Dataverse canvas app on pay-as-you-go because it gave real row security inside Microsoft's stack. At 50 people who open the app in a month, that meter is $500. James refused that bill. The same refusal removes Power Apps Premium at £770 a month for 50 assigned users.

The privacy requirement still stands. A list filtered to the current user is not security. The smaller control that costs no extra licence is a SharePoint item permission set by a flow Principia can already run.

Copilot Business changes the front door, not the record. Microsoft 365 Copilot user licences include Copilot Studio agents in Teams, SharePoint, and Copilot when the agent runs as that licensed user, within fair use. The lists remain the place the row lives.

## Recommendation

| Piece | What it is | Licence |
|-------|------------|---------|
| Skills list | One row per person per skill. Unique key stops a second row. Choice columns for skill and level. | SharePoint in Business Premium |
| Conflicts list | One row per interest, edited in place. One "Nothing to declare" row per person, with a Last reviewed date. | SharePoint in Business Premium |
| Permission flow | On create, stop sharing, grant edit to the creator, grant read to site owners. | Standard SharePoint connector, included |
| Admin view | Grouped by person. Export to Excel. | List view |
| Agent | Updates the same rows in Teams for people who hold Copilot Business. Connection is the signed-in user. | Included with that licence, fair use |

Staff without Copilot Business use the list. They are not blocked, and they are not put on an agent meter.

## Rejected for this client

| Option | Why it is out |
|--------|----------------|
| Dataverse pay-as-you-go | $500 in a month when 50 people open one app |
| Power Apps Premium | £15.40 × 50 = £770 a month, paid in quiet months too |
| Dataverse for Teams | Creation ends 15 November 2026, then the upgrade needs the licences above |
| Canvas app on the lists | The list form already edits a row. A second interface is spare parts. |
| Microsoft Forms or a shared workbook | New rows, or no row security |
| Custom Azure app | Two lists do not need a codebase |
| Agent as the only door | The minority without Copilot Business would be metered, and a matrix is still a list |

## Ceiling

Stay under about 4,000 uniquely permissioned rows on each list. Twenty skills for each of 50 people is about 1,000. That fits. Past that point, stop and look again. Do not pre-build the exit.
