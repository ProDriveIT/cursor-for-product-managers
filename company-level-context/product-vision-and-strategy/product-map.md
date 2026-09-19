# Pro Drive — Product Map

**Status:** Working map + coherence assessment  
**Last updated:** 2026-09-19  
**Owner:** James Stock  
**Company context:** [`../prodrive-context.md`](../prodrive-context.md)

Three product goals (James, 2026-09-19):

| # | Goal | Success looks like |
|---|------|--------------------|
| **A** | Reduce **RTEM** | Fewer reactive tickets / hours from preventable M365, identity, SharePoint, and access chaos |
| **B** | Sell these as **services** to existing clients | Named SKUs / SOWs under Pro Drive 360 (Audit → Roadmap → Align → Enforce); billable PS + recurring attach |
| **C** | Longer term — sell **outside** the managed-client base | Standalone product or partner-delivered offering with buyers who are not already MSP clients |

This map classifies every current initiative against those goals. Scores are **High / Med / Low / None** for contribution to A/B/C — not ICE, not roadmap priority.

---

## 1. Verdict (coherence)

**The portfolio is not yet a clear product offering.** It is three overlapping piles:

1. **Internal operating system** — EOS dashboard, Performance Hub, EHAN/Facilitator  
2. **Client M365 / SharePoint / identity tooling** — Standardiser, Archiver, SPAT, Travel, CE Mobile, Inforcer  
3. **Vertical / narrative products** — MSP Meeting Minutes, Client Monthly Report  

Piles 2 and 3 can become a sellable line. Pile 1 must stay — but it is **not** the commercial product line, and mixing it in the same “products” conversation confuses Bruce, Matt, and buyers.

**What will work:** Treat **M365 Estate Control** (Standardiser + Archiver + SPAT + Travel + Inforcer + CE Mobile) as one commercial family aimed at goals A and B, with **Standardiser as the spine** (design → audit → align → enforce). Sell **Minutes** and **Monthly Report** as attach / proof-of-value, not as the core catalogue.

**What will not work:** Marketing ten separate “products” externally, or claiming every tool reduces RTEM. EOS and Performance Hub do not sell. Directory Group Review and half-built tooling dilute clarity until they join a family or die.

Evidence that would change this verdict: a named buyer (not James) already paying for a multi-tool “estate package,” or Autotask data showing Travel/Minutes as top RTEM killers vs SharePoint sprawl.

---

## 2. Product map (by commercial family)

```text
                    PRO DRIVE COMMERCIAL OFFERING
 ┌─────────────────────────────────────────────────────────────────┐
 │  Pro Drive 360 (MSP delivery)                                   │
 │  Audit → Roadmap → Align → Enforce                              │
 └─────────────────────────────────────────────────────────────────┘
                │
    ┌───────────┼───────────────────────────┐
    ▼           ▼                           ▼
┌────────┐ ┌────────────────────┐  ┌──────────────────┐
│ A+B    │ │ B attach / proof   │  │ Internal only    │
│ Estate │ │ of proactive value │  │ (not SKUs)       │
│ Control│ │                    │  │                  │
└────────┘ └────────────────────┘  └──────────────────┘
    │              │                        │
    │              ├ Monthly Report         ├ EOS Dashboard
    │              └ (Reporting Agent)      ├ Performance Hub
    │                                       └ Facilitator / EHAN
    ├ ★ SharePoint Standardiser  ← spine
    ├ SharePoint Archiver
    ├ SPAT
    ├ Self-Service Travel
    ├ Inforcer Alignment
    └ CE Mobile Status

Specialist vertical (B now → C later):
    └ MSP Meeting Minutes (CoSec / board minutes)
```

★ = core product you just elevated; design-driven audit is the natural **Align** step that makes Archiver / SPAT / Inforcer coherent instead of a toolkit pile.

---

## 3. Scorecard vs goals A / B / C

| Product | Family | Maturity | **A RTEM** | **B Services** | **C External** | One-line job |
|---------|--------|----------|------------|----------------|----------------|--------------|
| **SharePoint Standardiser** | Estate Control | Phase 0 → core | **High** | **High** | Med | Measure estate vs declarative design; drive alignment programmes |
| SharePoint Archiver | Estate Control | Operational | **High** | **High** | Med | Fix OneDrive 300k / cold data without chaos |
| SPAT | Estate Control | Live | **Med** | **High** | Med | IT Contact “who can open this?” without desk tickets |
| Self-Service Travel | Estate Control | Live | **Med–High** | **High** | **High** | Time-boxed geo access without helpdesk CA gymnastics |
| Inforcer Alignment | Estate Control | Live (internal UI) | **High** | **High** | Low–Med | Baseline Entra/Intune/M365 alignment (Enforce) |
| CE Mobile Status | Estate Control | Live | **Med** | Med | Low | Phone readiness gate before CE work |
| Client Monthly Report | Proof / attach | Planning | Low* | **High** | Low | Make proactive work visible when tickets drop |
| MSP Meeting Minutes | Vertical | Live · freeze | Low | **High** (niche) | **High** | Board minutes from audio + pack |
| EOS Operating Dashboard | Internal OS | Priority #1 | None | None | None | Leadership L10 fidelity |
| PD Performance Hub | Internal OS | Unclear | None | None | None | Manager KPI / BreatheHR reviews |
| Directory Group Review | Below bar | Local tool | Med | Low | Low | HTML group membership review |
| Agent Ops / CIPP | Platform | Infra | — | — | — | Enable products; not sold |

\*Monthly Report does not reduce RTEM; it **defends the commercial outcome of reduced RTEM** (goal B retention / expansion). Do not score it as an RTEM tool.

---

## 4. Clarity assessment

| Question | Assessment |
|----------|------------|
| Can Bruce recite the product line in one breath? | **No today.** Tool names (SPAT, CE Mobile, Agent Ops) are engineer vocabulary. |
| Does a buyer know where Standardiser ends and Archiver/SPAT begin? | **Not yet.** Without Standardiser as spine, they look like unrelated PS jobs. |
| Is work-order #1–#3 aligned to A/B/C? | **Partially.** #1 is internal OS (necessary, not commercial). #2 serves B (proof). #3 serves A+B+C. Estate Control (incl. Standardiser) is under-weighted in the locked order relative to goal A. |
| Single SKU vs kit? | **Recommend kit:** “M365 Estate Control” engagement = Standardiser audit + optional Archiver / SPAT / Travel / Inforcer modules. Minutes sold separately to CoSec-like buyers. |

**Clarity fix (recommended naming for clients):**

| Internal name | Client-facing name (draft) |
|---------------|----------------------------|
| SharePoint Standardiser | **Estate Design & Alignment** |
| SharePoint Archiver | **SharePoint Sync & Archive** |
| SPAT | **SharePoint Access Picture** |
| Self-Service Travel | **Travel Access** (already used) |
| Inforcer Alignment | **Security Baseline Alignment** |
| CE Mobile Status | **Teams Phone Readiness** |
| Client Monthly Report | **Monthly Value Report** |
| MSP Meeting Minutes | **Board Minutes Assistant** |

---

## 5. Coherence assessment (will this become one offering?)

### What coheres

- **Estate Control family** shares: Agent Ops (or Travel) identity, client registry pattern, M365 tenant scope, Pro Drive 360 Align/Enforce, and a direct path to fewer access/SharePoint/identity tickets (**A**) plus billable PS (**B**).
- **Standardiser as spine** is the right call: declarative `design.json` → audit gap → programme of work that can attach Archiver, SPAT, and Inforcer without inventing a new story each time.
- **Travel** is the best near-term **C** candidate already live with non-MSP-shaped packaging (portal URL, guides, enrol script).
- **Minutes** is coherent as a **vertical** (CoSec), not as Estate Control — keep it separate so it does not warp the M365 story.

### What breaks coherence

1. **Calling EOS / Performance Hub / EHAN “products” in the same catalogue** — buyers do not care; LT should not either when discussing SKUs.  
2. **Ten parallel initiatives without a family owner** — capacity will keep shipping islands; RTEM will not move as a system metric.  
3. **Selling C before B is productised** — external sales need packaging, support, pricing, and a buyer who is not already on Autotask. Travel is closest; Standardiser is not ready for C until provisioning + support model exist.  
4. **Monthly Report as a “product” without Estate Control outcomes to report** — risk of a pretty HTML that still cannot answer “what did you do?” if Align/Enforce work is invisible.

### Forced ranking for goals (recommendation)

| Goal | Put weight on | Defer / ring-fence |
|------|---------------|-------------------|
| **A RTEM** | Standardiser, Archiver, Inforcer, SPAT, Travel | EOS (internal), Minutes (niche RTEM), Monthly Report (narrative) |
| **B Services** | Package Estate Control as SOW modules; Monthly Report as retain/expand proof; Minutes as CoSec SKU | Performance Hub; Directory Group Review |
| **C External** | Travel first (live + packagable); Minutes second (niche but productised); Estate Control only after repeatable enrol + support | Everything that still needs James on every client |

---

## 6. Implications for the locked work order

The locked order (#1 EOS → #2 Monthly Report → #3 Travel) optimises **internal rhythm + proof + one C candidate**. It does **not** yet optimise goal **A**.

**Recommendation (you decide):** Keep #1–#3 as capacity truth for the next few weeks, but add a parallel **Estate Control** track owned as one product family — with **SharePoint Standardiser** as the named core — so Align work is not indefinitely “below the bar.” Do not open a fourth deep build stream that displaces L10 readiness unless RTEM is red and LT writes that reorder down.

What would change my mind: Scorecard shows RTEM already ≤0.50 and stuck on commercial proof only — then #2/#3 correctly outrank Estate Control build.

---

## 7. Initiative index

| Family | Initiative folder |
|--------|-------------------|
| Estate Control | [`sharepoint-standardiser`](../../initiatives/sharepoint-standardiser/), [`sharepoint-archiver`](../../initiatives/sharepoint-archiver/), [`sharepoint-permissions-audit`](../../initiatives/sharepoint-permissions-audit/), [`self-service-travel`](../../initiatives/self-service-travel/), [`inforcer-alignment-portal`](../../initiatives/inforcer-alignment-portal/), [`ce-mobile-status`](../../initiatives/ce-mobile-status/) |
| Proof / attach | [`client-monthly-report`](../../initiatives/client-monthly-report/) |
| Vertical | [`msp-meeting-minutes`](../../initiatives/msp-meeting-minutes/) |
| Internal OS | [`eos-operating-dashboard`](../../initiatives/eos-operating-dashboard/), [`pd-performance-hub`](../../initiatives/pd-performance-hub/) |

---

## 8. Open decisions for James

1. Approve **Estate Control** as the client-facing family name (or pick better).  
2. Confirm Standardiser as **spine** of that family (this map assumes yes).  
3. Keep Minutes as vertical SKU, not inside Estate Control.  
4. Whether to amend work order to give Estate Control / Standardiser explicit capacity after #1, or only via PS delivery on client projects.  
5. One RTEM metric definition tied to this family (which Autotask categories / queues count).
