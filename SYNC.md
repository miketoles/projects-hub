# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-25 (STX Archery UX-P1 approved)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT Scatterplot V2 | 🟢 Spec complete, Phase 1 GO | Committee decisions on D1/D6, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟢 v1.0.9 built, docs current | Deploy installer to production users | Claude Code |
| STX Archery | 🟢 UX-P1 approved, ready to test | Device test UX-P1, then commit | Claude Code |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 | Codex |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** UX-P1 | **Status:** approved ✅
**Next agent:** mike (ready to test on device)
**Building:** V1 UX Polish Sprint — Settings cleanup, Score→Shoot rename, Gear keyboard fixes, Stats polish
**Gates:** tsc PASS, 86/583 tests PASS — approved by CC architecture review
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
UX-P1 is approved and ready for device testing. Manual checklist in HANDOFF.md (11 items). After testing, commit and move to next cycle or App Store prep.
<!-- DECISION_QUEUE_END -->

**What We Did:**
- Sent UX-P1 plan to Codex (adversarial review → amendments → build phase)
- Codex built all 5 phases: settings cleanup, Score→Shoot, keyboard avoidance, gear card enrichment, stats polish
- CC architecture review: all phases approved, tsc clean, 86/583 tests pass
- Found pre-existing issue: settings.test.tsx not in Jest discovery path (app/ excluded)
- Updated global AGENTS.md + project AGENTS.md with full multi-agent process docs

**What's Next:**
- [ ] Device test UX-P1 — run through manual checklist in HANDOFF.md ← START HERE
- [ ] Commit UX-P1 changes after device test passes
- [ ] Await Apple Developer enrollment approval (DUNS obtained, submitted)
- [ ] Follow-up ticket: add app/ to Jest testMatch so settings.test.tsx is discovered
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
