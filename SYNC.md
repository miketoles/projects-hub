# Sync File for Claude

*Last synced: January 28, 2026 by Claude Code*

---

## Current Focus

**Project:** Shipwreck Explorer
**Path:** `~/dev/ShipwreckExplorer`
**Run:** `cd ~/dev/ShipwreckExplorer && python3 -m http.server 8000` → http://localhost:8000

---

## What We Did This Session

- Fixed waterline position (lowered so whole boat visible)
- Fixed treasure/diver clipping through seafloor
- Made fins tapered properly (narrow ankle, wide toes)
- Made the Orca boat bigger (scale 2.4)
- Added auto-deposit treasure when near surface
- Hid hammer except during smash animation
- Fixed walking fin direction to point forward like feet

---

## Current State

**Shipwreck Explorer:**
- Core gameplay working (explore, collect treasure, smash chests, deposit at boat)
- Fish schools, sharks, whales, air line all functional
- **BROKEN: Diver animation system**

**The Problem:**
Multiple attempts to implement front-view (facing player when idle) vs side-view (swimming profile) all failed. The diver keeps looking wrong - limbs on one side, no smooth transitions, helmet not turning.

**Root Cause:**
The diver is drawn as a 2D side-view sprite. The bulldozer game works because it uses Three.js for actual 3D rotation. We tried pseudo-3D projection approaches but they didn't work.

---

## What's Next

Need fresh eyes on the animation system. Options to consider:
1. Switch to Three.js for the diver (like bulldozer)
2. Create completely separate front-view and side-view drawing functions
3. Simplify and keep diver always in side-view

---

## Open Questions / Mental Context

- Should study the bulldozer code more carefully to understand how it handles rotation
- The diver state now has viewAngle and targetViewAngle properties (may want to keep or remove)
- Animation code is in drawDiver() around line 3099
- ViewAngle update logic is around line 1656

---

## Notes for Mobile Session

Shipwreck Explorer gameplay is solid but diver animations need rework. Taking a break to get fresh perspective. When returning, consider whether to use Three.js like the bulldozer or find a simpler 2D solution.

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md | Mobile Claude fetches: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
