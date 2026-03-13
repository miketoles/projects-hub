# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-13 6:00 PM by Claude Code (FPR — RC listener refactor + bundled fixes, builds submitting)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle. FPR iOS build 11 + Android vc 13 submitted to EAS (auto-submit to TestFlight, manual upload for Play Console).
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
**Mike:** Device testing with John on new FPR build (iOS 11 on TestFlight). Process audit needed — rules not being enforced structurally.
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** Field Photo Report
**Path:** `~/dev/Field-Photo-Report`
**Run:** `npx expo run:ios`

---

## What We Did This Session (Mar 13 PM)

- Refactored paywall to RevenueCat listener pattern (issue #13) — PurchaseContext + usePurchaseStatus hook, eliminated all manual setUnlocked/stale closure bugs
- Fixed saveGeneratedReport timestamp drift (DB now preserves prepared report timestamp)
- Bundled 4 PDF/UI fixes: removed per-photo timestamp (#9), vendor contact separate lines (#10), blank service date (#11), SaveIndicator layout jump (#8)
- Removed "Generated at" timestamp from PDF entirely (John's suggestion — service date is what matters)
- Closed 9 issues total (#2, #4, #6, #8, #9, #10, #11, #12, #13), added lessons 42-47
- Identified process gap: rules exist but aren't enforced structurally — process audit queued

---

## What's Next

- [ ] Device testing with John (TestFlight build 11) ← START HERE
- [ ] Upload screenshots to ASC + Google Play from device testing
- [ ] Process audit: convert violated rules into enforced gates/hooks
- [ ] Submit for App Store + Play Store review
- [ ] Pixel 7a arrives Mar 18-19 — Android testing

---

## Notes

- Android auto-submit blocked by Google Service Account Key org policy (manual upload needed)
- 4 issues remain open: #1 (dark palette), #3 (preview zoom), #5 (vendor fields), #7 (settings nav)
- Sandbox purchases persist across reinstalls (tied to Apple ID) — use new sandbox tester to test locked state

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| Field Photo Report | 🟡 RC refactor done, build 11 submitting | Device testing → screenshots → submit |
| STX Archery | 🟡 v1.0.1 in review (both platforms) | Await approval, plan v1.1 |
| Lean v3 Process | 🟡 rules not enforced | Process audit after FPR testing |
| OneDoc | 🟢 M10.1 live | Install EXE on work laptop |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval |
| NRT | 🟡 local shell iteration | Resolve 15-min team-block display |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
