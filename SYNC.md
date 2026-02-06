# Sync File for Claude

*Last synced: February 6, 2026 by Claude Code*

---

## Current Focus

**Project:** NRT Core (Nurse Resource Tool)
**Repo:** https://github.com/miketoles/NRT
**Path:** `~/dev/NRT/core/frontend` + `~/dev/NRT/core/backend`
**Run:** `npm run dev` in both → frontend http://localhost:5175, backend http://127.0.0.1:3003

---

## What We Did This Session

- Completed full Phase A (testing framework), Phase C (9 compliance reviews), and Phase D prep (Track A)
- Agent B reviewed and approved all phases — 64 tests passing (46 BE + 18 FE)
- Locked AC-2 decision: staff-accessible scatterplot soft delete with safeguards (Option A)
- Rebuilt stale prototype (now includes rate limiter, retry wrapper, B2 start script fix)
- Final freshness sweep: all 4 status files consistent, review bundle current, prototype fresh

---

## Current State

All pre-deployment work is complete. Master plan approved, Phase C compliance reviews done (0 CRITICAL/HIGH code-level findings), Phase D prep Track A finished. 64 tests pass. Prototype rebuilt. Everything is **READY-WAITING-ON-B1** (target deployment environment access).

---

## What's Next

- [ ] **B1 environment access** — TLS/proxy/AD header trust verification ← GATING
- [ ] Phase D Track B: backup scheduling, post-deploy smoke test (4 user journeys)
- [ ] Commit all uncommitted Phase A/C/D changes (13 modified files, +1507/-359 lines)
- [ ] B2 backlog: full TypeScript strict-mode fix (Option 1) — tracked, deferred

---

## Open Questions / Mental Context

- All changes are uncommitted in git (HEAD is still `4836ea5`). Intentional workflow state but should commit before B1 work begins.
- B2 (backend build) resolved via runtime TS execution (Option 2). Option 1 (full type fix) is tracked backlog.
- Prototype zip is ~54MB at `prototypes/nrt-core-prototype.zip`, ready for Ari.

---

## Notes for Mobile Session

Think about B1 environment logistics: who provides access, what's the timeline, any IT coordination needed? Also worth deciding when to commit the accumulated changes.

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*Fetch: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
