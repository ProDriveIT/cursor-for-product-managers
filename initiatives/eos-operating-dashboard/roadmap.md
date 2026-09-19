# EOS Operating Dashboard — Roadmap

**Last updated:** 2026-09-19  
**Owner:** James Stock (Integrator)  
**Hard calendar anchor:** Focus Day with Rob Liddiard (Mission Group) — **1 October 2026**  
**Decision path:** C′ (CEOS/Azure L10 board) — Bruce + Matt sign-off still open

---

## One sentence

Phase 1 is the **Leadership L10 board only** (Issues, Rocks, To-Dos, KPIs/Scorecard). Focus Day stays Rob’s — **no dashboard**.

---

## Scope lock (Phase 1)

| In | Out |
|----|-----|
| L10 shared-screen board: Issues, Rocks, To-Dos, KPIs/Scorecard | Focus Day / quarterly meeting product |
| Fixed pure-EOS L10 agenda | Vision/V/TO tooling as a product surface |
| One writable meeting store for bake-off | Hub Lists as the L10 board |
| Azure host when ready (same L10 UI) | Department Traction, AI chase, Matt async (until L10 proves) |

**Later assessment only:** if there is clear value, consider dashboard for quarterly / Focus Day-style sessions — not Phase 1.

---

## Calendar (now → Focus Day)

| Date | What | Product role |
|------|------|----------------|
| **Now – 30 Sep** | Sign C′; run **2 L10 bake-offs** on CEOS dashboard (localhost or Azure if provisioned) | Prove L10 UX — independent of Focus Day |
| **Mon 22 Sep / Mon 29 Sep** | Likely Leadership L10 slots | Prefer these as bake-off #1 and #2 |
| **1 Oct 2026** | **Focus Day — first session with Rob Liddiard** | **No dashboard.** Rob runs the day as he wishes (paper / his templates / whatever he uses) |
| **After 1 Oct** | Weekly L10s toward **5 consecutive pure-EOS** | Dashboard is the L10 board only; Rob holds process fidelity |

---

## Phases

### Now — L10 bake-off gate

**Done**
- Decision Register on ProDrive-EOS `main` (C′ meeting UX)
- Phase 0 host on `main` (local server + Azure IaC)

**Must do (does not block Focus Day)**
1. Bruce + Matt **sign C′** (written on 1-pager / decision note)
2. **Two facilitated L10s** on the CEOS dashboard (share-screen in Teams)
3. Optional: Azure host + Easy Auth if James can `az login` on work PC

**Kill / pause rules**
- If Bruce remixed the agenda off-screen in both bake-offs → do not expand eng; fix facilitation + Rob contract first
- If Friday prep stays >20 min → fix Scorecard feed path before API work
- If Bruce/Matt refuse C′ → stop dashboard build; keep L10s on whatever interim surface James can run

### 1 Oct Focus Day — off product

| In scope | Out of scope |
|----------|----------------|
| Rob-led Focus Day, his method | Any CEOS/Azure dashboard use |
| James Integrator; Bruce Visionary; Matt present | Product demo, bake-off, or SSOT cutover |
| Process / Vision / seats as Rob frames them | Building Focus Day or quarterly meeting features |

**Position:** Focus Day is implementer-led re-adoption. Phase 1 product proof is **L10 only**. Do not put the dashboard in the room on 1 Oct.

### Later (after bake-off + toward five L10s)

1. Weekly L10s on CEOS dashboard until **5 consecutive pure-EOS**
2. Provision Azure Easy Auth host when ready (same L10 UI)
3. Only then: API / production meeting SSOT cutover (historical brief in git)
4. **v1.1:** Matt 2-minute async Scorecard/Rock updates
5. **Assess later (not committed):** dashboard for quarterly / Focus Day-style sessions — only if LT asks and L10 habit is solid

### Not now

- Dashboard on Focus Day or quarterly sessions
- Focus Day / V/TO product features
- Department Traction portals
- AI chase / agents on EOS data
- Bruce customization sandbox
- Client monthly reports (separate initiative)
- Third-party EOS SaaS (Ninety etc.)

---

## Success metrics (unchanged)

| Metric | Target |
|--------|--------|
| Pure-EOS Leadership L10s | 5 consecutive |
| James Friday prep | &lt; 20 minutes |
| Bruce / Matt | Participate without GitHub knowledge |
| Writable meeting store | One during bake-off (no dual-write) |

---

## Owners

| Work | Owner |
|------|--------|
| C′ sign-off | James drives; Bruce + Matt decide |
| Bake-off L10s | James facilitates; Bruce + Matt in room |
| Azure provision | James (`az login` on work PC) |
| Focus Day 1 Oct | Rob Liddiard leads; James Integrator |
| Roadmap / Decision Register | James |

---

## Related

- [1-pager](./prd/1-pager-eos-operating-dashboard.md)
- [Decision revision](./decision-revision-sharepoint-rejected.md)
- [Bake-off runbook](https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/blob/main/prodrive/deployment/Dashboard-Bakeoff-Runbook.md)
