# Sync File for Claude

*Last synced: February 1, 2026 by Claude Code*

---

## Current Focus

**Primary:** NRT Scatterplot System - Validation Workflow Refinement

---

## What We Did This Session

### NRT Scatterplot App - Major Validation Workflow Fixes (14 Bug Fixes)

**Critical Bug Fixes:**

1. **Validators can now see validation buttons** - Fixed mode priority logic (isValidation before isReadOnly)

2. **Validation mode works from any navigation path** - Added `effectiveIsValidation` computed from sheet status + `canValidate` from backend

3. **Changed rows detection fixed** - Use `modified_by === corrected_by` instead of timestamp comparison (timestamps failed due to row fill-in timing)

4. **Skipped rows (X) display correctly after submission** - Empty rows show as X (red) after submission, blank during Draft

5. **Cell-level editability in Corrections Review** - Only corrected cells are editable, verified cells are locked

**New Features:**

- Mode-based background colors: white (entry), light blue (validation), light orange (re-validation)
- Review column with "← Changed" markers for modified rows
- Banner shows "X cells verified • Y cells corrected (needs review)"
- Context-aware button text: "Confirm Corrections" vs "Mark as Validated"

**API Enhancements:**

- `canValidate` field in GET responses
- `changedCells` array (behaviorId + intervalIndex pairs)
- `verifiedCells` and `correctedCells` counts

**Open Questions (documented in design doc):**

1. Should re-validator be able to unlock all cells if they spot additional issues?
2. What if they notice errors in "verified" (locked) cells?
3. What's the escalation path for disagreements?

---

## NRT Status

**Location:** `~/dev/NRT/app-scatterplot/`
- `frontend/` - React app (port 5173)
- `backend/` - Express API (port 3001)

**To Run:**
```bash
cd ~/dev/NRT/app-scatterplot/backend && npm start
cd ~/dev/NRT/app-scatterplot/frontend && npm run dev
```

**Database:** `backend/data/nrt.db` (SQLite) - Fresh database with only dev users, no patients

**Design Doc:** v2.8 - Fully synchronized with implementation

**What's Working:**
- Full data entry flow with 3-state model
- Automatic row fill-in and row consistency
- Validation queue with proper permissions
- Corrections review with cell-level control
- Multi-user switching (dev mode)
- Auto-save
- Empty rows display as X after submission

**Still TODO:**
- Decide on Corrections Review open questions (unlock all? escalation path?)
- Notes entry UI
- Graphing/reporting (Phase 2)
- Production auth (Windows AD)

---

## Key Files

| File | Purpose |
|------|---------|
| `~/dev/NRT/docs/NRT Scatterplot System Design.md` | Complete design (v2.8) |
| `~/dev/NRT/app-scatterplot/STATUS.md` | Current status, 14 bug fixes |
| `~/dev/NRT/app-scatterplot/frontend/src/App.tsx` | Main React app |
| `~/dev/NRT/app-scatterplot/backend/src/routes/scatterplots.js` | API endpoints |

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md and PROJECTS.md*
