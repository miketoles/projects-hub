# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-11 by Claude Code (FPR submission — RevenueCat + store setup)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| Lean v3 Process | 🟢 broker live; both profiles validated | Use for new tasks via lane runner | Codex |
| STX Archery | 🟢 iOS RELEASED, Android LIVE on Google Play | Post-launch monitoring | Claude Code |
| OneDoc | 🟢 M10.1 live | Install EXE on work laptop | Codex |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval | Claude Code |
| NRT | 🟡 local shell concept iteration active; hosted sandbox stable | Resolve 15-minute team-block display, then continue Today shell refinement | Codex |
| Field Photo Report | 🟡 submission in progress — RC done, need EAS builds | EAS Android build → Play IAP → submit | Claude Code |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-07*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
(none) — iOS RELEASED Mar 10, Android LIVE on Google Play Mar 11
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- iOS v1.0 rejected by Apple — Guideline 5.1.1(ii): vague permission purpose strings
- Fixed all permission strings in app.json (photo library, camera, location) with specific explanations
- Added expo-location to plugins array with explicit locationWhenInUsePermission (was missing)
- Built and submitted build 23 to ASC via EAS (auto-submit, processing now)
- Updated lessons: 3dArchery/tasks/lessons.md, SUBMISSION-NOTES.md, NEXT-APP-PLAYBOOK.md

**What's Next:**
- [ ] Swap build 22 -> 23 in ASC and resubmit to App Review <- WAITING FOR PROCESSING
- [ ] Await Google Play review (submitted 2026-03-06) <- WAITING
- [ ] Set spiritlogic.app redirect to spiritlogic.dev
- [ ] Post-launch: UX-DELETE-01 (arrow deletion discoverability — v1.1)

**Notes:**
- iOS build 23 submitted to ASC, processing (5-10 min from 7:05 AM)
- Rejection was only purpose strings — no code/feature changes needed
- Android: version 2 (1.0.0), full rollout, 177 countries, still in review
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

<!-- AGENT: Claude Code | PROJECT: Field Photo Report -->
## Claude Code — Field Photo Report
*Last synced: 2026-03-11*

<!-- ACTIVE_BUILD_START -->
No active build cycle. Task contract at `/Users/miketoles/dev/Field-Photo-Report/TASK_CONTRACT.md`.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/Field-Photo-Report`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did This Session (Mar 11):**
- Completed RevenueCat setup: iOS app saved (IAP key + ASC API key + Issuer ID), Play Store app created (no JSON key — org policy blocker, tracked in spirit-logic-submit#1)
- Set EAS secrets for both RC API keys (iOS + Android)
- Created App Store product in RC (`app.spiritlogic.fieldphotoreport.unlimited`, non-consumable), attached to `unlimited` entitlement and `default` offering Lifetime package
- Google Play IAP blocked — needs first APK upload before product creation allowed
- Filed Lesson 32 (org policy skip) and Lesson 33 (Play Console nav terminology)

**What's Next:**
- [ ] EAS Android build (`eas build --platform android --profile production --non-interactive`) ← START HERE
- [ ] Upload Android build to Play Console internal testing track
- [ ] Create Google Play one-time product (`unlimited`, $9.99) in Play Console
- [ ] Add Play Store product to RC and link in offering
- [ ] EAS iOS build and TestFlight
- [ ] Device testing (Phase 4), screenshots (Phase 5), submit both stores

**Notes:**
- Phase 1 (subdomain), Phase 2 (app config), Phase 3.1 (ASC), Phase 3.3 (Apple IAP) all COMPLETE
- Phase 3.2 (Google Play record) mostly done — 9/11 setup tasks, store listing drafted, graphics deferred
- Google Cloud org policy (`iam.disableServiceAccountKeyCreation`) blocks service account JSON key — tracked in miketoles/spirit-logic-submit#1, skipped for now (works without it for one-time IAP)
- Automation of submission process is a high-priority future improvement
<!-- /AGENT: Claude Code | PROJECT: Field Photo Report -->

---

<!-- AGENT: Codex | PROJECT: NRT -->
## Codex — NRT
*Last synced: 2026-03-11*

<!-- ACTIVE_BUILD_START -->
**Current build:** Local Today-shell concept iteration only; real route migration paused until the shell/schedule design is settled.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/NRT`
**Run:** local frontend concept route: `http://127.0.0.1:5175/concept-lab/site-shell/left-rail-v1`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Kept the real routed app stable and iterated only in the standalone local concept page for the new NRT shell
- Refined the left-rail Today concept with a collapsible radar, collapsible schedule, date navigation, military time, role-based team views, sticky time column, and a centered schedule-detail popup
- Added realistic mock coverage for RBT/BCBA staffing across a week, with daily team-size variation and grouped team matrix views (`RBTs`, `BCBAs`, `Everyone`)
- Tightened the schedule interaction model around what staff actually care about first: patient, then time, then deeper details on inspect
- Confirmed the current concept still has one open UX issue: 15-minute schedule blocks remain too dense to read cleanly and need one more concept pass before we migrate this shell into the real app
- Noted a follow-up process requirement: once the shell/schedule concept stabilizes, the NRT design docs should be updated to reflect the new approved direction

**What's Next:**
- [ ] Resolve the 15-minute team-block display in the local Today concept ← START HERE
- [ ] Continue refining the local left-rail shell/schedule concept until the Today screen is stable enough to migrate
- [ ] After the concept is approved, update the NRT design docs and migration plan to reflect the final shell direction
- [ ] Only then apply the new shell primitives to the real `Today` route and continue module migration

**Notes:**
- Current concept source of truth remains local: `/concept-lab/site-shell/left-rail-v1`
- Hosted sandbox and Phase A/B infra remain stable; this session intentionally avoided changing the deployed routes while concept work is still fluid
- Current NRT repo has uncommitted local concept edits plus unrelated noise left intentionally untouched: `.DS_Store`, `supabase/.temp/`, and `core/docs/mockups/nrt-logo/`
- The next migration step should not start until the Today concept solves the quarter-hour scheduling readability problem
<!-- /AGENT: Codex | PROJECT: NRT -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
