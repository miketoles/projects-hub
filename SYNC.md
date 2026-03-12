# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-12 by Claude Code (FPR — 11 bugs fixed + 2 features, ready for paywall discussion)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle. Task contract at `/Users/miketoles/dev/Field-Photo-Report/TASK_CONTRACT.md`.
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
**Run:** `npx expo run:ios`

---

## What We Did This Session (Mar 12)

- Fixed 11 bugs from device testing (date picker, camera flow, duplicate company name, empty states, logo state, save indicator, date format wrapping, time format, etc.)
- Added 2 features: job counts on tab labels, removed redundant report ref from PDF footer
- All changes compile clean (`tsc --noEmit` passes)
- Changes uncommitted — ready for review and commit on return

---

## What's Next

- [ ] Review and commit bug fix + feature batch ← START HERE
- [ ] Discuss and implement paywall improvements (blur preview, "x of y free reports", prevent re-open bypass)
- [ ] New EAS builds for both platforms with fixes
- [ ] Device testing round 2
- [ ] Screenshots for both stores (Phase 5.1)
- [ ] Store metadata finalization + submission (Phase 5.2-5.3)

---

## Notes

- Phases 1-3 COMPLETE (subdomain, app config, store records, IAP, RevenueCat)
- Phase 4 builds done — device testing surfaced 11 bugs, all now fixed
- Paywall discussion pending: Mike wants blur preview after 3 reports, counter, prevent re-open bypass
- iOS credentials: reused STX Archery dist cert (G7SQLLU662), ASC submit key U6BLYHFZBH shared
- Test infrastructure (Jest) has pre-existing Babel config issue — not caused by changes

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| Lean v3 Process | 🟢 broker live; both profiles validated | Use for new tasks via lane runner | Codex |
| STX Archery | 🟢 iOS RELEASED, Android LIVE on Google Play | Post-launch monitoring | Claude Code |
| OneDoc | 🟢 M10.1 live | Install EXE on work laptop | Codex |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval | Claude Code |
| NRT | 🟡 local shell concept iteration active; hosted sandbox stable | Resolve 15-minute team-block display | Codex |
| Field Photo Report | 🟡 bugs fixed, paywall discussion + new builds next | Commit fixes → paywall → rebuild | Claude Code |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
