# Riskiest assumptions — Self-Service Travel

**Owner:** James Stock  
**Target:** ≥2 tagged, each with ≤14-day falsification test (PRISM core #2)  
**Filled on:** TBD (sprint day)  
**Rule:** Replace starter wording with evidence-backed claims after signals/baseline exist.

---

## A1 — Desirability

**Assumption:** MSP Org operators will change weekly behavior if they get central status reporting (planned / actioned / ended / failed).  
**Tag:** desirability  
**Why riskiest:** Reporting is the loudest ask; interest ≠ demand.  
**Falsify by (≤14 days):** Name one operator; observe current weekly ritual; if they already cope via ticket search/chat and refuse a 15-min reporting pilot, kill or shrink reporting.  
**Test design:** TBD on sprint day  
**Result:** TBD

---

## A2 — Viability

**Assumption:** Other clients will adopt if deploy drops to near one-click; **deployment friction is the binding constraint**, not trust, process, or training.  
**Tag:** viability  
**Why riskiest:** One-click is expensive; wrong bottleneck wastes the bet.  
**Falsify by (≤14 days):** Interview / shadow one non-live client path; if go-live blockers are policy/trust/training > deploy steps, deprioritize one-click.  
**Test design:** TBD on sprint day  
**Result:** TBD

---

## A3 — Feasibility / sequencing (partially decided)

**Assumption:** SST discovery and build can wait until after EOS L10-ready and one-client HTML reports without material revenue or ops damage.  
**Tag:** feasibility  
**Status:** **Accepted as working decision** via product work order (2026-09-19). Revisit only with a written reordering decision.  
**Falsify by:** Documented MD/board mandate or measurable ops failure attributable to delayed SST multi-client work.  
**Citation:** [`../../company-level-context/product-vision-and-strategy/product-work-order.md`](../../company-level-context/product-vision-and-strategy/product-work-order.md)

---

## Minimum for gate

Keep A1 + A2 (or replacements) with completed test designs on sprint day. A3 is sequencing, not a substitute for A1/A2.
