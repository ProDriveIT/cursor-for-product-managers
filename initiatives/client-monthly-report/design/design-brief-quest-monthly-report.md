# Design brief: Quest monthly service report

**Feature:** quest-monthly-report  
**Date:** 2026-09-28  
**Status:** Minimal brief. Chrome is already settled. Tokens are proposed because the August HTML sample was not in the repo.  
**Pair:** [design-brief-quest-monthly-report.json](./design-brief-quest-monthly-report.json)  
**Spec:** [prd-monthly-client-service-report.md](../prd/prd-monthly-client-service-report.md)

## Purpose and audience

One printed page (or a short scroll) that tells a Quest reader what Pro Drive did in a calendar month. Primary reader: the Quest economic buyer, on a PDF or a shared HTML file, not inside a product UI. Secondary: Bruce, in the Review folder, checking tiles before he sends. Ops does not use this layout; ops uses the run summary and the folder.

## Tone and brand voice

Brand: Pro Drive. Locale: en-GB. Voice: plain, specific, calm. The page states what happened and what decision is next.

**Do**

- Lead with counts and percents, then a short explanation.
- Use the three card labels Done, In effect, and Next.
- Leave a date off the page when the calendar source has none.

**Don't**

- Don't print ticket IDs, end-user names, or a title dump.
- Don't use a second visual system per client.
- Don't colour a red/green SLA with no percent in text.
- Don't fill a quiet month with praise.

## Design variables (tokens)

No `design-system/` folder exists in this workspace. Tokens below are **proposed** until someone opens `Quest-August-2026-service-report.html` and replaces them with the sample’s real values. Do not restyle the sample to match this table.

| Token | Proposed value | Role |
|-------|----------------|------|
| `color.paper` | `#ffffff` | Page background |
| `color.ink` | `#1a1a1a` | Body text |
| `color.ink.muted` | `#4a4a4a` | Footer, labels |
| `color.rule` | `#d0d0d0` | Dividers |
| `color.tile` | `#f4f6f8` | Metric tile fill |
| `font.family` | Calibri, Arial, sans-serif | Print-safe stack until the sample says otherwise |
| `font.size.body` | 11pt | Body |
| `font.size.section` | 14pt | Section headings |
| `font.size.tile` | 20pt | The figure |
| `space.page` | 18mm | Page margin |
| `space.stack` | 12px | Space between sections |

## Component library mapping

Nothing in a shared library to map. These are report regions, all **proposed** as names for the template, not new app components.

| Region | Required content | Interaction |
|--------|------------------|-------------|
| Report header | Pro Drive, client name, month, prepared for (or omit), account manager | None |
| Metric tiles | Ticket count, incidents, hours, first-response SLA %, resolution SLA % | None. Text always includes the number |
| Executive summary | Short prose grounded in the tiles | Bruce may edit in Review |
| What we did | Bullets from titles, rewritten, no IDs | Bruce may edit |
| Insight cards | 0 to 3. Labels: Done, In effect, Next | Bruce may edit. Drafter must not add a fourth |
| Across wider base | Bullets from PD Client Wide and/or Pro Drive statements, or one plain line if empty | Bruce may edit |
| Looking ahead | Omitted on the first Quest cycle unless decision B is signed | If present, date comes from Meeting Tracker / LCI only |
| Footer | Issued date, confidential line if the sample has one | None |

## Patterns and flows

1. Reader flow: header, tiles, summary, what we did, cards, wider base, footer. One sitting.
2. Bruce flow: open `Review/`, compare four or five figures to `facts.json`, edit cards, mark Approved, send.
3. Empty states: missing SLA field shows the words “not in this export”, not a dash that looks like zero. Empty wider-base shows one sentence. Missing looking-ahead section is absent, not “TBC”.

## Channel notes

- **Prototype / file:** HTML first, PDF for the send, matching the Quest sample path. No social, no ads.
- **Email (later):** the PDF or a link. Out of this cycle.

## Accessibility and language

- Contrast: body ink on white at WCAG 2.2 AA (proposed `#1a1a1a` on `#ffffff` passes).
- Headings are real headings: Executive summary, What we did, Insights, Across wider base.
- SLA meaning is the percent in text.
- Language: English (UK). No RTL requirement.
- Touch targets do not apply to a PDF. If an HTML review screen adds buttons later, those controls are at least 44px. This brief does not add those buttons.

## Naming and files

- Template stays one file, not per client.
- Output: `Monthly Packs/{Client}/{yyyy-MM}/Review/` then an Approved location still to be chosen.
- Facts sit beside the month folder as `facts.json`.

## Success metrics

- Bruce’s observed review: 15 minutes or less, 0 tile corrections.
- Buyer recall: 2 non-break-fix items.
- Visual experiment: none. The Quest sample is the control. A redesign is a fail.

## Assets

- Find and attach `Quest-August-2026-service-report.html` and the PDF. Until that file is linked here, do not generate a new visual.
