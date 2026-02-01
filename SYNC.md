# Sync File for Claude

*Last synced: January 31, 2026 by Claude Code*

---

## Current Focus

**Primary:** NRT Scatterplot System - Building MVP

---

## What We Did This Session

### NRT Scatterplot App - Observation Model Refinement

Established the core philosophy for all NRT behavioral data: **"Was an observer present?"**

**Key Design Decisions:**

1. **3-State Database Model**
   - `1` = behavior occurred
   - `0` = observed, no behavior
   - No record = not observed
   - Eliminated -1, null, and special markers

2. **Row-Level Observation**
   - You can't partially observe an interval - you're either with the patient or not
   - If any cell in a row has data, ALL cells must have data (no partial rows)
   - Skip is a row-level action only

3. **Automatic Row Fill-In**
   - When user marks any cell, backend auto-fills other behaviors in that row with value=0
   - Example: User shades Bx3 → DB stores Bx1=0, Bx2=0, Bx3=1
   - Reasoning: If observer marked anything, they were present for all behaviors

4. **Row Consistency Enforced**
   - Can't clear individual cells in observed rows (converts to 0 instead of delete)
   - Only way to clear observed row is to skip entire row

**Files Updated:**
- `schema.sql` - value constraint: CHECK (value IN (0,1))
- `scatterplots.js` - auto-fill and row consistency logic
- `App.tsx` - updated cellToDbValue and buildGridFromData
- Design doc updated to v2.4 with full philosophy documentation

**Database Reset Required:** Deleted old DB files - new schema applies on next server start.

---

## NRT Status

**Location:** `~/dev/NRT/app-scatterplot/`
- `frontend/` - React app (port 5173)
- `backend/` - Express API (port 3001)

**To Run:**
```bash
cd ~/dev/NRT/app-scatterplot/backend && npm run dev
cd ~/dev/NRT/app-scatterplot/frontend && npm run dev
```

**Database:** `backend/data/nrt.db` (SQLite with WAL mode) - will be recreated on first run

**What's Working:**
- Full data entry flow with 3-state model
- Automatic row fill-in
- Row consistency enforcement
- Validation queue
- Multi-user switching (dev mode)
- Auto-save

**Still TODO:**
- Graphing/reporting (Phase 2)
- Notes entry UI
- Production auth (Windows AD)
- Export capabilities

---

## Key Files

| File | Purpose |
|------|---------|
| `~/dev/NRT/docs/NRT Scatterplot System Design.md` | Complete design (v2.4) |
| `~/dev/NRT/app-scatterplot/frontend/src/App.tsx` | Main React app |
| `~/dev/NRT/app-scatterplot/backend/src/routes/scatterplots.js` | API endpoints |
| `~/dev/NRT/app-scatterplot/backend/src/db/schema.sql` | Database schema |

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md and PROJECTS.md*
