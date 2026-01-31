# Sync File for Claude

*Last synced: January 30, 2026 by Claude Code*

---

## Current Focus

**Primary:** NRT Scatterplot System rebuild
**Secondary:** Game testing (Moon Rocks, Shipwreck Explorer, Bulldozer)

---

## What We Did This Session

### 1. Reviewed NRT Scatterplot System Design (v2.2)

Read the complete 3,345-line design document. Key decision made:

**Rebuild from scratch with lean open-source stack** instead of continuing with existing Next.js/Prisma code.

The mockup at `~/dev/NRT/mockup/quick-entry.html` defines the paint-it-in interface that MUST be preserved.

### 2. Started Game Servers for Testing

| Game | URL | Port |
|------|-----|------|
| Moon Rocks | http://localhost:8080 | 8080 |
| Shipwreck Explorer | http://localhost:8081 | 8081 |
| Bulldozer | http://localhost:8082 | 8082 |

### 3. Updated Project Hub Files

- ACTIVE.md - Added MikeText, updated NRT status, added games
- PROJECTS.md - Complete refresh with all current projects
- SYNC.md - This file

---

## NRT Rebuild Plan

**Stack:**
- Frontend: React 18 + Vite + TypeScript + Tailwind CSS
- Backend: Node.js + Express + better-sqlite3
- Database: SQLite (SQLCipher for encryption later)
- Auth: No login - dev mode user picker, prod reads X-Remote-User header

**Phase 0 (Next Session):**
- [ ] Create `nrt-scatterplot/frontend/` + `backend/` structure
- [ ] Initialize Vite + React + TypeScript
- [ ] Initialize Express + better-sqlite3
- [ ] Create SQLite schema from design doc
- [ ] Set up Tailwind CSS
- [ ] Dev mode user picker
- [ ] Port ScatterplotGrid (preserving paint-it-in behavior)

### Paint-It-In Interface (Critical to Preserve)

| Behavior | Description |
|----------|-------------|
| **Format painter drag** | Drag brush determined by starting cell's value, not toolbar |
| **Single click toggle** | IND ↔ ERR (shaded ↔ blank observed) |
| **Check column** | Row-level: ✓ checked / ✗ skipped. Blank when row has any IND |
| **Auto-promotion** | Marking a cell IND makes other cells in row become ERR |
| **Keyboard shortcuts** | I = Shaded, E = Check row, S = Skip row, C = Clear |

---

## Active Projects Summary

| Project | Status | Next Step |
|---------|--------|-----------|
| **NRT** | Design complete (v2.2) | Phase 0: Project setup |
| **MikeText** | Complete, daily use | None (maintenance only) |
| **Moon Rocks** | Playable (v21) | Fix mobile scaling |
| **Shipwreck Explorer** | Playable MVP (v33) | More content |
| **Bulldozer** | Feature complete | Grandson visits |
| **ScatterplotCreator** | In review | Stakeholder feedback |

---

## Key Files

| File | Purpose |
|------|---------|
| `~/dev/NRT/docs/NRT Scatterplot System Design.md` | Complete NRT design (v2.2) |
| `~/dev/NRT/mockup/quick-entry.html` | Paint-it-in interface reference |
| `~/dev/MikeText/DESIGN.md` | MikeText design and status |
| `~/dev/game-ideas/moon-rocks/STATUS.md` | Moon Rocks status |
| `~/dev/ShipwreckExplorer/STATUS.md` | Shipwreck status |

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md and PROJECTS.md*
