# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-26 (STX Archery GEA-B committed, pivoting to Spirit Logic website)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟢 GEA-B committed | Device test GEA-B | Claude Code |
| Spirit Logic Website | 🟡 Logo work | Add white-bird/green-text variation | Claude Code |
| NRT Scatterplot V2 | 🟢 Spec complete | Committee D1/D6 decisions, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟢 v1.0.9 built | Deploy installer to production users | Claude Code |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 | Codex |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** GEA-B | **Status:** committed ✅
**Next agent:** mike (device test)
**Building:** Gear enhancements — bow notes, arrow-bow M2M, free round countdown, dead-code cleanup
**Gates:** tsc PASS, 87/587 tests PASS — CC architecture review clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
(none — committed, ready for device testing)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Confirmed GEA-B plan fully implemented (all 5 UX issues resolved by Codex build)
- Pivoting to Spirit Logic website logo work

**What's Next:**
- [ ] Device test GEA-B (multi-bow select, bow notes, free rounds countdown, dev options no 10-tap) ← START HERE
- [ ] GPS trail testing (walk a real round — still pending)
- [ ] Await Apple Developer enrollment (DUNS submitted, pending)
- [ ] When enrolled: Copy Device ID → EAS Build → TestFlight → submission
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

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
- [ ] v2 template — gate: committee D1/D6/D4 decisions
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

<!-- AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->
## Claude Code — NRT Scatterplot V2
*Last synced: 2026-02-22*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

<!-- DECISION_QUEUE_START -->
- D1 — confirm shift boundary time with committee (7AM/7PM assumed)
- D6 — NP overwrite UX (overwrite-to-B vs block)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Get committee confirmation on D1 and D6 ← START HERE
- [ ] Begin Phase 1: ScatterplotCreator v2 PDF template
<!-- /AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->

---

<!-- AGENT: Codex | PROJECT: Goldmine -->
## Codex — Goldmine
*Last synced: 2026-02-23*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Claude adversarial pass on `packet-r2` ← START HERE
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
