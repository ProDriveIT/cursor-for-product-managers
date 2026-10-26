# Approve a sales-only pilot of the quoting agent

**Initiative:** Sales catalogue quoting  
**Owner:** Dan  
**Decision owner:** Bruce Penson  
**Date:** 23 Oct 2026  
**Status:** Draft, waiting on Bruce

## Outcome

Sales quotes for Pro Drive services still depend on whoever last opened the SC:020 guide, or on a copy someone saved. A copied price becomes wrong the day the guide changes, and a seller under pressure will fill a blank fee from memory. The outcome of this product is a quote a seller can stand behind: every time, place, role, and fee on the page is on the live guide, and every blank is labelled "Not in the guide" with the document name, link, and updated time.

The pilot test is concrete. One seller asks three questions, including one that names two services. You, or Dan with you watching, open the IT Glue pages. Every number in the answer is on those pages. Any number that is not on the page fails the pilot. There is no count of quotes per week to use as a baseline, so this pass/fail check is the metric.

- The source of a quote is the live SC:020 guide, read at the time of the question.
- A missing monthly fee stays missing. The agent does not invent one.
- Pilot bar: one seller, three questions, numbers match the guides.
- No weekly quote volume is on record. Do not treat a time-saved claim as a result.

## Opportunity needs two guides, not a blended total. On 23 Oct 2026 the agent returned those as separate setup guides: Datto SaaS backup, document `1728698485424363`, new setup 2 hours, updated 2024-08-19; Datto Secure Edge, document `3359347199295674`, 4 hours, updated 2023-09-21. Both guides name catalogue codes and omit the monthly managed service fee. The answer said so.

That is the opportunity. Sellers can ask in Copilot and get the guide's own words, including the gaps, without a spreadsheet. The opportunity collapses if the gaps are so common that sellers stop trusting the answer and go back to asking a person. Both proof quotes were missing the fee. If that is typical, the valuable next act is to fill the guides, and the agent is only as useful as that work.

This supports goal B on the product map: selling services to existing clients. It is an internal sales tool. It is not a client SKU and it does not reduce reactive tickets. Quarter OKRs are not written in `company-level-context/okrs/`.

- One question can name more than one service. Each service keeps its own time and fee.
- The proof pair is Datto SaaS (2 hours) and Datto Secure Edge (4 hours). The monthly fee was absent in both.
- Goal B is the link. This agent is not a product you sell.
- If guides stay blank, sellers will ignore the agent.

## Lessons

The hard part was not reading IT Glue. The hard part was stopping the agent from calling the tool with an empty question, asking the seller for a document id, or treating a pair of quote marks as an id. Those faults are fixed in the test agent. Search text is the seller's message. The document id goes through blank. A quote takes about a minute because the function reads the live folder list. The flow allows 90 seconds.

The uncomfortable lesson is in the catalogue. A quoting agent will not be more complete than SC:020. Both proof guides tell the seller the work is remote, name a PS engineer, and name Autotask catalogue codes, then leave the monthly fee out. Shipping the agent to sales before you accept that behaviour will look like a broken bot. It is a faithful bot in front of a thin guide.

Dan has not had a seller use the chat. The test chat was James's. Dan needed a click-by-click guide to connect the flow. The Cursor skill that James uses in his own editor is a different tool and is outside this product.

- Empty inputs and a fake document id were real faults. They are fixed in test.
- A quote takes about a minute. That wait is the live read.
- The monthly fee was missing on both proof guides.
- No seller has used it. James's test chat is not a sales trial.

## Solutions and assumptions

The path already in test is one Copilot agent, Service Catalogue Quoting Assistant, with one flow that calls one Azure function. The function reads IT Glue. The agent writes a summary table with one column per service, then a short section per service. Client-sendable wording is only the Service Specification. Dan publishes it. You decide who can open it.

**Value.** Sellers will prefer a labelled gap to a remembered fee. If they do not, the agent will not replace the side list. Test: the seller's three questions, then one sentence from that seller on whether they would send the sheet without opening IT Glue.

**Viability.** Prices stay inside sales. A company-wide Copilot publish puts the catalogue in front of people who should not quote it. The IT Glue key stays on the function. Dan holds a function key only. Test: you name the sales security group before Dan publishes. There is no revenue number attached to this tool.

**Feasibility.** The two proof quotes returned the document ids above and kept 2 hours and 4 hours apart. Test: the same check on the seller's three questions, including one two-service question. A run that finishes in under a second did not read the guide.

**Usability.** A seller can ask in plain language and get the table without knowing what an SC:020 is. That is untested. Dan's build pain is not the seller's pain, but it is a warning that the tool is brittle to edit. Test: the seller runs the three questions with you or Dan present and James not typing.

- One agent, one flow, one function, live read.
- Value fails if sellers will not tolerate "Not in the guide".
- Viability fails if the agent is published outside sales.
- Feasibility is proved on two guides. Usability is not proved on a seller.

## Decision requests

Choose one.

1. **Pilot.** You read the Datto SaaS plus Datto Secure Edge answer and confirm the 2 hours, the 4 hours, and the missing monthly fee match the two IT Glue pages. You name the sales security group. Dan publishes to that group only. One seller then runs three questions. The pilot passes only if every number is on the guide.
2. **Hold.** The agent stays in the test chat until the monthly fee is in the guides you care about. No seller gets access yet.
3. **Stop.** Sales keep quoting from IT Glue themselves. Dan does no further work on this agent.

Recommendation: **1.** You check one two-service answer before anyone else sees it. Company-wide publish is the wrong call. Stopping leaves quotes in copies and in memory, which is the problem this agent is here to end.

After you choose 1 and the three-question check passes, the next product document is a PRD. Until then, a PRD would freeze rules a seller has not used.
