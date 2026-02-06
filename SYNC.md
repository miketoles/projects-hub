# Sync File for Claude

*Last synced: February 5, 2026 by Claude Code*

---

## Current Focus

**Project:** NRT Core (Nurse Resource Tool)
**Repo:** https://github.com/miketoles/NRT
**Path:** `~/dev/NRT/core/frontend` + `~/dev/NRT/core/backend`
**Run:** `npm run dev` in both → frontend http://localhost:5175, backend http://127.0.0.1:3003

---

## What We Did This Session

- Analyzed Phase 3 options: Offline Support vs Testing Framework
- Decided: **Testing first, offline deferred**
- Wrote full Phase 3 plan at `~/dev/NRT/docs/Phase3-Plan.md`

---

## Current State

All 3 frontend UI/UX phases complete (MVP → Accessibility → Routing). Backend has Vitest with 3 test files; frontend has zero tests. Prototype runs locally via start.bat with bundled Node + Caddy.

---

## What's Next

- [ ] Review Phase 3 plan on mobile ← START HERE
- [ ] Phase 3A: Install Vitest + jsdom in frontend (~1 day)
- [ ] Phase 3B: Frontend pure logic tests (~1 day)
- [ ] Phase 3C: Expand backend API tests (~1-2 days)
- [ ] Phase 3D: Add retry wrapper on apiFetch (~30 min)

---

## Open Questions / Mental Context

- **Why not offline?** Prototype runs localhost (no network hop). Full offline needs service worker + IndexedDB + conflict resolution for 23 endpoints — 2-3 weeks. A retry wrapper on apiFetch handles wifi blips in 30 min.
- **What to test:** Pure functions first (route param validation, grid transforms, CHSA calcs) — no DOM needed. Then backend API routes (patient CRUD, scatterplot save/load).
- **What NOT to test:** E2E (Playwright — too flaky while UI changes), component rendering (low value).
- **Key question:** Is wifi reliability actually causing problems today, or is offline hypothetical?

---

## Notes for Mobile Session

Review Phase 3 plan (`~/dev/NRT/docs/Phase3-Plan.md`) and decide:
1. Agree with testing-first approach?
2. Is wifi causing real user problems, or is offline a future concern?
3. Any specific bugs/regressions tests should target first?
4. Any Phase 3 ideas beyond testing + retry wrapper?

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*Fetch: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
