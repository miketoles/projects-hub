# Sync File for Claude

*Last synced: January 28, 2026 by Claude Code*

---

## Current Focus

**Project:** Moon Rocks (Game Ideas)
**Path:** `~/dev/game-ideas/moon-rocks`
**Run:** `cd ~/dev/game-ideas/moon-rocks && python3 -m http.server 8001` → http://localhost:8001

---

## What We Did This Session

- **Built astronaut animation mockup** - Full 2.5D side-view astronaut with articulated limbs
- **Implemented finger-height hop control** - Touch high = big floaty bounds, touch low = quick hops (core mechanic!)
- **Tuned bounding gait** - Alternating feet, push-off motion, not bunny hop
- **Added organic variation** - Random hop strength, arm wobble, body squash/stretch
- **Fixed direction flipping** - Only changes direction when on ground, prevents mid-air glitching
- **Fixed lean direction** - Astronaut leans into movement both directions
- **Dynamic dust system** - More particles for harder landings
- **Updated GAME-IDEAS.md** with full animation implementation details

---

## Current State

**Moon Rocks Mockup:**
- Astronaut animation feels good - bouncy Apollo-style movement
- Finger height controls hop intensity (0.25x to 5x range)
- Bounding gait with alternating feet
- Organic variation makes it feel alive
- Lunar lander, flag, parallax mountains all in place
- Monochrome grey/black/white aesthetic

**Shipwreck Explorer:** (previous session)
- Core gameplay working
- Diver animations working with 2.5D flip

---

## Key Technical Details

**Moon Rocks Animation System:**
```javascript
// Finger height → hop intensity
const fingerYNorm = finger.y / canvas.height;  // 0 = top, 1 = bottom
hopIntensity = 4.5 - fingerYNorm * 4.25;       // 0.25x to 5.0x

// Only change direction when grounded
if (!astro.airborne) {
    // Can flip direction
}

// Organic variation each hop
astro.hopVariation = hopIntensity * (0.94 + Math.random() * 0.12);
astro.hopSpeedVar = 2.0 - hopIntensity * 0.35;  // Big = floaty, small = snappy
```

**2.5D Flip:** Scale X transitions through 0 for smooth turn animation
**Articulated Limbs:** Hip/knee angles for legs, shoulder/elbow for arms
**Body Squash:** Compresses on landing, stretches at apex

---

## Files Updated

- `~/dev/game-ideas/moon-rocks/astronaut-mockup.html` - Main animation mockup (v19)
- `~/dev/game-ideas/moon-rocks/index.html` - Cache busting redirect
- `~/dev/game-ideas/GAME-IDEAS.md` - Design doc with implementation details

---

## Reference Materials

Apollo footage gifs in `~/dev/game-ideas/moon-rocks/reference/`:
- bounce.gif, bounce2.gif, bounce3.gif - Bouncy walking
- bounce-jump.gif - Bigger jumps
- fall.gif, fall2.gif - Falling/stumbling

---

## Notes for Mobile Session

The astronaut animation is working well. Key insight: **finger height controls hop intensity** is a great zen mechanic - gives intuitive control over movement feel.

Next steps could be:
- Add the lunar rover
- Add rock collection
- Add oxygen system
- Or pivot to another game idea

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md | Mobile Claude fetches: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
