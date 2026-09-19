# Client monthly report — canonical path (SSOT)

**Decision date:** 2026-09-19  
**Vault twin:** [ProDriveIT/GitHub-Repos — 00 Meta/Client-Monthly-Report-Canonical-Path.md](https://github.com/ProDriveIT/GitHub-Repos/blob/main/00%20Meta/Client-Monthly-Report-Canonical-Path.md)

## Canonical delivery path (only)

```text
Autotask → Azure Insights client packs (reporting-kpi-automation)
        → Copilot Reporting Agent (agent-ecosystem-copilot)
        → vCIO approve
        → human-gated send
```

| Layer | Location | Role |
|-------|----------|------|
| Numbers / HTML packs | [GitHub-Repos `reporting-kpi-automation`](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-01%20reporting-kpi-automation) | Produce `client-pack-*.html` |
| Draft + sign-off | [GitHub-Repos `agent-ecosystem-copilot`](https://github.com/ProDriveIT/GitHub-Repos/tree/main/10%20Projects/2026-09%20agent-ecosystem-copilot) | Reporting Agent; draft ≠ send |
| Product / pilot | This initiative | Quest pilot; Bruce vCIO; Danny TAM; James ops |
| Meeting footer (Phase 2) | Meeting calendar | Next **vCIO** and **TAM** meetings |

## Dead / do not resume

| Path | Status | Agent rule |
|------|--------|------------|
| [GitHub-Repos `90 Archive/2026-01 reporting-client`](https://github.com/ProDriveIT/GitHub-Repos/tree/main/90%20Archive/2026-01%20reporting-client) | **Superseded** | Do not continue, extend, revive, or restore to `10 Projects` |
| `Generate-ClientValueAddReport.ps1` + launch `.bat`s | **Superseded** | Do not run, copy, or rebuild |

## Alive but not this product

Internal KPI scorecards, engineer HTML reports, and EHAN / KPI Analysis Assistant are **internal numbers** surfaces — not the client monthly proof-of-value report.

## Related

- [1-pager](./prd/1-pager-client-monthly-report.md)
- [Prior art inventory](./prior-art-github-repos.md)
