# EOS Operating Dashboard — Roadmap

**Last updated:** 2026-09-19  
**Owner:** James Stock (Integrator)  
**Hard calendar anchor:** Focus Day with Rob Liddiard (Mission Group) — **1 October 2026**  
**Decision path:** C′ (CEOS/Azure L10 board) — Bruce + Matt sign-off still open

---

## One sentence

Get Leadership running pure EOS L10s on the CEOS dashboard; use Rob’s Focus Day for Vision/Rocks/seats — not as a substitute for the L10 board.

---

## Calendar (now → Focus Day)

| Date | What | Product role |
|------|------|----------------|
| **Now – 30 Sep** | Sign C′; run **2 L10 bake-offs** on CEOS dashboard (localhost or Azure if provisioned) | Prove meeting UX before Rob arrives |
| **Mon 22 Sep / Mon 29 Sep** | Likely Leadership L10 slots before Focus Day | Prefer these as bake-off #1 and #2 |
| **1 Oct 2026** | **Focus Day — first session with Rob Liddiard** | Process/Vision day with implementer. Dashboard is a *support surface* if ready; Focus Day agenda is Rob’s, not a product demo |
| **After 1 Oct** | Weekly L10s toward **5 consecutive pure-EOS** | Dashboard is the board; Rob holds fidelity |

---

## Phases

### Now (before 1 Oct) — bake-off gate

**Done**
- Decision Register on ProDrive-EOS `main` (C′ meeting UX)
- Phase 0 host on `main` (local server + Azure IaC)

**Must finish before Focus Day**
1. Bruce + Matt **sign C′** (written on 1-pager / decision note)
2. **Two facilitated L10s** on the CEOS dashboard (share-screen in Teams) — success bar from 1-pager
3. Optional but useful: Azure host + Easy Auth if James can `az login` on work PC

**Kill / pause rules**
- If Bruce remixed the agenda off-screen in both bake-offs → do not expand eng; fix facilitation + Rob contract first
- If Friday prep stays >20 min → fix Scorecard feed path before API work
- If Bruce/Matt refuse C′ → stop dashboard build; run Focus Day on paper/Rob’s template only

**Not required for Focus Day**
- Azure production cutover / `eos.prodriveit.co.uk`
- API / dual-write elimination beyond “one writable store in the meeting”
- Matt async updates, department Traction, AI

### Next (1 Oct Focus Day)

| In scope for the day | Out of scope for the day |
|----------------------|---------------------------|
| Rob-led Focus Day (V/TO, seats, Rocks as he runs it) | Declaring dashboard SSOT cutover |
| James as Integrator; Bruce Visionary; Matt present | Building Power App / Lists-as-board |
| Optional: open CEOS dashboard if bake-off already passed | Treating Focus Day as the product bake-off |

**Position:** Focus Day validates **re-adoption with an implementer**. It does **not** validate C′. Do not conflate “good day with Rob” with “Lists or dashboard won.”

### Later (after Focus Day → five L10s)

1. Weekly L10s on CEOS dashboard until **5 consecutive pure-EOS**
2. Provision Azure Easy Auth host when ready (same UI)
3. Only then: API / production meeting SSOT cutover (historical brief in git)
4. **v1.1:** Matt 2-minute async Scorecard/Rock updates

### Not now

- Department Traction portals
- Focus Day *product* features
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
