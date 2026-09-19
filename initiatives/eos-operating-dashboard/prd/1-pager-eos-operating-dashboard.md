# 1-Pager: Leadership L10 Console (EOS Operating Dashboard v1)

**Initiative:** eos-operating-dashboard  
**Owner:** James (Integrator)  
**Decision makers:** James, Bruce, Matt (all three must sign off)  
**Date:** 2026-09-19  
**Status:** Draft for decision — **Revision 2 active** (Hub rejected after use; revive Azure/CEOS dashboard)  
**Related:** [Diagnostic](../diagnostic-eos-dashboard.md) · [Company context](../../../company-level-context/prodrive-context.md)

---

## Outcome

Pro Drive has tried EOS before and dropped it. The operating rhythm never lived in one place, the MD remixed the process until it stopped being EOS, and department Traction collapsed into passenger meetings. The outcome we want from this initiative is narrower and measurable: **five consecutive leadership Level 10 meetings run to pure EOS**, with Scorecard KPIs either updated on the dashboard before each meeting or collected through the current KPI entry methods (automated where they already are, manual where they are not) and reflected on the same Scorecard the room uses. James’s prep on the Friday before the Monday L10 stays **under 20 minutes**. Bruce has already accepted this as the way leadership will run L10s; the product must make that acceptance stick by putting the agenda, Scorecard, Issues, and To-Dos on one shared screen instead of Teams threads, notes, and SharePoint variants.

- Target: 5 consecutive pure-EOS leadership L10s
- KPI path: dashboard before meeting, or current automated/manual → spreadsheet → Scorecard flow mirrored into the dashboard
- Integrator prep: Friday before L10, under 20 minutes
- Social proof already present: Bruce has accepted this as the L10 method

## Opportunity

The opportunity is not “build an EOS platform.” It is to give the Integrator a single, opinionated place to run the leadership L10 so process fidelity survives contact with a strong MD and a time-poor management peer. Today, KPI truth still partially lives in a spreadsheet that feeds a management Scorecard; meeting admin still risks splintering across channels. When that happens, James spends the week chasing Rocks, Issues, and numbers, and Bruce defaults to improvising. A Leadership L10 Console on infrastructure Pro Drive already owns (Azure, Microsoft 365, Copilot) creates one system of record for the room: fixed agenda, live Scorecard, Issues, and To-Dos. That lowers James’s admin cost enough that he can enforce the plan, gives Bruce an on-screen “what next and why,” and sets Matt up for a later 2-minute update habit once room mode works. Client reporting, department Traction, Focus Days, and AI chase are dividends of stored data later; they are not this opportunity.

- Primary user: James (Integrator); contributors: Bruce (plan fidelity), Matt (later async updates)
- Pain: no SSOT for L10; remix culture; Integrator chase/admin load
- Bet: shared-screen L10 room mode on Azure/M365 makes a second EOS adoption stick
- Explicit non-opportunity for v1: full Traction suite, departments, time logging, third-party EOS SaaS

## Lessons

The last EOS attempt taught four lessons this proposal takes as constraints. First, when artifacts live in a whiteboard loop, notes, Teams, and SharePoint, every meeting becomes a different process. Second, if Bruce can reshape the method in the room without a canonical artifact, peers will not challenge him and EOS dies by a thousand tweaks. Third, a third-party implementer helps with accountability, but software cannot replace authority; the product only works if James (and the implementer) use the screen to hold the line. Fourth, pushing Traction into departments before leadership cadence is real produces solo meetings and passengers. We also learned what not to build first: time logging (not required), AI automation of chase (amplifies empty data), and buy-vs-build via Ninety or similar (ruled out by the self-hosted constraint).

- Lesson: SSOT beats multi-channel “wherever we wrote it down”
- Lesson: customization killed fidelity; v1 must be hard to fork
- Lesson: leadership L10 before department rollouts
- Lesson: no third-party EOS tools; stay on Azure / M365 / Copilot inside Pro Drive

## Solutions & Assumptions

**Selected solution (wedge B):** Build a Leadership L10 Console: shared-screen room mode with a fixed pure-EOS agenda, Scorecard, Issues list, and To-Dos, hosted and managed on Pro Drive’s Azure and Microsoft 365 stack, with Copilot available only where it helps inside that boundary. v1 does not include async Matt updates (v1.1 after room mode proves out), Focus Days, department portals, time logging, or a customization sandbox for Bruce. KPI ingestion for v1 may continue to accept the existing automated-plus-manual → spreadsheet path so Friday prep stays under 20 minutes while the room runs from one Scorecard view.

| Risk axis | Assumption | Test plan |
|-----------|------------|-----------|
| **Value** | Five pure-EOS L10s on one screen are worth eng spend vs restarting on spreadsheets alone | Count consecutive compliant L10s; stop build expansion until 5 are hit |
| **Viability** | Bruce, James, and Matt will all sign off and Bruce will keep accepting the fixed agenda for the trial | Written sign-off on this 1-pager; after L10 #2, check whether agenda was remixed |
| **Feasibility** | L10 room mode can be built and hosted entirely on existing Azure / M365 / Copilot without third-party SaaS | Architecture spike in `ProDrive-EOS` (or successor repo): auth (Entra), data store, app host; kill custom build if spike fails |
| **Usability** | James can prep Friday in under 20 minutes and run Monday L10 from the screen without leaving to Teams/SharePoint for core artifacts | Time James’s Friday prep for first 3 L10s; log every off-screen fetch during the meeting |

Open assumptions still untested: eng access and state of the EOS code repo; exact list of automated vs manual KPIs; implementer name and whether they will facilitate from this console; whether Matt will adopt async updates in v1.1.

- Solution: opinionated Leadership L10 Console on Azure/M365/Copilot only
- In: fixed agenda, Scorecard, Issues, To-Dos; spreadsheet-fed KPIs allowed in v1
- Out: third-party tools, time logging, AI chase, departments, Focus Days, Bruce remix tools
- Next slice after success: Matt’s 2-minute async Scorecard/Rock updates (v1.1)

## Decision Requests

James, Bruce, and Matt are asked to decide the following together. The recommended path is **A**.

1. **Build now?**  
   - **A (recommended):** Approve building Leadership L10 room mode on Pro Drive Azure / M365 / Copilot, scoped as above, aimed at five consecutive pure-EOS leadership L10s and sub-20-minute Friday prep.  
   - **B:** Pilot 4–8 weeks on a rigid non-app template first, then reconsider build.  
   - **C:** Reject custom build and restart EOS without a Pro Drive–hosted console (conflicts with “no third-party tools” if the alternative is Ninety-class SaaS).  
   - **D:** Do not restart EOS until accountability agreements (Bruce + implementer) are rewritten, independent of software.

2. **Scope lock:** Confirm v1 excludes department Traction, Focus Days, time logging, third-party SaaS, and AI chase until five consecutive compliant L10s are recorded.

3. **Sign-off:** James / Bruce / Matt each mark Approve or Reject on option A with date.

| Name | Role | Decision (A/B/C/D) | Approve scope lock? | Date |
|------|------|--------------------|---------------------|------|
| James | Integrator | | | |
| Bruce | MD | | | |
| Matt | Management | | | |

---

## Revision 1 — 2026-09-19 (repo analysis)

Engineering repo had decided M365-native production; Azure dashboard superseded. Interim recommendation was **A′** (Power App on Lists). See [engineering-repo-analysis.md](../engineering-repo-analysis.md).

## Revision 2 — 2026-09-19 (after Hub use test) — CURRENT

James ran a dummy L10 on the live SharePoint EOS Hub and shared the site with the team. Result: **in-meeting Lists UX feels like a fudge**; **zero LT engagement**; Hub feels too close to OneNote/Loop/Planner. The never-fully-tested CEOS/Azure dashboard is judged more effective for L10.

**A′ is withdrawn.** Full write-up: [decision-revision-sharepoint-rejected.md](../decision-revision-sharepoint-rejected.md).

### Current recommendation

- **C′ (recommended):** Revive **CEOS/Azure Leadership L10 dashboard** as the meeting console. Update the ProDrive-EOS Decision Register. Bake off with two L10s before full SSOT cutover. Keep Azure/M365/Copilot hosting; **do not** use SharePoint Lists as the in-meeting board.
- **A′′:** Power App-only L10 room mode (no raw Lists) as a competing bake-off.
- **B′:** Keep Hub Lists (rejected by this test).
- **D:** Pause build; coach-led process only.

| Name | Role | Decision (C′/A′′/B′/D) | Approve scope lock? | Date |
|------|------|-------------------------|---------------------|------|
| James | Integrator | C′ (proposed) | | 2026-09-19 |
| Bruce | MD / Visionary | | | |
| Matt | Management | | | |

**Recommendation:** Choose **C′**, update the Decision Register in ProDrive-EOS, and schedule the dashboard bake-off against the same outcome metrics (five consecutive pure L10s; Friday prep under 20 minutes).

