# Sync File for Claude

*Last synced: February 5, 2026 by Claude Code*

---

## Current Focus

**Project:** NRT Core
**Repo:** https://github.com/miketoles/NRT
**Path:** `~/dev/NRT/core/`
**Run:** `cd core/backend && npm run dev` → http://127.0.0.1:3003 | `cd core/frontend && npm run dev` → http://localhost:5175

---

## What We Did This Session

- Completed Phase 2: Navigation & Routing (URL routing, ConfirmDialog, useUnsavedChanges, breadcrumbs, admin gating)
- Created `core/frontend/STATUS.md` covering all 3 completed phases
- Rebuilt prototype with Phase 2 changes
- Added zip packaging step to `scripts/build-prototype.sh` (53MB distributable zip)

---

## Current State

All 3 frontend UI/UX phases are complete and pushed. Phase 0: MVP, Phase 1: Accessibility (WCAG 2.1 AA), Phase 2: Navigation & Routing. Prototype is synced and zip-packaged for tester. No Phase 3 defined yet.

---

## What's Next

- [ ] Define Phase 3 direction (offline, testing, auth, notes UI, or reporting)
- [ ] Decide on Corrections Review open questions from legacy app
- [ ] Production auth (Windows AD)

---

## Open Questions / Mental Context

- Phase 3 direction is open — multiple possibilities discussed but none chosen
- Legacy `app-scatterplot` still has open questions on cell-level corrections review
- Backend `npm start` (dist bundle) has ESM require issues — use `npm run dev` only

---

## Notes for Mobile Session

- Think about what Phase 3 should prioritize for tester feedback
- Consider whether offline support or testing framework is more urgent

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*Fetch: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
