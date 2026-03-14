# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-13 7:15 PM by Claude Code (FPR — process diagnosis, builds submitted, autoSubmit enforced)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle. FPR builds submitted: iOS build 11 (TestFlight, processing) + Android vc 13 (Play Console internal testing, live).
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
**Mike:** Device testing with John on new FPR builds. Upload Android AAB reminder pending.
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** Field Photo Report
**Path:** `~/dev/Field-Photo-Report`
**Run:** `npx expo run:ios`

---

## What We Did This Session (Mar 13 PM continued)

- Diagnosed why Lean v3 process is failing — agreed on 4-step core process (talk → Codex builds → Claude reviews → ship)
- Identified lessons file is broken (47 items, wrong abstraction) — split strategy: submission runbook, project CLAUDE.md, behavioral rules
- Found existing NEXT-APP-PLAYBOOK.md wasn't being read — added to global session start contract
- Added `autoSubmit: true` to eas.json for both FPR and STX Archery (structural fix, not a lesson)
- Fixed MEMORY.md truncation bug — screenshot convention was past line 200 cutoff, moved to top
- Submitted iOS build 11 to TestFlight + Android vc 13 uploaded to Play Console internal testing

---

## What's Next

- [ ] Device testing with John (TestFlight build 11 + Play internal vc 13) ← START HERE
- [ ] Upload screenshots to ASC + Google Play from device testing
- [ ] Submit for App Store + Play Store review
- [ ] Pixel 7a arrives Mar 18-19 — Android device testing

---

## Notes

- 4 FPR issues remain open: #1 (dark palette), #3 (preview zoom), #5 (vendor fields), #7 (settings nav)
- Codex → Claude handoff communication is #1 process blocker (Mike pastes manually)
- Screen-sharing product idea noted — solve "agent can't see the screen" problem

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| Field Photo Report | 🟡 Builds submitted, awaiting testing | Device testing → screenshots → submit |
| STX Archery | 🟡 v1.0.1 in review (both platforms) | Await approval, plan v1.1 |
| Lean v3 Process | 🟡 Simplified to 4-step core | Stop adding infra, use what works |
| OneDoc | 🟢 M10.1 live | Install EXE on work laptop |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval |
| NRT | 🟡 local shell iteration | Resolve 15-min team-block display |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
