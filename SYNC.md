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

- Created **NRT Unified Master Plan** at `~/dev/NRT/docs/NRT-MASTER-PLAN.md` (~600 lines, 12 sections)
- Two-agent review cycle: Codex applied 3 Medium fixes, Claude Code verified. Then Codex added G5/B2 sequencing (diagnose ESM in Phase A, fix in Phase C, gate Phase D), Claude Code verified clean.
- All review findings resolved. Plan is internally consistent on: baseline reviews, compliance artifacts (12-17), corrections authority (core/main), and B2 pre-Phase-D gating.
- Agent A signed off. **Agent B + Mike sign-off is the next gate.**

---

## Current State

Phases 0-2 complete. 18 risks resolved. 40 backend tests, zero frontend tests. Master plan finalized and verified. Ready for sign-off, then Phase A execution.

---

## What's Next

- [ ] **Agent B: Review master plan and sign off** ← START HERE
- [ ] Mike: Resolve CR1-CR4 and sign off
- [ ] Phase A Day 3: Freshness check + B2 ESM diagnosis + create tasks/ dir + update STATUS.md

---

## Open Questions / Mental Context

- **Master plan:** `~/dev/NRT/docs/NRT-MASTER-PLAN.md` — fully reviewed, all findings closed
- **B2 (npm start ESM):** Now sequenced as diagnose-in-A → fix-in-C → gate-D. No longer deferred.
- **4 Conflicts needing Mike's input (Section 3.1):**
  - CR1: STATUS.md says offline → recommend update to testing-first
  - CR2: System Design offline specs → recommend mark "Future/ABA only"
  - CR3: UI/UX Phases 3-5 → recommend defer to backlog
  - CR4: Two SDE specs → recommend `~/dev/NRT/docs/SDE Scatterplot Data Entry Design.md` as authoritative

---

## Notes for Mobile Session

**Agent B: Review `~/dev/NRT/docs/NRT-MASTER-PLAN.md` Section 12 checklist:**
1. Plan completeness — no orphaned items?
2. Phase sequence — dependencies make sense?
3. Review process — executable by any agent?
4. Ari feedback path — clear?
5. Corrections review decision — sound?
6. Could hand to Craig Hospital IT?
7. Any unresolved concerns?

**Mike: Resolve CR1-CR4 in Conflict Register (Section 3.1).**

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*Fetch: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
