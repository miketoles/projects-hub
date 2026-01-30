# Sync File for Claude

*Last synced: January 30, 2026 by Claude Code*

---

## Current Focus

**Project:** NRT Scatterplot System
**Path:** `~/dev/NRT`
**Design Doc:** `~/dev/NRT/docs/NRT Scatterplot System Design.md` (v2.2, 3345 lines)

---

## What We Did This Session

### Reviewed Full Design Doc and Current State

1. Read the entire 3,345-line design document (v2.2)
2. Compared existing Next.js code vs design doc's lean stack
3. Reviewed the quick-entry.html mockup in detail

**Key Decision:** Mike wants to **rebuild from scratch** using the design doc's lean stack (React + Vite, Express, better-sqlite3) rather than continue with the existing Next.js/Prisma code.

---

## Critical: Preserve the Paint-It-In Interface

The quick-entry.html mockup at `~/dev/NRT/mockup/quick-entry.html` defines the exact interaction model. **This behavior must be preserved in the rebuild.**

### Core Behaviors to Keep

| Behavior | Description |
|----------|-------------|
| **Format painter drag** | Drag brush determined by starting cell's value, not toolbar |
| **Single click toggle** | IND ↔ ERR (shaded ↔ blank observed) |
| **Check column** | Row-level: ✓ checked / ✗ skipped. Blank when row has any IND |
| **Auto-promotion** | Marking a cell IND makes other cells in row become ERR |
| **Keyboard shortcuts** | I = Shaded, E = Check row, S = Skip row, C = Clear |

### State Model (from mockup)

```
grid[96][B] where B = number of behaviors (max 4)
Values: empty | ind | err | skip

rowStatus[96] where each row is: empty | checked | skipped
```

### Render Rules

1. If any cell in row is `ind`, check column is blank
2. If row status is `checked` and no `ind` cells, check column shows ✓
3. If row status is `skipped`, check column shows ✗ and all cells show ✗
4. ERR cells appear visually blank (ERR is data, not a glyph)

---

## Current State

**Design Doc:** Complete and ready to build (v2.2)

**Existing Code:** Next.js + Prisma (will be replaced)

**Mockup:** `~/dev/NRT/mockup/quick-entry.html` - authoritative reference for data entry UI

---

## Next Session: Rebuild with Lean Stack

When Mike returns, we'll start **Phase 0: Project Setup**:

- [ ] Create new project structure: `nrt-scatterplot/frontend/` + `backend/`
- [ ] Initialize Vite + React + TypeScript frontend
- [ ] Initialize Express + better-sqlite3 backend
- [ ] Create SQLite schema from design doc
- [ ] Set up Tailwind CSS
- [ ] Dev mode user picker for testing
- [ ] Port the ScatterplotGrid component (preserving paint-it-in behavior)

**Stack:**
- Frontend: React 18, Vite, TypeScript, Tailwind CSS
- Backend: Node.js, Express, better-sqlite3
- Database: SQLite (with SQLCipher for encryption later)
- No login - dev mode user picker, prod reads X-Remote-User header

---

## Key Files

| File | Purpose |
|------|---------|
| `~/dev/NRT/docs/NRT Scatterplot System Design.md` | Complete design (v2.2) |
| `~/dev/NRT/mockup/quick-entry.html` | Reference mockup - authoritative UI behavior |
| `~/dev/NRT/STATUS.md` | Project status |

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md*
