# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-02-28 by Claude Code (STX Archery — device testing, Vegas bug investigation)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟡 TestFlight active, John testing, 1 build pending | Build: custom rounds removal + format count fix | Claude Code |
| Goldmine | 🟢 Strata v3 approved + App Store design drafted | Mike reviews design docs before build | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning | Claude Code |
| ScatterplotCreator | 🟡 v2 committee decisions captured | Build v1 Bx limit + v2 template | Claude Code |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-28*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** BFX-05 | **Status:** pending-build
**Next agent:** codex (after Mike approves build)
**Building:** Custom rounds removal + format count fixes + Vegas regression tests — ready to build
**Gates:** 90 suites / 619 tests (8 new Vegas regression), tsc clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
- Mike: Kick off Build 5 (custom rounds removal + "21 formats" everywhere + Vegas tests)
- Mike: John continues testing tomorrow — gather any new bugs before submission
- Mike: Format Rules feature — needs design approval before Codex build (show rules from create + shoot screens)
- Mike: IAP product setup in App Store Connect required before App Store submission
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- TestFlight fully set up: 2 internal testers (Mike + John), 4 builds submitted
- Fixed AnimalPill flicker bug (tap-to-change text layout shift) → Build 3
- Fixed zoom button disappearing when all arrows placed → Build 4
- Removed Custom Rounds from v1 entirely (app, docs, marketing, website)
- Updated all format counts from "22+" to exact "21" across all metadata/store files
- Investigated Vegas 300 "7-ring scoring as 8" report — scoring is correct, visual overlap issue; added 8 regression tests; documented as VEGAS-VISUAL-01

**What's Next:**
- [ ] Build 5: custom rounds removal + 21-format count + Vegas regression tests ← START HERE (tomorrow)
- [ ] John's continued testing feedback (tomorrow)
- [ ] Format Rules feature build (Codex, after Mike approves design)
- [ ] IAP product setup in App Store Connect
- [ ] App Store submission when testing complete
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: Goldmine -->
## Claude Code — Goldmine
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
**Project:** Goldmine | **Cycle:** 3 | **Status:** review-complete
**Next agent:** mike
**Building:** Infrastructure Signal Strata — adversarial review passed, implementation plan produced
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/goldmine`

<!-- DECISION_QUEUE_START -->
- Mike to review finished API Signal Strata design doc (v3) + implementation plan before build starts
- Mike to review App Store Opportunity Research design doc (v1)
- 4 open architectural decisions in Strata implementation plan
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Mike reviews both design docs ← START HERE
- [ ] Send App Store design to Codex for adversarial review
- [ ] Resolve 4 open decisions in Strata implementation plan
<!-- /AGENT: Claude Code | PROJECT: Goldmine -->

---

<!-- AGENT: Claude Code | PROJECT: NRT -->
## Claude Code — NRT
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/NRT`

<!-- DECISION_QUEUE_START -->
(none — all decisions resolved)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] RBT Session implementation planning sprint
- [ ] Fix 6 BLOCKING issues in NRT-INTELLIGENCE-DESIGN.md
- [ ] Phase D deploys when Craig IT responds
<!-- /AGENT: Claude Code | PROJECT: NRT -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`

<!-- DECISION_QUEUE_START -->
(none — field limits resolved, CNA field test blocking v2 final approval)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Build v1 Bx description 400-char limit
- [ ] Build v2 template into ScatterplotCreator
- [ ] Await CNA field test results before v2 final approval
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
