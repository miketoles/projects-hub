# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-19 7:30 PM by Claude Code (STX + FPR Android bug fixes)*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Status:** code complete, build blocked
**Building:** Android bug fixes #8, #14, #15 (pinch-to-zoom, button text, sight mark auto-save)
**Blocker:** Local Android build fails with "unknown error" after Gradle completes 407 tasks. Needs investigation next session.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
**Mike:** Investigate STX local Android build failure. FPR local build works (Expo 55/Gradle 9), STX fails (Expo 54/Gradle 8.14). May need cloud build or Gradle config fix.
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** STX Archery + Field Photo Report
**Path:** `~/dev/3dArchery` + `~/dev/Field-Photo-Report`
**Run:** `npx expo run:ios`

---

## What We Did This Session (Mar 19)

- Fixed 5 FPR Android bugs (#22-#26): keyboard, date picker, mark complete crash, tab icons, PDF crash
- Built FPR Android AAB successfully (build 21 on Play internal testing)
- Fixed 3 STX Android bugs (#8, #14, #15): sight mark auto-save, button font weight, pinch-to-zoom gesture
- Diagnosed button text issue: Android can't synthesize fontWeight 600 — added SourceSans3-SemiBold.ttf
- Uploaded RevenueCat service account key for both FPR and STX Play Store apps

---

## What's Next

- [ ] Fix STX Android local build failure ← START HERE
- [ ] Upload STX Android build to Play Console for testing
- [ ] Device test FPR Android build 21 (John testing 5 bug fixes)
- [ ] FPR: Google Play screenshots + production submission
- [ ] STX: Re-test IAP on Android after RC propagation

---

## Notes

- `ANDROID_HOME=/usr/local/share/android-commandlinetools` required for local builds
- FPR local builds work, STX fails — likely Expo 54 vs 55 Gradle version difference
- STX TASK_CONTRACT.md and commit `d8c0640` have all 3 bug fixes ready, just needs successful build
- Created STX #16 (sight mark v2 UX review for future equipment redesign)

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| Field Photo Report | 🟡 Android build 21 in internal testing | John device testing, then production submit |
| STX Archery | 🔴 Code done, Android build blocked | Fix local build, upload to Play Console |
| Lean v3 Process | 🟢 Stable | Use as-is |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
