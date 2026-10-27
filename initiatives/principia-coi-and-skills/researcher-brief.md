# Researcher brief: Principia conflicts register and skills matrix

**Date:** 22 October 2026  
**From:** James Stock, Pro Drive  
**Client:** Principia Advisory  
**Pack:** `initiatives/principia-coi-and-skills/`  
**Current decision:** `prd/decision-principia-registers-v2.md` (v0 and v1 are history)

You are researching a client delivery, not a new Pro Drive product. Do not invent staff names, quotes, regulators, field lists, or headcount. Where a fact below is marked unknown, leave it unknown and say what evidence would close it. Read the decision file before you propose a different architecture. Reopen that architecture only if you find a sourced fact that breaks a requirement below.

## Client

Principia Advisory is an existing Pro Drive managed client (Supporting Data pack `principia-advisory`). The work runs in Principia's own Microsoft tenant. Data stays there.

| Fact | Value |
|------|--------|
| Employees | 50 |
| Base licence | Microsoft 365 Business Premium |
| Copilot | Most staff have a Copilot Business licence. Treat that as the Microsoft 365 Copilot Business add-on until a tenant admin confirms the SKU. Copilot Chat included with Business Premium is a smaller right and meters custom agents. |
| Monthly run-cost ceiling | About $500 a month is not justified |
| Named sponsor, admins, regulator | Unknown |
| Current workaround | Unknown. No one has been watched using it. |

Pro Drive's locked product work order is unchanged: EOS Operating Dashboard, then client monthly reports, then self-service travel. This brief does not jump that order.

## Jobs

Two jobs, one system.

1. **Conflicts of interest.** Staff record interests such as working for another company. A named admin can later produce each person's current position. Colleagues cannot read one another's interests.
2. **Skills.** Staff keep their own skills current. One person's skills are visible together. The same privacy rule was requested for skills. That rule blocks the usual reason for a skills matrix, which is staffing. Build privacy the way the brief asks. Add a skills reader only when a named person who staffs work asks for it.

## Functional requirements

- Staff update an existing entry. A correction to a skill or an existing interest edits that row. A genuinely new interest is a new row. A second save must not leave the old row in place as well.
- One employee's skills appear together. The admin view groups by person. A time-ordered feed fails this.
- Some fields are free text. Some are dropdowns. The dropdown lists are not specified. Do not invent the skill scale, the skill catalogue, or the conflict types.
- An employee sees only their own skills and their own conflicts.
- Specified admins see all rows and can produce a report. Dashboards are optional later, not part of the first release.
- A quiet period must still count as a review. Each person has one "Nothing to declare" row and updates the date on it. Silence is not evidence they looked.
- Staff get a form, not a grid. The form shows the rows they already have. Save writes back to the same row. Add skill offers only skills they do not already have.
- The form runs as the signed-in person. A gallery filter is not the security boundary. Item permissions are.
- People who already have Copilot Business may also update the same rows through a Copilot Studio agent in Teams. The agent runs as that user. People without the add-on use the form.

## Licence and cost constraints

- Stay inside Principia's Microsoft tenant and use Microsoft tools.
- Prefer licences they already pay: Business Premium, plus Copilot Business where it is already assigned.
- Azure spend is acceptable only when it is stronger or cheaper than extra per-user licences. At 50 people it is not cheaper. Pay-as-you-go Dataverse is $10 per person who opens an app in a month, which is $500. Power Apps Premium at £15.40 per user is £770 a month for 50. Both are refused.
- A Power Apps form whose only connection is SharePoint is included with Business Premium. The app's licence designation must read Standard before it is shared. Dataverse, a premium connector, a custom connector, an on-premises gateway, or a Managed Environment flips the cost back to the refused meter. Microsoft's February 2027 enforcement pass targets managed environments, model-driven apps, and Dynamics-licensed apps used outside that Dynamics environment.
- Power BI is not in Business Premium. Do not licence the firm for it.
- Confirm the Copilot SKU before publishing an agent. If the licence is only Copilot Chat from Business Premium, ship the form and leave the agent unpublished.

## Decisions already made

Do not redesign these unless a requirement above is impossible on this shape.

| Piece | Decision |
|-------|----------|
| Store | Two SharePoint lists: Skills, Conflicts |
| Staff door | One Power Apps screen in Teams. Skills and conflicts on that screen. |
| Security | A Power Automate flow using the standard SharePoint connector. On create, stop sharing, grant edit to the creator, grant read to the site owners. Item sharing off. |
| Admins | Site owners. They use the list grouped by person, and Excel export. An admin screen inside the form waits until an admin asks for it. |
| Nil return | One "Nothing to declare" row per person on the conflicts list. Last reviewed date. |
| Duplicate skills | Unique key of email plus skill. The form also hides skills they already have. |
| Copilot | Second door, same rows, licensed users only, user's own connection. |
| Scale | About 1,000 skill rows if each person has 20 skills. SharePoint guidance is 5,000 unique permission scopes on a list. Revisit near 4,000. |

Skills columns: Employee (set from the creator), Skill (choice), Level (choice), Notes (text), Skill key (unique).

Conflict columns: Employee, Type (choice, including "Nothing to declare"), Organisation, Role, Detail, Status (Current, Ended), Start, End, Last reviewed.

## Out of scope

- Dataverse, Dataverse for Teams, pay-as-you-go, Power Apps Premium
- Microsoft Forms as the front door (each response is a new row)
- A shared Excel workbook
- A canvas filter with no item permissions
- A custom Azure web app
- A skill catalogue list, until the choice dropdown is too long to use
- A separate attestation list
- Power BI on day one
- An agent for staff who do not have Copilot Business
- Hosting the data in Pro Drive's tenant
- A Pro Drive product SKU

## What you should find out

Answer these from Principia, or say you cannot. Do not fill them from general practice.

1. Who is the sponsor, and who are the named admins?
2. Where do conflicts and skills live today, and what does that workaround cost?
3. What belongs on the skill dropdown, and what is the level scale?
4. What conflict types and statuses does Principia actually use?
5. Does anyone who staffs work need to read skills, and are they allowed to see conflicts?
6. How often must a person review, and who chases a missing review?
7. May an employee delete a conflict, or only close it?
8. Is there a policy, contract, or regulator that sets the fields or the retention? Cite it, or record that there is none.
9. Which licence SKU is on a person described as having Copilot Business?
10. Has anyone asked for a dashboard, and who would read it?

## Checks already set

No test has been run.

- Two accounts. The second sees none of the first account's rows in the form, in search, and in the agent. An owner sees both, grouped under the first person. A second save on the same skill leaves one row.
- Five employees then use the form. 4 of 5 saving one skill and either one interest or "Nothing to declare" is enough to invite the other 45. 0 of 5 stops the rollout.

## Evidence rule

One sponsor brief plus three later constraints (50 employees, the $500 ceiling, Copilot Business, and the request for a form) is the whole input. Interest is not demand. A category such as "staff" or "admins" is not a person. If you cannot name the human or show the current file, say so.
