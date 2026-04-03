# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-04-03 by Claude Code (NRTTBI design review — BCBA answers, role permissions, deferred questions)*

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

## What We Did This Session (Apr 3)

- Answered Q7 seed data (7/8 — session_type +4, clinical_event_category +4, only pref_assessment_type remains)
- Answered Q19 partially (Quick ABC unrestricted, demo mode desired, thresholds TBD)
- Closed Q20 (RBT + BCBA only, no nursing/CNA access)
- Updated screen permissions: Schedule, Session Live View, Reports, IOA, Check-In, Audit Log
- Added Q26 (standard protocol templates, v2) and Q27 (Learning Trees / RBT education, v2)
- Updated project-knowledge layer to reflect all changes

---

## What's Next

- [ ] Phase 0: Final Codex adversarial review (doc freeze gate) ← START HERE
- [ ] Phase 1: Cargo workspace + Tauri v2 + SvelteKit scaffold + migrations
- [ ] Run remaining BCBA questions: Q17 (pref assessments), Q21 (BERT/incidents — HIGH)
- [ ] IT questions (IT-1 through IT-6) — deployment gates, not build-blocking

---

## Notes

- NRTTBI repo: https://github.com/miketoles/nrttbi.git
- Open questions reduced from 11 to 9 (3 clinical + 6 IT)
- High priority: Q21 (Escalated events/BERT), Q17 (Preference assessments)
- Q7 closes fully when Q17 is answered (pref_assessment_type seed data)

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
