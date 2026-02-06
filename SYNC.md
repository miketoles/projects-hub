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

- Created **NRT Unified Master Plan** at `~/dev/NRT/docs/NRT-MASTER-PLAN.md`
- Consolidated ALL active plans, decisions, reviews, and workstreams into one document
- Validated all file paths against filesystem (found 7 gaps, all documented)
- Identified 4 conflicts between existing docs (logged in Conflict Register)
- Agent A signed off. Agent B review pending.

---

## Current State

Phases 0-2 complete. Feb 5 review cycle resolved all 18 risks. 40 backend tests, zero frontend tests. Ari actively testing prototype. IT infrastructure request pending. Master plan defines Phases A-E with entry/exit criteria.

---

## What's Next

- [ ] **Agent B: Review master plan** ← START HERE
- [ ] Both agents + Mike sign off on master plan
- [ ] Phase A: Testing framework (~3 days)
- [ ] Phase C: Full review bundle (9 categories)
- [ ] Phase D: Production deployment (blocked on IT)

---

## Open Questions / Mental Context

- **Master plan location:** `~/dev/NRT/docs/NRT-MASTER-PLAN.md` — 12 sections, all required format
- **4 Conflicts found (need Mike's input):**
  - CR1: STATUS.md says "Phase 3: Offline" but offline is removed from scatterplot roadmap
  - CR2: System Design doc has offline specs that won't be built for scatterplot
  - CR3: UI/UX Plan Phases 3-5 (component consolidation, polish, responsive) not sequenced — deferred to backlog?
  - CR4: Two SDE specs at different paths — which is authoritative?
- **7 Gaps found:** tasks/ dir missing, docs/modules/ dir missing, REVIEW_BUNDLE numbering conflicts (resolved: new reviews use slots 12-17), npm start ESM issue undiagnosed, IT status unknown
- **Corrections review:** Resolved — Core's re-validation loop (option c) is the answer

---

## Notes for Mobile Session

**Agent B: Please review `~/dev/NRT/docs/NRT-MASTER-PLAN.md` and check off Section 12 items:**
1. Plan completeness — no orphaned items?
2. Phase sequence — dependencies make sense?
3. Review process — executable by any agent?
4. Ari feedback path — clear?
5. Corrections review decision — sound?
6. Could hand this to Craig Hospital IT?
7. Any unresolved concerns?

**Also: Mike needs to resolve Conflict Register items CR1-CR4.**

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*Fetch: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
