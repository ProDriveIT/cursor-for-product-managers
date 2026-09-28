# Decision: facts contract in, drafter still unsigned

**Date:** 2026-09-28  
**Status:** Proposed. James decides. Canonical path is unchanged until this page is signed.  
**Source PRD:** `C:\Github-Repos\10 Projects\2026-01 reporting-kpi-automation\Documentation\PRD-Monthly-Client-Service-Report.md` (v0.1, draft for review, WIP-027)  
**Signed baseline:** [1-pager](./prd/1-pager-client-monthly-report.md) option A (James 19 Sep, Bruce 20 Sep) and [canonical path](./canonical-path.md) (19 Sep)

## What is already decided

Quest Fund Placement is the pilot. Bruce Penson is the operator and the send gate. Danny Bray owns TAM context. James Stock owns ops. The artefact is HTML a client can be shown. Numbers come from the Autotask Insights spine. Nothing sends without Bruce. Archived `reporting-client` stays dead. Work order #2 is one Quest HTML report Pro Drive will show externally.

## What the 28 Sep PRD changes

| Topic | Signed 19–20 Sep | PRD v0.1 (28 Sep) |
|-------|------------------|-------------------|
| Number handoff | Branded `client-pack-*.html` | `facts.json` per client month, tiles copied from that file |
| Who drafts prose | Copilot Reporting Agent | Microsoft 365 Copilot Cowork |
| Operator label | vCIO (Bruce) | Account manager (same person on Quest) |
| Looking ahead | Phase 2, after the first approved draft | MVP (F9), from Meeting Tracker / LCI |
| Layout | HTML pack | Settled Quest layout (one template) |

The outcome does not change. Quest’s buyer should be able to name proactive work when ticket volume is low. The argument is about the handoff and what sits in the first send.

## Recommendation

Accept the **facts contract**. Reject running **two drafters**. Keep **Looking ahead out of the first Quest send**.

1. **Facts.** `facts.json` is a stricter number lock than asking a model to read HTML. Azure still counts. Cowork or the Reporting Agent copies figures. This matches the signed rule that agents do not invent metrics.
2. **One drafter.** Cowork is the drafter named in the PRD. The Reporting Agent is the signed fallback if Cowork cannot read the KPI Insights library. Build one prompt path for the pilot. Do not staff both.
3. **Looking ahead stays Phase 2.** Bruce and James locked that out until a Bruce-approved draft exists. F9 pulls an unsigned Meeting Tracker path into the first cycle. Empty dates are honest; a wrong date in a client PDF is worse. Ship tiles, exec summary, What we did, and at most three insight cards first.

Evidence that would change this:

- Bruce says he will not send Quest a report that lacks next-meeting dates. Then F9 enters the first cycle, and the Meeting Tracker path has to be named before the prompt is written.
- A Cowork run on the real library fails governance. Then the Reporting Agent stays the drafter and still consumes `facts.json`, not a fresh HTML generator.
- Quest August facts cannot be made to match a manual count. Then Phase 1 stops, as the 1-pager already says.

## What stays unsigned

The eight questions at the end of PRD v0.1 are still open. Do not treat `Sergio`, folder-move approval, or a 1st-working-day schedule as decided. Company context and the canonical path still say Reporting Agent until this page is signed.

## Ask

| Name | Choice | Date |
|------|--------|------|
| James Stock | A. Accept this recommendation | |
| James Stock | B. Adopt the PRD as written, including Looking ahead in the first send and Cowork as the only drafter | |
| James Stock | C. Keep the 19 Sep canonical path (`client-pack` HTML + Reporting Agent) and treat PRD v0.1 as engineering notes only | |
