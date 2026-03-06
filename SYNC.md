# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-06 by Claude Code (STX Archery Google Play production submitted)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| Lean v3 Process | 🟢 both profiles validated | Use for new tasks | Codex |
| STX Archery | ✅ iOS in review; Android submitted to production review | Await both reviews | Claude Code |
| OneDoc | 🟢 M10.1 live | Install EXE on work laptop | Codex |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval | Claude Code |
| NRT | 🟡 plan review complete | Mike decides go/no-go on Phase A build | Claude Code |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-06*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
(none — both platforms in review)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Completed Google Play store listing (icon, feature graphic, screenshots, tablet screenshots, descriptions)
- Completed all 11 app content declarations + fixed blocking issues (photo/video permissions, advertising ID)
- Verified bank micro-deposit complete (Checking 817 verified)
- Submitted STX Archery to Google Play production review — 2026-03-06 ~9:46 AM
- Updated NEXT-APP-PLAYBOOK.md with full Google Play production submission lessons

**What's Next:**
- [ ] Await Apple App Store review (submitted 2026-03-04) <- WAITING
- [ ] Await Google Play review (submitted 2026-03-06) <- WAITING
- [ ] Set spiritlogic.app redirect to spiritlogic.dev
- [ ] Post-launch: UX-DELETE-01 (arrow deletion discoverability — v1.1)

**Notes:**
- iOS Submission ID: fa548694-7165-4a25-ad64-7af5ae30dd63
- Android: version 2 (1.0.0), full rollout, 177 countries, "Changes in review"
- Feature graphic: `assets/field-plates/feature-graphic-1024x500.png`
- Privacy policy URL: `https://stx-archery.com/privacy`
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: NRT -->
## Claude Code — NRT
*Last synced: 2026-03-06*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/NRT`

<!-- DECISION_QUEUE_START -->
- Mike: review merged NRT-SANDBOX-IMPLEMENTATION.md and decide go/no-go on Phase A build
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Mike reviews final merged plan (Sections 23-25) <- DECISION NEEDED
- [ ] If approved: CC writes Phase A build plan + dispatches to Codex
<!-- /AGENT: Claude Code | PROJECT: NRT -->

---

<!-- AGENT: Claude Code | PROJECT: Lean v3 Process -->
## Claude Code — Lean v3 Process
*Last synced: 2026-03-05*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/lean_v3_full_test`
**Runner:** `./lane.sh start --profile <claude-pr|codex-pr> --request "..."`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Use for new tasks — both profiles production-ready
<!-- /AGENT: Claude Code | PROJECT: Lean v3 Process -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-03-02*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`
**Run:** `npm start`

<!-- DECISION_QUEUE_START -->
- Committee approval needed to flip v2 as default (1-line change in main.js)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Await committee v2 approval <- BLOCKED
- [ ] Flip default to v2 when approved
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
