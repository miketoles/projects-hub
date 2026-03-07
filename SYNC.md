# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-07 by Codex (Lean v3 broker launchd + token rotation verified)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| Lean v3 Process | 🟢 broker live; both profiles validated | Use for new tasks via lane runner | Codex |
| STX Archery | ✅ iOS in review; Android submitted to production review | Await both reviews | Claude Code |
| OneDoc | 🟢 M10.1 live | Install EXE on work laptop | Codex |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval | Claude Code |
| NRT | 🟡 plan review complete | Mike decides go/no-go on Phase A build | Claude Code |
| Field Photo Report | 🟡 v1 running on iPhone; polish in progress | Fix camera dual-save + simplify PDF UX | Codex |

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

<!-- AGENT: Codex | PROJECT: Lean v3 Process -->
## Codex — Lean v3 Process
*Last synced: 2026-03-07*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/lean_v3_full_test`
**Run:** `./lane.sh start --profile <claude-pr|codex-pr> --request "..."`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Hardened the v2 design doctrine and closed the adversarial Claude review loop against the new single-file doctrine
- Fixed the Codex -> Claude broker transport path and documented the real noninteractive Claude requirements
- Created and pushed the standalone Lean v3 repo: `https://github.com/miketoles/lean-v3.git`
- Installed the launchd broker with a private token env file, rotated the Claude token, restarted the agent, and re-verified the passive smoke path

**What's Next:**
- [ ] Use Lean v3 for new tasks through `./lane.sh` with the launchd broker active ← START HERE
- [ ] If Claude broker auth fails: refresh `~/.config/lean-v3/claude-broker.env`, kickstart the launchd agent, rerun smoke

**Notes:**
- LaunchAgent label: `com.spiritlogic.lean-v3-broker`
- Broker token lives outside repos in `~/.config/lean-v3/claude-broker.env`
- Latest Lean v3 commits pushed: `239fc09` and `189b58b`
- Passive broker smoke after token rotation returned `REVIEW_RESULT: APPROVE` and `TRANSPORT_STATUS: OK`
<!-- /AGENT: Codex | PROJECT: Lean v3 Process -->

---

<!-- AGENT: Codex | PROJECT: Field Photo Report -->
## Codex — Field Photo Report
*Last synced: 2026-03-06*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/Field-Photo-Report`
**Run:** `npx expo run:ios --device`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Built the v1 Expo app end-to-end: jobs, photos, report preview, PDF generation/share, settings, offline local storage
- Ran the app on Mike's iPhone and iterated directly against real-device UX and report bugs
- Fixed routing, date handling, phone formatting, report field mapping, preview generation, and completed-job navigation
- Updated the design doc with an implementation checkpoint and explicit v1 camera dual-save requirement
- Added new Expo dev-build / Metro troubleshooting lessons to `spirit-logic-submit`

**What's Next:**
- [ ] Fix camera capture so every in-app photo saves to both app storage and iPhone Photos silently ← START HERE
- [ ] Simplify PDF UX to one obvious top-level PDF action
- [ ] Finalize exact preview/PDF parity and remaining on-device report polish

**Notes:**
- Latest Field Photo Report commits pushed: `b6e988e` and `b0a7887`
- Latest submission framework commit pushed: `04e2c89`
- Native iPhone dev build with `expo-media-library` was rebuilt and installed; dual-save behavior still needs verification/fix
<!-- /AGENT: Codex | PROJECT: Field Photo Report -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
