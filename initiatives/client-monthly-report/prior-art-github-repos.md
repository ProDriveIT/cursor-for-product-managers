# Prior art — GitHub-Repos & related

**Last reviewed:** 2026-09-19  
**Source vault:** [ProDriveIT/GitHub-Repos](https://github.com/ProDriveIT/GitHub-Repos)

This initiative is **not greenfield**. Multiple starts already exist. Use them; do not rebuild KPI math or invent a second HTML generator.

## Starts (chronological)

| When | Path in GitHub-Repos | Status | What it is |
|------|------------------------|--------|------------|
| 2026-01 | [`90 Archive/2026-01 reporting-client`](https://github.com/ProDriveIT/GitHub-Repos/tree/main/90%20Archive/2026-01%20reporting-client) | **SUPERSEDED 19-09-2026 — DO NOT RESUME** | First client “value-add” HTML generator (`Generate-ClientValueAddReport.ps1`). Archived Aug 2026 (RTEM STOP); superseded by Insights packs + Reporting Agent. |
| 2026-01 (ongoing) | [`10 Projects/2026-01 reporting-kpi-automation`](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-01%20reporting-kpi-automation) | **Active** | Azure KPI / Insights spine. **WIP-027** [`Monthly-Client-Service-Report.md`](https://github.com/ProDriveIT/GitHub-Repos/blob/main/10%20Projects/2026-01%20reporting-kpi-automation/Documentation/Monthly-Client-Service-Report.md) — branded `client-pack-{runId}.html` per account/month (preventative vs end-user, jobs, alignment). Human review before send. |
| 2026-09 | [`10 Projects/2026-09 agent-ecosystem-copilot`](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-09%20agent-ecosystem-copilot) | **Active** (docs / build guides) | **Reporting Agent** — Copilot drafts monthly HTML from Insights packs → **vCIO sign-off** → send. Phase 2 adds vCIO narrative list + next **vCIO and TAM meeting** dates. First Copilot vertical slice by design. |

## Locked product decisions (from agent-ecosystem pack)

Do not reopen these without evidence:

- Artefact: **HTML**
- Operator / sign-off: that client’s **vCIO** (not auto-send)
- Numbers: from Azure Insights **client packs** only — agents never invent metrics
- Narrative half: SharePoint list, vCIO-authored (“This month Pro Drive have worked on…”)
- Meeting footer: calendar spreadsheet — next **vCIO meeting** + next **TAM meeting** (product language; some GitHub-Repos build guides still say “town meeting”)
- Builder: James; product owner: vCIO practice
- External **reports repo** exists for HTML templates / assembly (attach in multi-root workspace)

Primary briefs:

- [Reporting-Agent-Brief.md](https://github.com/ProDriveIT/GitHub-Repos/blob/main/10%20Projects/2026-09%20agent-ecosystem-copilot/03-briefs/Reporting-Agent-Brief.md)
- [Roadmap.md](https://github.com/ProDriveIT/GitHub-Repos/blob/main/10%20Projects/2026-09%20agent-ecosystem-copilot/01-roadmap/Roadmap.md)
- [SharePoint-VCIO-Narrative-List.md](https://github.com/ProDriveIT/GitHub-Repos/blob/main/10%20Projects/2026-09%20agent-ecosystem-copilot/04-build-guides/SharePoint-VCIO-Narrative-List.md)
- [Meeting-Calendar-Spreadsheet.md](https://github.com/ProDriveIT/GitHub-Repos/blob/main/10%20Projects/2026-09%20agent-ecosystem-copilot/04-build-guides/Meeting-Calendar-Spreadsheet.md)

## How this PM initiative should relate

| This folder (`cursor-for-product-managers`) | Engineering / ops (GitHub-Repos + reports repo) |
|--------------------------------------------|--------------------------------------------------|
| Problem framing, discovery, PRD/1-pager, measurement, stakeholder narrative | Pack generation, Copilot Reporting Agent, SharePoint lists, send workflow |

**Recommendation:** Treat **Reporting Agent Phase 1–2** as the delivery path. Pull reusable ideas from superseded `reporting-client` (category taxonomy, “value you can’t see” framing) into the narrative/pack design — do not revive the PowerShell launcher.

**Agent hygiene (done 19-09-2026 in GitHub-Repos):** SSOT note in `00 Meta/`; `reporting-client` ARCHIVE/AGENTS/cursorkleosr marked DO NOT RESUME; live `AGENTS.md` walls; vault Cursor rule + `superseded` convention; Azure ValueAdd errata.

## Open reconciliation items

1. Confirm path/name of the **external reports repo** and link it here.
2. ~~Pilot client + named pilot **vCIO**~~ — **Locked:** Quest Fund Placement · Bruce Penson (vCIO) · Danny Bray (TAM) · James Stock (ops). See [1-pager](./prd/1-pager-client-monthly-report.md).
3. ~~Prevent agent drift into dead starts~~ — **Done 19-09-2026** in GitHub-Repos (superseded + SSOT + AGENTS walls). Twin: [canonical-path.md](./canonical-path.md).
4. Capture Quest economic-buyer reaction after first approved cycle (demand evidence still company-wide, not Quest-specific).
5. Confirm Quest Insights pack exists for the chosen `YYYY-MM` before calling Phase 1 live.
