# Sync File for Claude

*Last synced: January 28, 2026 by Claude Code*

---

## Current Focus

**Project:** Moon Rocks (Game Ideas)
**Path:** `~/dev/game-ideas/moon-rocks`
**Run:** `cd ~/dev/game-ideas/moon-rocks && python3 -m http.server 8001` → http://localhost:8001

---

## What We Did This Session

### Animation Work (Earlier)
- Extensive animation tuning (v33-v44) to get astronaut movement feeling right
- Fixed direction flipping bug caused by stale finger world coordinates
- Fixed "uncanny valley" leg movement - legs now stay under body with slight alternating spread
- Tuned body tilt, added arm swing, simplified to sine-based animation

### Game Development (v1-v21)
- Built full playable game from the v44 animation mockup
- Rock collection system with 6 rock types by rarity
- Oxygen system with drain/refill mechanics
- Detailed Lunar Module based on Apollo reference photos
- Auto-collect rocks, unlimited carrying, slam-dunk deposits while jumping
- Infinite terrain generation in both directions
- Added cute alien characters (from plush toy reference) that spawn in groups of 1-3, speak gibberish, run away when approached
- **Oxygen warning at 55%** - large animated "RETURN NOW" warning
- **Deposit HUD** - visor-style manifest showing each rock type deposited, sorted by total score, fades after 5 seconds
- **Apollo-style footprints** - ribbed bootprints appear on landing, proper perspective (foreshortened for side view), fade over ~30 seconds

---

## Current State (v21)

**Moon Rocks - Fully Playable:**
- Touch/click to move astronaut with lunar bouncy physics
- Auto-collect rocks, return to LM to deposit and refill O2
- Score based on rock rarity (Basalt 10pts → Meteorite 500pts)
- Blue/purple glow on collectible rocks
- Sound effects: breathing, rock pickup, lander arrival, deposits, alien speech
- Stars twinkle with color variation, Earth in sky
- Footprints appear on landing and fade over time

**Key Files:**
- `~/dev/game-ideas/moon-rocks/game.html` - Main game (v21)
- `~/dev/game-ideas/moon-rocks/STATUS.md` - Full documentation
- `~/dev/game-ideas/moon-rocks/reference/` - Apollo photos

---

## Technical Wins

1. **Finger tracking fix** - Store screen position, compute world position each frame
2. **Animation feel** - Sine-based curves, legs under body, arm swing opposite
3. **Footprint perspective** - Foreshortened ellipses with ribbed pattern for side-view
4. **HUD design** - Visor-style with scanlines, cyan glow, fades naturally

---

## Notes for Next Session

Game is in great shape! Possible next steps:
- More alien behaviors/interactions
- Achievement system
- Different lunar locations
- Rover vehicle
- Polish and share with grandson

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md*
