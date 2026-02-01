# Sync File for Claude

*Last synced: January 31, 2026 by Claude Code*

---

## Current Focus

**Primary:** NRT Scatterplot System - Building MVP

---

## What We Did This Session

### NRT Scatterplot App - Major Implementation Progress

Built a functional scatterplot data entry and validation system:

**Frontend (React + Vite + TypeScript + Tailwind):**
- Patient list with add patient form (max 4 behaviors enforced)
- Date selection screen with status badges (Draft, Awaiting Validation, Validated)
- Paint-it-in scatterplot grid (click+drag format painter behavior)
- Check column with drag support for row-level actions
- Validation queue showing sheets awaiting review
- Visual differentiation: blue banner for first review, orange for corrections review
- Changed row highlighting during re-validation
- User picker for dev/testing multi-user workflows

**Backend (Express + better-sqlite3):**
- SQLite database with full schema
- CRUD endpoints for patients, behaviors, scatterplot sheets
- Interval batch updates with auto-save
- Validation queue filtering (excludes your own work)
- Status management (Draft → NeedsValidation → Validated or NeedsRevalidation)

**Key Features Implemented:**
1. **Draft Status** - Users can start entry, leave, and come back without being locked out
2. **Validation Workflow** - Can't validate your own most recent changes
3. **Corrections Flow** - Validator edits → NeedsRevalidation → Someone else confirms
4. **Read-Only Mode** - Own submitted entries are view-only until validated
5. **Auto-Save** - All changes save automatically, no data loss on crashes

**Design Doc Updated (v2.3):**
- Added Draft status documentation
- Added date selection screen flow
- Added validation visual differentiation details
- Updated interval values to include skip (-1)
- Clarified 4-behavior limit enforcement

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

**Database:** `backend/data/nrt.db` (SQLite with WAL mode)

**What's Working:**
- Full data entry flow
- Validation queue
- Multi-user switching (dev mode)
- Auto-save
- Status transitions

**Still TODO:**
- Graphing/reporting (Phase 2)
- Notes entry UI
- Production auth (Windows AD)
- Export capabilities

---

## Key Files

| File | Purpose |
|------|---------|
| `~/dev/NRT/docs/NRT Scatterplot System Design.md` | Complete design (v2.3) |
| `~/dev/NRT/app-scatterplot/frontend/src/App.tsx` | Main React app |
| `~/dev/NRT/app-scatterplot/backend/src/routes/scatterplots.js` | API endpoints |
| `~/dev/NRT/app-scatterplot/backend/src/db/schema.sql` | Database schema |

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md and PROJECTS.md*
