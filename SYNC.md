# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-02 by Claude Code (OneDoc — installer built, blank screen root-caused)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| OneDoc | 🟡 Installer built, pending Windows test | Install new EXE on work laptop | Claude Code |
| STX Archery | 🟡 Build 21 in TestFlight | Await John feedback on pinch zoom | Claude Code |
| ScatterplotCreator | 🟢 v1.0.10 — archive feature + BUG-008 fix | Await committee v2 approval | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning | Claude Code |

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
- If it works: v1 is done, ready for real-world testing with Word + network drive
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Completed M3 CC review — found+fixed Word COM `PrintOut()` $Copies wrong parameter position
- Dispatched + approved M4 (network hardening: NetworkHealthMonitor, cache, offline UX)
- Dispatched + approved M5 (rotating logger, electron-builder NSIS config)
- Built Windows installer — fixed 3 bugs: `dist/`→`out/` path, 32→256px ICO, ESM preload needs `sandbox: false`

**What's Next:**
- [ ] Install new EXE on work laptop ← START HERE (Task #1 in CC)
- [ ] Verify UI renders (should show full dark UI, no more blank screen)
- [ ] Test with real Word + L-drive if UI works
<!-- /AGENT: Claude Code | PROJECT: OneDoc -->

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-02*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** BFX-06 | **Status:** submitted ✅
**Next agent:** mike
**Building:** John feedback — archer colors, pinch-to-zoom, ring label hide
**Gates:** 91 suites / 626 tests, tsc clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
- Waiting on John's feedback on Build 21 before any further work
- IAP product setup in App Store Connect ($14.99 non-consumable) — not yet done
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] John reviews Build 21 ← WAITING
- [ ] IAP product setup in App Store Connect
- [ ] App Store submission when testing + IAP complete
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

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
