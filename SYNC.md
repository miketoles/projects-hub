# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-25 (ScatterplotCreator v1.0.7)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT Scatterplot V2 | 🟢 Spec complete, Phase 1 GO | Committee decisions on D1/D6, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟢 v1.0.7 built, ready to deploy | Deploy installer to production users | Claude Code |
| STX Archery | 🟢 DH complete, commit done | GPS trail walk test, await Apple enrollment | Claude Code |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 | Codex |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** DH-B4 | **Status:** approved ✅ — commit done
**Next agent:** mike (GPS trail walk test, await Apple enrollment)
**Building:** Device hardening complete — GPS trail fix, Map Course hidden for v1, settings fixes
**Gates:** 86 suites / 583 tests PASS, tsc clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did:**
- DH-B4 CC review — all 15 points PASS (GPS trail, Map Course, settings)
- Commit pass complete — DH-B3 + DH-B4 committed (37 commits ahead of origin)
- HANDOFF.md updated: cycle DH-B4 approved, next agent: mike

**What's Next:**
- [ ] GPS trail walk test — outdoor walk on device to verify trail records end-to-end ← START HERE
- [ ] Await Apple Developer enrollment approval (DUNS obtained, submitted)
- [ ] Push + App Store submission once enrolled
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

**What We Did:**
- Implemented v1.0.7: Print All checkbox selections now persist across modal reopens (`state.printAllSelections` Map)
- Committed all prior v1.0.4–v1.0.6 work (bug fixes, hardening, test infrastructure, lock.js, dead code removal)
- 82/82 tests passing; `npm run build:installer` → `NRT Scatterplot Creator Setup 1.0.7.exe`; pushed to GitHub

**What's Next:**
- [ ] Deploy v1.0.7 installer to production users ← START HERE
- [ ] v2 template design — gate: Mike approval + committee D1/D6 decisions
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
