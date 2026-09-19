# 1-Pager: Client monthly report — Quest Fund Placement pilot

**Initiative:** client-monthly-report  
**Owner (ops):** James Stock (Head of Operations)  
**Pilot client:** Quest Fund Placement (`Quest Fund Placement Ltd` in Autotask / KPI data)  
**Pilot vCIO:** Bruce Penson  
**Pilot TAM:** Danny Bray  
**Decision makers:** James, Bruce (and Danny on TAM cadence / meeting footer inputs)  
**Date:** 2026-09-19  
**Status:** Draft for decision  
**Prior art:** [prior-art-github-repos.md](../prior-art-github-repos.md)  
**Engineering path:** [Reporting Agent](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-09%20agent-ecosystem-copilot) on [Insights client packs](https://github.com/ProDriveIT/GitHub-Repos/blob/main/10%20Projects/2026-01%20reporting-kpi-automation/Documentation/Monthly-Client-Service-Report.md)

---

## Outcome

Pro Drive’s proactive model is working: reactive tickets and issues have fallen. That success creates a commercial blind spot. Clients who once measured us by “how many tickets did you fix?” now ask what they are paying for. The outcome of this initiative is that **Quest Fund Placement’s economic buyers leave the monthly cycle able to name the proactive, initiative, and alignment work Pro Drive did for them**, and walk into the next **vCIO / TAM** conversation with that evidence in hand, without Pro Drive inventing numbers or sending an unreviewed pack.

For the pilot, “working” means one concrete bar: for a single calendar month, Bruce (vCIO) receives an HTML **draft** rooted in the Azure Insights client pack for Quest, spot-checks that the numbers match the pack, **approves** it, and either sends it or stages it for send. Cycle time target: draft available the same day the pack lands in SharePoint KPI Insights. Zero client sends without Bruce’s approval trail.

- Pilot: Quest Fund Placement · vCIO Bruce · TAM Danny · ops owner James
- Success bar: one month, Bruce-approved HTML draft whose numbers match the Insights pack
- Cadence goal: draft same day as pack drop; no auto-send
- Client outcome to test: buyer can answer “what are we paying for?” from the report + next vCIO/TAM meeting

## Opportunity

The opportunity is not “build another reporting platform.” It is to make proactive MSP value **legible** to one named client using the spine Pro Drive already owns: Autotask → Azure Insights client packs → Copilot **Reporting Agent** → vCIO sign-off → send. Quest is a real account with ticket history in the KPI pipeline and prior project work in the vault (AI governance, DLP, Copilot memo tooling). That makes it a fair pilot: enough proactive and alignment work to show, and a vCIO (Bruce) who already owns the account relationship.

Without this surface, low reactive volume reads as low service. Ticket dumps make that worse. A monthly HTML pack that separates preventative and end-user work (pack numbers) and, in Phase 2, adds Bruce’s narrative plus next **vCIO and TAM meeting** dates turns the proactive model into something Quest can renew and expand against. Expansion to other clients is a later decision; this opportunity is Quest’s first approved cycle.

- Primary operator: Bruce (vCIO); TAM context: Danny; builder/ops: James
- Pain: proactive success looks like “nothing happened” to the buyer
- Bet: one approved Quest pack proves the value-visibility loop before multi-client rollout
- Non-opportunity for this decision: revive archived `reporting-client` PowerShell; rebuild KPI math; auto-send; full multi-client launch

## Lessons

Three prior starts teach the constraints for this decision. First, the Jan 2026 **value-add** HTML generator solved the same problem (show work clients cannot see), was **STOP’d in August 2026** under the RTEM mission filter, and was **superseded 19-09-2026** (DO NOT RESUME) in favour of Insights packs + Reporting Agent. Second, **Insights client packs** (WIP-027) already encode preventative vs end-user, jobs, and alignment from Autotask; inventing a second numbers engine breaks trust. Third, the Sep 2026 **Reporting Agent** pack already locked draft ≠ send, vCIO as sign-off, and pack-as-truth. The uncomfortable gap: we do not yet have a Quest-specific recorded quote of “what are we paying for?”; the demand signal is company-wide. The pilot must produce buyer reaction evidence, not assume the report will be loved.

- Lesson: same problem already had a STOP’d tool; it is now **superseded** — consolidate, don’t fork
- Lesson: numbers come only from Insights packs; agents never invent metrics
- Lesson: vCIO approval is the gate; auto-send is out
- Gap: Quest buyer reaction is untested; pilot must capture it

## Solutions & Assumptions

**Selected solution (wedge):** Run **Reporting Agent Phase 1** for Quest Fund Placement only. Azure monthly Insights produces `client-pack-*.html` for the Autotask account `Quest Fund Placement Ltd`; Logic App lands it in SharePoint KPI Insights; Bruce asks Copilot Reporting Agent to draft that month; draft stores under Quest’s Drafts folder; Bruce approves or requests changes; send is human-gated. Phase 2 (vCIO narrative list + next **vCIO and TAM meeting** dates from the meeting calendar) starts only after Phase 1 exit. Archived `Generate-ClientValueAddReport.ps1` stays archived; its category framing may inform narrative copy later, not a second generator.

| Risk axis | Assumption | Test plan |
|-----------|------------|-----------|
| **Value** | A pack-based HTML draft, once Bruce-approved and shown to Quest, reduces “what are we paying for?” friction for that account | After first send (or walkthrough in a vCIO/TAM meeting), capture Quest contact reaction in writing; renew/expand conversation tone vs prior month |
| **Viability** | Bruce will operate the draft → approve loop for Quest; Danny will supply TAM meeting context when Phase 2 starts | Bruce completes one full approve cycle; log time from pack-ready to approve |
| **Feasibility** | A known-good Insights pack exists (or can be produced) for Quest for one `YYYY-MM`, and Reporting Agent can locate it under KPI Insights | Confirm pack file for Quest + month before agent build polish; kill Phase 1 if pack cannot be produced for Quest |
| **Usability** | Bruce can get a reviewable draft in Copilot without James hand-building HTML each month | Bruce runs the draft prompt once with James observing; count manual steps and failures |

Open assumptions: whether Quest’s pack already lands in `{AccountSlug}/` or still in the flat KPI Insights root (Sep 2026 debt); exact path of the external reports repo for HTML chrome; which Quest contact is the economic buyer for the reaction test.

- Solution: Reporting Agent Phase 1 on Quest only; Phase 2 after exit
- In: Insights pack numbers, Bruce sign-off, HTML artefact, human-gated send
- Out: archived value-add launcher, auto-send, multi-client rollout, inventing narrative numbers
- Pre-flight: confirm Quest pack for chosen month exists before calling the pilot “live”

## Decision Requests

James and Bruce are asked to decide the following. The recommended path is **A**.

1. **Pursue this opportunity now?**  
   - **A (recommended):** Approve the Quest Fund Placement pilot on Reporting Agent Phase 1: one calendar month, Bruce as vCIO sign-off, Danny as TAM context owner, James as ops owner. Exit = Bruce-approved draft matching pack numbers; then capture Quest buyer reaction.  
   - **B:** Gather more demand evidence first (interview Quest economic buyer before any draft).  
   - **C:** Reject / defer; keep RTEM and internal KPI reports only; no client-facing monthly HTML this quarter.  
   - **D:** Restart a separate value-add generator outside Insights / Reporting Agent (not recommended; repeats the STOP’d path).

2. **Scope lock:** Confirm Phase 1 excludes auto-send, multi-client rollout, narrative list, and meeting footer until Quest’s first approved draft exists. Confirm archived `reporting-client` stays archived.

3. **Pilot month:** Agree the first `YYYY-MM` once James confirms a Quest Insights pack is available (or scheduled) for that month.

4. **Sign-off:**

| Name | Role | Decision (A/B/C/D) | Approve scope lock? | Pilot month | Date |
|------|------|--------------------|---------------------|-------------|------|
| James Stock | Head of Operations | A (proposed) | | | 2026-09-19 |
| Bruce Penson | vCIO (Quest) | | | | |
| Danny Bray | TAM (Quest) | (ack / meeting inputs) | | | |

**Recommendation:** Choose **A**. Next operational step after sign-off: James confirms Quest pack for the chosen month in SharePoint KPI Insights, then Bruce runs one Reporting Agent draft → approve cycle.
