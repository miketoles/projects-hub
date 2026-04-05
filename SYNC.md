# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-04-05 by Claude Code (NRTTBI process cleanup, folder restructure, design passes)*

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

## What We Did This Session (Apr 3-5)

- Answered BCBA questions: Q7 (7/8 seed data), Q19 (partial), Q20 (closed — RBT+BCBA only)
- Updated role permissions: RBT full on Schedule/Reports, BCBA full on Session Live View/IOA/Check-In
- Added SCC (Standard Celeration Chart) to reports, simplified ABC to 3 free-form text boxes
- Moved all design docs to docs/, kept CLAUDE/AGENTS/SYNC at root for build readiness
- Deduplicated process: single-source ownership, mandatory Edit Protocol, DESIGN-PASSES.md
- Enriched Schedule screen with My Day/Team View/Week View from NRT core prototype
- Added Q26 (protocol templates) and Q27 (Learning Trees) as deferred v2 questions
- Added Obsidian wiki links across all docs for graph navigation

---

## What's Next

- [ ] Schedule design pass — resolve multi-staff entries + conflict detection ← START HERE
- [ ] Session Live View mockup (Svelte + Tailwind, hardcoded data)
- [ ] Phase 0: final Codex adversarial review + DESIGN-PASSES.md gate
- [ ] Phase 1: Cargo workspace + Tauri v2 + SvelteKit scaffold + migrations

---

## Notes

- NRTTBI repo: https://github.com/miketoles/nrttbi.git
- Awaiting Ari's email reply on Q17 (preference assessments)
- Q21 (BERT/incidents) remains highest priority open question
- Folder structure ready for Tauri scaffold: docs/ for design, root for code

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| NRTTBI | 🟢 Build ready | Schedule design pass, then Phase 0 gate |
| Mission Control | 🟢 Phase 3 shipped | Radar Board shows updated status |
| FieldSketch | 🟡 Phase 1 built | Fix bugs #18-#21, then Phase 2 |
| STX Archery | 🟢 Build 9 in production | Monitor rollout |
| Field Photo Report | 🟡 Testing passed | Screenshots + submission |
| ScatterplotCreator | 🟢 v1.0.10 stable | Await committee v2 approval |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
