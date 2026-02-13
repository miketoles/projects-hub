# Sync File for Claude

*Last synced: Feb 12, 2026 by Claude Code*

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Repo:** https://github.com/miketoles/3darchery
**Path:** `~/dev/3dArchery`
**Run:** `cd ~/dev/3dArchery && npx expo run:ios`

---

## What We Did This Session

- B3 (Cycle 52): Animal names in summary/export + target navigation — MERGED
- Fixed export success messages ("Shared" → "Saved... to disk")
- Ran comprehensive 20-finding UX audit across all app screens
- B4 (Cycle 53): UX audit fixes — 7 tasks, APPROVED FOR MERGE
  - Added back buttons to Quick Shoot + Export (users were trapped)
  - Confirmation dialogs for destructive actions (delete round/bow/arrow, clear all data)
  - Equipment create save feedback, bow edit save confirmation
  - Rounds + Stats tabs auto-refresh on focus
  - Deduped resolveAnimalShortName, PDF scorecard display names
- Created beta tester guide (docs/TESTER-GUIDE.md)
- Gates: 38 suites / 234 tests, all green

---

## Current State

App is feature-rich: scoring, animal targets, course templates, equipment, exports (CSV/PDF/JSON/share card), stats. B4 UX fixes approved, needs sim-test before merge. 10 deferred UX items remain (tab icons, "Shoot Again" fix, etc). DUNS pending for Apple Developer enrollment.

---

## What's Next

- [ ] Sim-test B4 UX fixes → merge ← START HERE
- [ ] DUNS → Apple Developer enrollment → TestFlight
- [ ] Address deferred UX items (10 remaining)
- [ ] Beta testing with TESTER-GUIDE.md
- [ ] App Store submission (EAS builds, store assets)

---

## Open Questions / Mental Context

- Equipment create "stale bow list" bug: code looks correct but seen once — needs runtime verification
- Mike prefers VS Code plugin over Desktop (faster)
- TestFlight needs Apple Developer ($99 individual or org with DUNS)

---

## Notes for Mobile Session

- 10 deferred UX items in HANDOFF.md — good to prioritize on mobile
- Beta tester recruitment, App Store listing copy, pricing strategy

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md*
https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md
https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md
