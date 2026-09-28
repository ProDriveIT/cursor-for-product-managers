# EOS Operating Dashboard — Roadmap

**Last updated:** 2026-09-21  
**Owner:** James Stock (Integrator)  
**Live board:** https://eos.prodriveit.co.uk  
**Hard calendar anchor:** Focus Day with Rob Liddiard (Mission Group) — **1 October 2026**  
**Decision path:** C′ (CEOS/Azure L10 board) — decided by James 19 Sep 2026. Board is live. Bruce + Matt sign the product after 3 live L10s.

---

## One sentence

Phase 1 is the **Leadership L10 board only** (Issues, Rocks, To-Dos, KPIs/Scorecard). Focus Day stays Rob’s — **no dashboard**.

---

## Scope lock (Phase 1)

| In | Out |
|----|-----|
| L10 shared-screen board: Issues, Rocks, To-Dos, KPIs/Scorecard | Focus Day / quarterly meeting product |
| Fixed pure-EOS L10 agenda | Vision/V/TO tooling as a product surface |
| One writable meeting store (Azure `state.json`) | Hub Lists as the L10 board |
| Azure host `eos.prodriveit.co.uk` + Entra SSO | Department Traction, AI chase, Matt async (until L10 proves) |

**Later assessment only:** if there is clear value, consider dashboard for quarterly / Focus Day-style sessions — not Phase 1.

---

## Calendar (now → Focus Day)

| Date | What | Product role |
|------|------|----------------|
| **21 Sep 2026** | Leadership L10 #1 | **Done.** Board used in the room. Team agreed the approach; freeze further dashboard automation until Rob |
| **Mon 29 Sep** | Leadership L10 #2 | Still Q3 Rocks. Do not invent Q4 titles |
| **1 Oct 2026** | **Focus Day — Rob Liddiard** | **No dashboard.** Set Q4 Rocks. Plan lives in Supporting Data `50-eos/implementation/Q4-2026-Setting.md` |
| **Mon 6 Oct** | Leadership L10 #3 | First Monday after Focus Day. Load **agreed** Q4 Rocks. Bruce + Matt sign the product |
| **After 6 Oct** | Weekly L10s toward **5 consecutive pure-EOS** | Dashboard is the L10 board only; Rob holds process fidelity |

---

## Phases

### Now — first live L10s

**Done**
- Decision Register on ProDrive-EOS `main` (C′ meeting UX)
- Azure B1 host, Easy Auth, custom domain `eos.prodriveit.co.uk`
- Live meeting store (Azure JSON); eight KPIs; Q3 Rocks
- Design brief in [`design/`](./design/)
- **L10 #1 — 21 Sep 2026.** Team agreed the board. Automations frozen until Rob

**Must do (does not block Focus Day)**
1. **L10 #2 Mon 29 Sep** on the live URL (Q3 content)
2. **L10 #3 Mon 6 Oct** after Focus Day, with agreed Q4 Rocks; then Bruce + Matt **sign the product**

**After L10 #1 (not until Rob says the L10 method is good)**
- Issues: add **and remove** a Scorecard metric from the Issues list; L10 “Add to Issues / On Issues” follows that link
- Rocks: Add to Issues when a Rock is marked off track (EOS: drop it, don’t discuss in Rock Review)
- Planner / Todoist / KPI pull / transcripts

**Kill / pause rules**
- If Bruce remixed the agenda off-screen in the first two live L10s → do not expand eng; fix facilitation + Rob contract first
- If Friday prep stays >20 min → fix Scorecard feed path before more API work
- If Bruce/Matt refuse the product after 3 L10s → stop dashboard build; keep L10s on whatever interim surface James can run

### 1 Oct Focus Day — off product

| In scope | Out of scope |
|----------|----------------|
| Rob-led Focus Day, his method | Any CEOS/Azure dashboard use |
| James Integrator; Bruce Visionary; Matt present | Product demo or SSOT cutover talk |
| Process / Vision / seats as Rob frames them | Building Focus Day or quarterly meeting features |

**Position:** Focus Day is implementer-led re-adoption. Phase 1 product proof is **L10 only**. Do not put the dashboard in the room on 1 Oct.

### Later (after three live L10s + toward five)

1. Weekly L10s on `eos.prodriveit.co.uk` until **5 consecutive pure-EOS**
2. Azure host is already live; do not rebuild it
3. **v1.1:** Matt 2-minute async Scorecard/Rock updates
4. **Assess later (not committed):** dashboard for quarterly / Focus Day-style sessions — only if LT asks and L10 habit is solid

### Not now

- Dashboard on Focus Day or quarterly sessions
- Focus Day / V/TO product features
- Department Traction portals
- AI chase / agents on EOS data
- Bruce customization sandbox
- Client monthly reports (separate initiative)
- Third-party EOS SaaS (Ninety etc.)
- Autotask–HubSpot / Planner / Todoist until Rob validates the L10 method

---

## Success metrics (unchanged)

| Metric | Target |
|--------|--------|
| Pure-EOS Leadership L10s | 5 consecutive |
| James Friday prep | &lt; 20 minutes |
| Bruce / Matt | Participate without GitHub knowledge |
| Writable meeting store | Azure `state.json` only (no Lists dual-write) |

---

## Owners

| Work | Owner |
|------|--------|
| C′ path | James decided 19 Sep; Bruce + Matt sign the product after 3 L10s |
| Live L10s | James facilitates; Bruce + Matt in room |
| Azure host | Done — `eos.prodriveit.co.uk` |
| Focus Day 1 Oct | Rob Liddiard leads; James Integrator |
| Roadmap / Decision Register | James |

---

## Related

- [1-pager](./prd/1-pager-eos-operating-dashboard.md)
- [Decision revision](./decision-revision-sharepoint-rejected.md)
- [Design brief](./design/design-brief-leadership-l10-console.md)
- [L10 runbook](https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/blob/main/prodrive/deployment/Dashboard-Bakeoff-Runbook.md)
