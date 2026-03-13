# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-13 by Claude Code (FPR — paywall redesign, builds passing, store listings drafted)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
**Mike:** Device testing with John on TestFlight build 6 (iOS) + Play internal testing build 8 (Android). Android blocked on unlocked test device purchase.
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** Field Photo Report
**Path:** `~/dev/Field-Photo-Report`
**Run:** `npx expo run:ios`

---

## What We Did This Session (Mar 13)

- Redesigned paywall: removed free tier entirely, locked all report output behind $9.99 one-time purchase with zero bypass surface
- Fixed EAS build failures (4 consecutive failures) — root cause: Expo transitive peer dep conflict, fix: `.npmrc` with `legacy-peer-deps=true`
- Both builds now passing: iOS build 6 submitted to TestFlight, Android build 8 on Play Console internal testing
- Updated store listing copy on both ASC and Google Play (no more "free to try" language), linked build 6 in ASC
- Updated landing page + support FAQ on fpr.spiritlogic.dev, added lessons 36-40 to global lessons log

---

## What's Next

- [ ] Device testing with John (TestFlight iOS + Android internal) ← START HERE
- [ ] Take screenshots from device testing for both stores
- [ ] Upload screenshots to ASC + Google Play, finalize listings
- [ ] Submit for App Store + Play Store review
- [ ] Mike: order unlocked Android test device

---

## Notes

- Google Play listing saved as draft (text + icon done, screenshots required to publish)
- ASC listing saved (text + build linked, screenshots required for review submission)
- Android testing blocked on unlocked device — carrier-locked Moto G returned
- Mike wants to explore "AI screen sharing" product idea — saved to memory for future design session

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| Field Photo Report | 🟡 builds passing, store listings drafted | Device testing → screenshots → submit |
| STX Archery | 🟢 iOS RELEASED, Android LIVE | Post-launch monitoring |
| Lean v3 Process | 🟢 broker live | Use for new tasks |
| OneDoc | 🟢 M10.1 live | Install EXE on work laptop |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval |
| NRT | 🟡 local shell iteration | Resolve 15-min team-block display |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
