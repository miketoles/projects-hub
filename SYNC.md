# Sync File for Claude

*Last synced: January 28, 2026 by Claude Code*

---

## Current Focus

**Project:** Moon Rocks (Game Ideas)
**Path:** `~/dev/game-ideas/moon-rocks`
**Run:** `cd ~/dev/game-ideas/moon-rocks && python3 -m http.server 8001` → http://localhost:8001

---

## What We Did This Session

- **Extensive animation tuning** - Many iterations (v33-v44) to get astronaut movement feeling right
- **Fixed direction flipping bug** - Was caused by stale finger world coordinates; now updates each frame
- **Fixed "uncanny valley" leg movement** - Legs now stay mostly under body with slight alternating spread
- **Tuned body tilt** - Reduced from ~24° to ~4.5° max to prevent "swimming" look
- **Added arm swing** - Arms now swing opposite to each other like natural walking
- **Simplified animation to sine-based** - Smoother than velocity-driven, less jerky

---

## Current State (v44)

**Moon Rocks Mockup - Working but still evaluating:**
- Astronaut bounces with legs mostly under body (center of gravity correct)
- Small leg spread alternates each hop (not tied-together look)
- Arms swing opposite to each other
- Knees bend 35-70° during hops
- Subtle body tilt (~4.5° max)
- Direction only changes when on ground
- Finger position properly tracks with camera movement

**Key Versions to Remember:**
- **v33** - First "safe" version after fixing major issues
- **v44** - Current version, not bad but Mike is still evaluating

**Still Evaluating:**
- Mike says "not bad" but wants to think about it
- May still have subtle uncanny valley quality
- Legs/movement feel is close but might need more tweaking

---

## Key Technical Details

**Current Animation System (v44):**
```javascript
// Sine-based smooth animation
const hp = astro.hopProgress;
const spread = Math.sin(hp * Math.PI);

// Small leg separation, alternates each hop
const legSign = foot === 0 ? 1 : -1;
const legSpread = spread * 0.12;  // ~7 degrees max
astro.leftHipAngle = -legSpread * legSign;
astro.rightHipAngle = legSpread * legSign;

// Knees bend equally
const kneeBend = 0.6 + spread * 0.6;  // 35-70 degrees

// Arms swing opposite
if (foot === 0) {
    astro.leftShoulderAngle = 0.1 + armSwing;   // Back
    astro.rightShoulderAngle = -0.3 - armSwing; // Forward
}
```

**Finger tracking fix:**
```javascript
// Store SCREEN position, compute world position each frame
state.finger.screenX = x;  // On touch/mouse events
// Then each frame:
state.finger.x = state.finger.screenX + state.camera.x;
```

---

## Files

- `~/dev/game-ideas/moon-rocks/astronaut-mockup.html` - Main mockup (v44)
- `~/dev/game-ideas/moon-rocks/index.html` - Cache busting redirect (v=44)
- `~/dev/game-ideas/moon-rocks/reference/` - Apollo bounce gifs for reference

---

## Notes for Mobile Session

Animation is close but Mike wants to think about it. The movement has been through many iterations trying to match Apollo footage feel. Key challenges were:
1. Legs looking like "ballet dancer" or "splits" - fixed by reducing hip angles
2. Center of gravity looking wrong - fixed by keeping legs under body
3. Direction flipping randomly - fixed by updating finger coords each frame
4. Uncanny valley feel - improved by using sine curves instead of velocity-driven

If continuing, look at the Apollo reference gifs and compare to current movement. The goal is "WHEEEEE!" not "WTF?".

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md*
