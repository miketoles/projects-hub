# Sync File for Claude

*Last synced: February 7, 2026 by Claude Code*

---

## Current Focus

**Project:** MikeText — multiplatform (macOS + iOS/iPad)
**Path:** `~/dev/MikeText`
**Run:** Open `MikeText/MikeText.xcodeproj` in Xcode → Run

## What We Did This Session

- Completed Phase 4 (iOS polish) code review — **PASS**
- Verified settings sheet, compact status bar, line number gutter, iPad keyboard shortcuts
- All 4 implementation phases (1, 2a, 2b, 4) built by Codex and reviewed by Claude
- Both macOS and iOS simulator builds passing

## Current State

MikeText is a SwiftUI text editor with syntax highlighting, line numbers, invisibles, and multiple color modes. Originally macOS-only, now compiles for macOS + iPhone + iPad. Phase 4 changes are uncommitted (pending Mike's runtime verification). Phase 3 (iCloud Drive sync) is deferred — no code needed, just manual testing on real devices.

## What's Next

- [ ] Runtime-test Phase 4 on iPhone simulator (settings sheet, line numbers, status bar) ← START HERE
- [ ] Commit Phase 4 changes after verification
- [ ] Phase 3: iCloud Drive sync testing on real device (checklist at `tasks/phase3-icloud-testing-checklist.md`)
- [ ] ScatterplotCreator: smoke test v1.0.3 on Windows, then deploy

## Open Questions

- Whether to get a paid Apple Developer account (enables app-specific iCloud container, App Store)
- Parkour Runner game still queued — Phase 1 scaffolding approved

## Notes for Mobile Session

MikeText multiplatform is functionally complete. Think about whether you want to do the iCloud sync testing soon (needs real iPhone + same Apple ID) or move on to other projects.

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| MikeText | :green_circle: | Runtime test Phase 4, then commit |
| ScatterplotCreator | :green_circle: | Smoke test on Windows, deploy v1.0.3 |
| Parkour Runner | :yellow_circle: | Phase 1 scaffolding ready to start |
| NRT Core | :yellow_circle: | IT meeting, collecting triage feedback |

---

*Fetch: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
