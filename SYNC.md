# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-05 by Claude Code (Lean v3 process validation + hardening)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| Lean v3 Process | 🟡 claude-pr validated; codex-pr has 5 known gaps | Write Codex hardening prompt + smoke test | Claude Code |
| STX Archery | ✅ iOS submitted — Waiting for Review | Android: RC key + rebuild + Play Console | Claude Code |
| OneDoc | 🟢 M10.1 UX polish live; DOCX+Excel printing stable | Install EXE on work laptop | Codex |
| ScatterplotCreator | 🟢 v1.0.10 — archive + BUG-008 fix | Await committee v2 approval | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning | Claude Code |

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
- Review 5 gaps listed in session before approving codex-pr profile as production-ready
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Scaffolded lean_v3_full_test and ran full end-to-end claude-pr cycle (CC Planner+Reviewer, Codex Builder)
- Discovered and hardened: Codex cannot run `handoff send` from sandbox — rule now in process.md + lessons
- Codex built lane.sh + lane-broker.sh: full runner/broker transport system with two profiles
- Both agents got sandbox-constraint preambles (.codex-preamble.md, .claude-preamble.md)
- Identified 5 gaps blocking codex-pr readiness (preamble role-hardcoding, untested paths, entry trigger)

**What's Next:**
- [ ] Write Codex prompt: fix .codex-preamble.md (role-neutral), add codex-first entry trigger, reset HANDOFF.md on lane start ← START HERE
- [ ] Run codex-pr smoke test (validates Codex-as-Planner + Claude-as-Builder in one shot)
- [ ] If smoke passes: declare both profiles production-ready, update LEAN_V3_RUNTIME_STATE.md

**Known gaps (codex-pr):**
1. `.codex-preamble.md` says "You are the Builder" — wrong when Codex runs as Reviewer
2. Codex-as-Planner output quality untested (14-section HANDOFF.md)
3. Claude-as-Builder via `claude -p` path untested
4. Codex-first entry: no trigger for Codex to output the `./lane.sh start` command to Mike
5. `HANDOFF.md` not reset between cycles by the runner
<!-- /AGENT: Claude Code | PROJECT: Lean v3 Process -->

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-05*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
(none — waiting on Apple review)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Await Apple review (1-3 business days) ← WAITING
- [ ] Android: create Premium Lifetime product in Google Play Console ← START HERE (after Apple review)
- [ ] Android: add RC Android app, store `EXPO_PUBLIC_REVENUECAT_ANDROID_API_KEY` as EAS secret
- [ ] Android: rebuild .aab with RC key, manual first upload to Play Console
- [ ] Post-launch: UX-DELETE-01 (arrow deletion discoverability — v1.1)

**Notes:**
- iOS 1.0 Submission ID: fa548694-7165-4a25-ad64-7af5ae30dd63
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: OneDoc -->
## Claude Code — OneDoc
*Last synced: 2026-03-02*

<!-- ACTIVE_BUILD_START -->
**Project:** OneDoc Print Manager | **Cycle:** M5 | **Status:** feature-complete ✅
**Next agent:** mike
**Building:** Windows integration testing — install EXE, verify UI loads
**Gates:** 8 suites / 37 tests, tsc clean, installer built (84MB NSIS)
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/OneDoc`
**Run:** `npm run dev`

<!-- DECISION_QUEUE_START -->
- Install `dist-installer/OneDoc Print Manager Setup 0.1.0.exe` on work laptop and confirm UI loads
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Install new EXE on work laptop ← START HERE
- [ ] Verify UI renders (full dark UI, no blank screen)
- [ ] Test with real Word + L-drive if UI works
<!-- /AGENT: Claude Code | PROJECT: OneDoc -->

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
- [ ] Mike testing v1.0.10 in active use ← IN PROGRESS
- [ ] Await committee v2 approval ← BLOCKED
- [ ] Flip default to v2 when approved (1-line change in main.js)
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
