# Assumptions after the cost ceiling

**Topic:** Principia conflicts register and skills matrix  
**Version:** v2  
**Date:** 2026-10-22  
**Replaces:** the pay-as-you-go recommendation in `assumptions-principia-registers-v1.md`  
**Solution under test:** Two SharePoint lists, one permission flow, one Copilot agent for licensed staff. See `prd/decision-principia-registers-v1.md`.

## What is now decided

| Earlier assumption | Position on 22 October 2026 |
|--------------------|-----------------------------|
| Pay-as-you-go at $10 per active user is acceptable | Withdrawn. 50 employees is $500 in a month they use it. James refused that. |
| Premium at £15.40 is the fallback | Withdrawn on the same bill. £770 a month for 50. |
| Tenant can link Azure pay-as-you-go | No longer required. |
| Sponsor must choose a skills reader list before any build | Withdrawn as a gate. Build both lists private to the employee and the site owners. Add a skills reader when someone who staffs work asks. |

## Still unproven

**D1. Staff will edit a row.** Five employees each save one skill and either one interest or a "Nothing to declare" row, after the two-account privacy check. 4 of 5 within five business days is a pass. 0 of 5 is a stop. An empty register is still a failure, and it is a cheap one.

**F2. Item permissions hold.** Account B sees 0 of account A's rows in the list, in search, and through the agent. An owner sees 2 of 2. The agent connection is the signed-in user.

**F4. The Copilot SKU is the paid add-on.** Someone with tenant admin rights confirms the licence on a licensed user is Microsoft 365 Copilot Business, not only the Copilot Chat included with Business Premium. 1 of 1 written confirmations before the agent is offered to staff. If the SKU is the free chat, ship the lists and leave the agent unpublished.

No test has been run.
