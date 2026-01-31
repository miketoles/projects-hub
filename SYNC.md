# Sync File for Claude

*Last synced: January 31, 2026 by Claude Code*

---

## Current Focus

**Primary:** NRT Scatterplot System (docs cleaned up, ready to build)
**Secondary:** ScatterplotCreator (new build with Refresh button)

---

## What We Did This Session

### 1. NRT Documentation Cleanup

Implemented two-tier documentation structure:

**Tier 1 - Main Design Doc** (`NRT Scatterplot System Design.md`)
- Now 3,656 lines (added Continuity & Handoff Guide section)
- Comprehensive but not unwieldy

**Tier 2 - Operations Guide** (`NRT-OPERATIONS-GUIDE.md`)
- Raspberry Pi dev server setup
- Running Pi as production (alternative to IIS)
- Detailed continuity procedures
- CentralReach migration notes

**Archived:** Monday conversation guide moved to `docs/archive/`
**Deleted:** Redundant continuity files (merged into above)

### 2. ScatterplotCreator - Added Refresh Button

Problem identified: When two users have app open, User B doesn't see User A's new patients without closing/reopening.

Fix: Added 🔄 Refresh button to header that reloads patient list from shared data file.

**New build ready:**
- `~/dev/ScatterplotCreator/dist/NRT Scatterplot Creator Setup 1.0.0.exe`
- `~/dev/ScatterplotCreator/dist/NRT-Scatterplot-Creator.zip`

Updated DESIGN.md and STATUS.md to document the change.

---

## NRT Status

**Docs:** Complete and organized
**Code:** Not started yet - ready for Phase 0

**Phase 0 (Next):**
- Create `nrt-scatterplot/frontend/` + `backend/` structure
- Initialize Vite + React + TypeScript
- Initialize Express + better-sqlite3
- Create SQLite schema from design doc
- Port ScatterplotGrid (preserving paint-it-in behavior)

**Key reference:** `~/dev/NRT/mockup/quick-entry.html` defines paint-it-in interface

---

## Active Projects Summary

| Project | Status | Next Step |
|---------|--------|-----------|
| **NRT** | Docs complete | Phase 0: Project setup |
| **ScatterplotCreator** | New build ready | Deploy to stakeholders |
| **MikeText** | Complete, daily use | Maintenance only |
| **Moon Rocks** | Playable (v21) | Fix mobile scaling |
| **Shipwreck Explorer** | Playable MVP (v33) | More content |
| **Bulldozer** | Feature complete | Grandson visits |

---

## Key Files

| File | Purpose |
|------|---------|
| `~/dev/NRT/docs/NRT Scatterplot System Design.md` | Complete NRT design (3,656 lines) |
| `~/dev/NRT/docs/NRT-OPERATIONS-GUIDE.md` | Deployment/operations details |
| `~/dev/NRT/mockup/quick-entry.html` | Paint-it-in interface reference |
| `~/dev/ScatterplotCreator/dist/` | New installer ready to deploy |

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md and PROJECTS.md*
