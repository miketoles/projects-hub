# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-15 2:20 PM by Claude Code (FPR — iOS submitted to App Review)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle. FPR iOS v1.0.0 (build 20) submitted to App Store Review. Waiting for approval.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
**Mike:** Watch for Apple review email. Android submission when test device arrives (~Mar 19-20).
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** Field Photo Report
**Path:** `~/dev/Field-Photo-Report`
**Run:** `npx expo run:ios`

---

## What We Did This Session (Mar 15)

- Fixed "Preparing images for preview..." bug (status persisted after tapping preview)
- Updated iOS permission strings to avoid Apple 5.1.1 rejection (learned from STX Archery)
- Built locally (build 20), uploaded via Transporter to TestFlight
- Completed full ASC submission: screenshots, store copy, age rating, privacy, copyright
- Submitted FPR iOS v1.0.0 to App Store Review
- Logged STX Archery edge-to-edge deprecation issue (#13)

---

## What's Next

- [ ] Wait for Apple review (1-3 business days) ← WAITING
- [ ] Android build + device testing when Pixel arrives (~Mar 19-20)
- [ ] Google Play Store submission (screenshots, content declarations, production release)
- [ ] STX Archery v2 design doc when Mike has bandwidth

---

## Notes

- FPR open issues: #1 (dark palette), #3 (preview zoom), #5 (vendor fields), #7 (settings nav), #20 (tagline), #21 (report architecture)
- STX Archery open: #13 (edge-to-edge API deprecations for Android 15)
- PDF generation was the main bug source in FPR — added lesson to NEXT-APP-PLAYBOOK.md

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| Field Photo Report | 🟡 iOS submitted, waiting for review | Apple review → Android build + submit |
| STX Archery | 🟢 Live on both stores | v2 design doc, fix #13 in next build |
| Lean v3 Process | 🟢 Stable | Use as-is |
| OneDoc | 🟢 M10.1 live | Install EXE on work laptop |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval |
| NRT | 🟡 Local shell iteration | Resolve 15-min team-block display |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
