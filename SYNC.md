# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-04-02 by Claude Code (NRTTBI implementation plan ready, build begins)*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** NRTTBI (NRT for TBI)
**Path:** `~/dev/nrttbi`
**Run:** No code yet — Phase 0 (doc freeze) is next, then Phase 1 scaffold.

---

## What We Did This Session (Apr 1–2)

- NRTTBI: Created AGENTS.md (Codex instruction set for this repo)
- NRTTBI: Full adversarial review — role model cleanup (RBT+BCBA only, admin=flag), MSSQL language consistency
- NRTTBI: Defined ~45 new commands in command contract (full data-layer-first coverage)
- NRTTBI: Added sync protocol, clinical-day normalization, audit log commands, source enum fix
- NRTTBI: Created IMPLEMENTATION-PLAN.md — 13 phases, ~85 tasks, WAL sync engine task added
- NRTTBI: Reclassified IT green light as deployment gate only — build proceeds on local MacBook now

---

## What's Next

- [ ] Phase 0: Final Codex adversarial review (doc freeze gate) ← START HERE
- [ ] Phase 1: Cargo workspace + Tauri v2 + SvelteKit scaffold + migrations
- [ ] Phase 2: Repository trait pattern + all sqlx queries
- [ ] Run 15 BCBA questions through clinical team (parallel to build)

---

## Notes

- NRTTBI repo: https://github.com/miketoles/nrttbi.git
- Craig IT green light = deployment gate only, not build gate
- BCBA answers coming in informally — update bcba-questions.md as received
- High priority Qs: Q21 (Escalated events/BERT), Q17 (Preference assessments)

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| NRTTBI | 🟢 Build begins | Phase 0 doc freeze, then Phase 1 scaffold |
| Mission Control | 🟢 Phase 3 shipped | Radar Board shows updated status |
| FieldSketch | 🟡 Phase 1 built | Fix bugs #18-#21, then Phase 2 |
| STX Archery | 🟢 Build 9 in production | Monitor rollout |
| Field Photo Report | 🟡 Testing passed | Screenshots + submission |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
