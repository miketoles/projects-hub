# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-25 (Website polish — spiritlogic.dev + stx-archery.com)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT Scatterplot V2 | 🟢 Spec complete, Phase 1 GO | Committee decisions on D1/D6, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟢 v1.0.9 built, docs current | Deploy installer to production users | Claude Code |
| STX Archery | 🟢 Sites polished, awaiting enrollment | GPS trail walk test, await Apple enrollment | Claude Code |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 | Codex |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** UX-P1 | **Status:** reviewing 🔍 — adversarial plan review sent to Codex
**Next agent:** codex
**Building:** V1 UX Polish Sprint — Settings cleanup, Score→Shoot rename, Gear keyboard fixes, Stats polish
**Baseline:** 86 suites / 583 tests PASS, tsc clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did:**
- spiritlogic.dev: stripped to minimal logo landing page (no products, no nav)
- Added tagline "Human Intuition. Technical Precision." to spiritlogic.dev
- Fixed logo: transparent background + neon green marks (was solid color box)
- stx-archery.com: "Spirit Logic LLC" in footer now links to spiritlogic.dev
- Gate 0 of submit framework bootstrapped (9/9 tools verified, asc binary built)

**What's Next:**
- [ ] GPS trail walk test — outdoor walk on device to verify trail records end-to-end ← START HERE
- [ ] Await Apple Developer enrollment approval (DUNS obtained, submitted)
- [ ] Gate 1: dev@spiritlogic.dev email live → Apple org verification → enroll
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: Process -->
## Claude Code — Global Process
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] No immediate action — process improvements are live
<!-- /AGENT: Claude Code | PROJECT: Process -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Deploy v1.0.9 installer to production users ← START HERE
- [ ] v2 template design — gate: committee D1/D6/D4 decisions
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

<!-- AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->
## Claude Code — NRT Scatterplot V2
*Last synced: 2026-02-22*

**Active Build:** No active build cycle — design/spec only, no code yet.
**Path:** `~/dev/NRT/docs/SCATTERPLOT_TEMPLATE_V2_DESIGN_SPEC.md`

**Decision Queue:**
- D1 — confirm exact shift boundary time with committee (7AM/7PM assumed)
- D6 — NP overwrite UX (overwrite-to-B vs block)

**What's Next:**
- [ ] Get committee confirmation on D1 and D6 ← START HERE
- [ ] Begin Phase 1 implementation: ScatterplotCreator v2 PDF template
<!-- /AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->

---

<!-- AGENT: Codex | PROJECT: Goldmine -->
## Codex — Goldmine
*Last synced: 2026-02-23*

**Active Build:** No active build cycle — spec hardening / calibration branch.

**What's Next:**
- [ ] Claude adversarial pass on `packet-r2` ← START HERE
- [ ] Rerun `design_first` on revised packet and compare output quality
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
