# Sync File for Claude

*Last synced: January 29, 2026 by Claude Code*

---

## Current Focus

**Project:** NRT Scatterplot System
**Path:** `~/dev/NRT`
**Design Doc:** `~/dev/NRT/docs/NRT Scatterplot System Design.md` (v2.2, 3345 lines)

---

## What We Did This Session

### Reviewed NRT Scatterplot System Design (v2.2)

Read the complete design document for the NRT Scatterplot System - the first module of the NRT Platform for Craig Hospital's Neurorehabilitation Team.

**The Problem:**
- Paper scatterplots → CentralReach transcription takes 10+ min per patient
- 96 intervals × 4 behaviors = 384 data points per patient per day
- Manual Excel graphing, tedious exports, thousands of clicks per week

**The Solution:**
- Click+drag "paint on" data entry (2 min per patient)
- Instant graphing with intervention annotations
- Export to PNG/PDF/Excel/PowerPoint
- 7-year data retention (BACB compliance)

**Key Design Elements:**

| Area | Details |
|------|---------|
| Data Entry | 96-interval grid, brush modes (Checkmark/Shaded/Clear), auto-save |
| Validation | Two-person workflow, error correction, re-validation, audit trail |
| Graphing | Frequency over time, heatmaps, before/after comparisons |
| Data Model | Patient, Behavior, ScatterplotSheet, Interval, ValidationError, ScatterplotNote |
| Auth | No login - reads Windows/AD identity via X-Remote-User header |
| Offline | IndexedDB auto-save, sync when online, conflict detection |

**Tech Stack (Lean Open-Source):**
- **Frontend:** React 18, Vite, TypeScript, Tailwind CSS
- **Backend:** Node.js, Express, better-sqlite3
- **Database:** SQLite (with SQLCipher for encryption)
- **Exports:** Recharts, ExcelJS, jsPDF, pptxgenjs

**Implementation Phases:**
0. Project Setup (Day 1)
1. Data Entry MVP (Week 1-2)
2. Validation (Week 2-3)
3. Basic Graphs (Week 3-4)
4. Full Graphing Suite (Week 4-5)
5. Reports & Polish (Week 5-6)
6. Production Hardening (Week 7-8)
7. Rollout & Feedback (Ongoing)

---

## Current State

**NRT Scatterplot System design is complete and ready to build.**

Key files:
- `~/dev/NRT/docs/NRT Scatterplot System Design.md` - Complete design (v2.2)
- `~/dev/NRT/mockup/quick-entry.html` - Reference mockup for data entry UI

**MikeText is ready for daily use** (completed previous session).

---

## Notes for Next Session

- NRT Scatterplot System ready to build with lean stack
- Start with Phase 0: Project Setup (create frontend/backend structure)
- MikeText window frame issue documented for later fix
- Shipwreck Explorer game plan at `~/.claude/plans/ticklish-wobbling-volcano.md`

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md*
