# Sync File for Claude

*Last synced: February 12, 2026 by Claude Code*

---

## Current Focus

**Project:** STX Archery (formerly 3D Archery Score Tracker)
**Repo:** https://github.com/miketoles/3darchery
**Path:** `~/dev/3dArchery`
**Run:** `npx expo start` (Expo dev server, iOS simulator)

---

## What We Did This Session

- Architecture review of PNG-RENDERER-SPEC.md (B1 migration: SVG paths -> PNG images + elliptical scoring)
- Found 1 BLOCKER (ASA validation throws on legacy IDs) + 2 MEDIUM + 2 LOW issues
- Applied 5 patches to spec, promoted to v1.1 FINAL
- Updated HANDOFF.md (Cycle 45), wrote PROMPT FOR CODEX handoff block
- Codex build in progress: PNG renderer migration across rendering, scoring, and round manager layers

---

## Current State

STX Archery is feature-complete (Cycle 44, 29 suites / 206 tests). Animal catalog module built (17 animals, pack system). PNG renderer migration spec reviewed and finalized — Codex is building it now (Cycle 45). This replaces SVG-path animal rendering with PNG images + elliptical vital zone scoring. The spec touches 8 files: renderer, IBO/WA-3D/ASA scoring engines, round manager, shoot screen, types, and shared utilities. DUNS application still pending (blocks Apple Developer enrollment).

---

## What's Next

- [ ] Review Codex's PNG renderer build (Cycle 45) when complete <- NEXT
- [ ] Wait for DUNS number -> Apple Developer Organization enrollment + Google Play <- BLOCKED
- [ ] Step 22: App Store submission (EAS builds, real RevenueCat API keys, store assets)
- [ ] Visual tuning of zone fractions (0.3/0.6/1.0/2.5) after first PNG render test

---

## Open Questions

- DUNS number pending — blocks Apple Developer + Google Play enrollment
- Zone ring fractions (0.3/0.6/1.0/2.5) may need visual tuning after first PNG render on device
- ASA_TARGET_CENTERS only maps 5 legacy animals — new catalog IDs fall back to canvas center (acceptable for now)

---

## Notes for Mobile Session

PNG renderer migration is the last major code change before App Store submission. Once Codex finishes and CC reviews, the app will render actual animal PNG images instead of SVG silhouettes, with elliptical scoring zones. After that it's submission mechanics: EAS builds, API keys, store listing, final gate review.

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md*
https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md
https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md
