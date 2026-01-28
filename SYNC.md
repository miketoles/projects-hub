# Sync File for Claude

*Last synced: January 28, 2026 by Claude Code*

---

## Current Focus

**Project:** NRT (Neurorehabilitation Team Platform)
**Repo:** https://github.com/miketoles/NRT
**Path:** `~/dev/NRT`
**Run:** `cd ~/dev/NRT && npm run dev` → http://localhost:3000
**Demo logins:** admin@example.com / admin123, bcba@example.com / bcba123

---

## What We Did This Session

- **Fixed ScatterplotGrid click/drag logic** - Now matches the mockup exactly:
  - Single click toggles cells (IND ↔ ERR)
  - Drag uses "format painter" style (starting cell determines brush)
  - Check column now has full drag support
  - Added `hasDragged` tracking to distinguish click vs drag

- **Created Simple theme** in `/Users/miketoles/dev/UI Schemas/simple/`:
  - `simple-light.html` - White background, dark text (Day mode)
  - `simple-dark.html` - Black background, light text (Night mode)
  - `index.html` - Gallery page
  - Added to master UI Schemas index

- **Implemented day/night toggle in NRT**:
  - Added Simple themes to `globals.css`
  - Updated ThemeProvider with `toggleDayNight()` function
  - Navigation now has sun/moon icon toggle button
  - **simple-dark is the default** for development

- **Key design decision:** Grid cells are ALWAYS white with black text for readability, even in dark mode. Time column and headers follow the theme, but data entry cells stay white.

---

## Current State

**NRT Platform:**
- Scatterplot data entry working with correct click/drag behavior
- Day/night theme toggle functional
- Simple theme with clean black/white aesthetic
- Grid is always readable (white cells, visible grid lines)

**UI Schemas:**
- New "Simple" collection added with 2 themes
- Located at `~/dev/UI Schemas/simple/`

---

## What's Next

- [ ] Excel export for scatterplot reports
- [ ] Remove login requirement (AD/Windows auth)
- [ ] Flesh out DESIGN.md with TBI/ABA model details
- [ ] Test with real team members

---

## Open Questions / Mental Context

- Theme architecture is now solid - can easily add new color schemes
- Grid always stays readable regardless of theme choice
- Mike mentioned wanting to discuss a new game project

---

## Notes for Mobile Session

NRT is in good shape with working data entry and theming. Ready to pivot to discussing the new game project Mike mentioned.

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md | Mobile Claude fetches: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
