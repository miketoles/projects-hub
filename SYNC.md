# Sync File for Claude

*Last synced: January 28, 2026 by Claude Code*

---

## Current Focus

**Project:** Shipwreck Explorer
**Path:** `~/dev/ShipwreckExplorer`
**Run:** `cd ~/dev/ShipwreckExplorer && python3 -m http.server 8000` → http://localhost:8000

---

## What We Did This Session

- **Fixed diver animation system completely** - abandoned front-view attempts, now pure side-view with 2.5D flip
- Fixed helmet orientation (viewport on positive X side = front after scale flip)
- Fixed arm positioning for side-view (tighter spread, proper layering)
- Fixed walking animation (forward lean 0.35 rad, arms in front with bent elbows)
- Fixed hammer swing direction (now swings DOWN from above head, not up)
- Made hammer head copper colored for visibility
- Fixed drawing order (belt before front arm so arms visible)
- Fixed knee bending direction in walking animation
- Updated design doc to v2.0 with all implementation details

---

## Current State

**Shipwreck Explorer:**
- Core gameplay working (explore, collect treasure, smash chests, deposit at boat)
- **Diver animations NOW WORKING** - 2.5D side-view with smooth flip transitions
- Animation states: swimming, floating/treading, walking on seafloor
- Hammer smash working with proper down-swing
- Fish schools, sharks, whales, air line all functional

---

## Key Technical Details

The diver animation system uses:
- `flipProgress` (0 = mid-turn, 1 = fully facing direction)
- 2.5D effect via `ctx.scale(scaleX, 1)` where scaleX transitions through 0
- Side-view drawing order: back arm → torso → harness → belt → front arm → legs → helmet
- Walking: fixed `ctx.rotate(0.35)` for forward lean, arms at shoulder angle 1.2
- Hammer uses LEFT arm angles (front arm after flip)

---

## Files Updated

- `ShipwreckExplorer.html` - Main game with fixed animations
- `ShipwreckExplorer-idea.md` - Design doc updated to v2.0
- `index.html` - Cache busting v=33

---

## Notes for Mobile Session

Diver animations are now working well. The key insight was:
1. Pure side-view only (no front-view attempts)
2. 2.5D flip using scale X through 0
3. Proper drawing order for layered limbs
4. Helmet viewport at positive X (front after flip)
5. Walking uses fixed rotation, not rotationMultiplier

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md | Mobile Claude fetches: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
