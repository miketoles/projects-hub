# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-20 2:30 PM by Claude Code (FPR production submission prep)*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** Field Photo Report
**Path:** `~/dev/Field-Photo-Report`
**Run:** `npx expo start`

---

## What We Did This Session (Mar 20)

- Reviewed + merged Codex's `useAndroidKeyboardScroll` hook (auto-scroll focused input on Android)
- Built FPR Android AAB (build 24) via EAS cloud, downloaded to project dir
- Uploaded to Play Console internal testing, John + Mike confirmed testing passed
- Filed #27 for remaining keyboard polish (buttons below fields still blocked — low priority)
- Committed + pushed all code, 35/35 tests pass, tsc clean

---

## What's Next

- [ ] Take screenshots for both stores (iPhone 6.7", iPad 12.9", Android phone) ← START HERE
- [ ] Create Play Store feature graphic (1024x500)
- [ ] Decide: submit fresh iOS build with latest code or use existing TestFlight build 2
- [ ] Submit to Google Play production track
- [ ] Submit to App Store for review
- [ ] STX: Re-test IAP on Android after RC credential propagation (JSON key uploaded Mar 19)

---

## Notes

- FPR device testing PASSED — keyboard, mark complete, date picker, tab icons, PDF all confirmed working
- Keyboard fix is "good enough for launch" — #27 tracks future improvement
- STX Archery build 8 uploaded to Play Console, awaiting John's device testing
- STX IAP: RevenueCat credential propagation may be complete (36hr window from Mar 19)

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| Field Photo Report | 🟡 Testing passed, ready for submission | Screenshots + production submit |
| STX Archery | 🟡 Build 8 on Play Console | John device testing + IAP retest |
| Lean v3 Process | 🟢 Stable | Use as-is |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
