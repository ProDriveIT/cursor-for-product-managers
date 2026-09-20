# Design brief — Leadership L10 console

**Status:** Shipped 20 Sep 2026  
**URL:** https://eos.prodriveit.co.uk  
**Brand:** Pro Drive 2026 (Electric Green, Core Black, Clear White, Dark Grey, TikTok Sans)

This is the as-shipped board, not a future mock.

## Purpose and audience

James shares this screen in the Monday L10. Bruce and Matt use it in the room. They should never need GitHub.

The board holds Scorecard, Rocks, Issues, To-Dos, and the 90-minute L10 agenda. One writable store: Azure `state.json`.

## Tone

EOS words only. Short labels. No “bake-off pack” line. No slogan under the title.

## Tokens

| Role | Value |
|------|--------|
| Accent | `#B1FF53` |
| Banner | `#000000` |
| Page | `#FFFFFF` |
| Panel on black | `#0F0F0F` |
| Type | TikTok Sans, then system-ui |
| Card radius | 8px |

Green is the banner accent and the wordmark. Body copy stays black on white. Red and green on Scorecard mean miss and hit, not brand colour.

## What is on screen

| Surface | Rule |
|---------|------|
| Banner | Black bar, green/white logo, “EOS Leadership Dashboard · 2026-Q3” |
| Tabs | Rocks, Scorecard, Issues, To-Dos, L10, Accountability, V/TO, Calendar |
| Scorecard | One `table-fixed` grid. Department names are header rows. Eight KPIs only |
| Owner chips | James blue, Matt purple, Bruce green |
| Rocks | Q3 cards. Edit milestones in a textarea; save must survive refresh |
| L10 | Seven-section agenda, 90-minute clock, Add to Issues on a red KPI |

## Meeting flow

1. Sign in as `James.Stock@prodriveit.co.uk` (not `admin-jstock`).
2. Open the L10 tab. Start the clock.
3. Run Segue → Scorecard → Rocks → Headlines → To-Dos → IDS → Conclude.
4. Stay on this URL. Do not open Lists.

## Accessibility

White body meets AA for black text. Banner type is white or green on black. Meeting use is a shared desktop screen; 44px targets on Edit / Save / Add to Issues.

## Success

Monday 22 Sep runs on this URL. Edits stay after refresh. Bruce and Matt do not touch GitHub. Five consecutive pure L10s remains the product bar.
