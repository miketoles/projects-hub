# Sync File for Claude

*Last synced: Feb 20, 2026 by Claude Code*

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Branch:** main
**Run:** `cd ~/dev/3dArchery && npx expo run:ios --device`

## What We Did This Session (Feb 20)

- Fixed **BFX-01: Vegas 3-spot 0-scoring** — `RingTarget` now renders rings at all 3 spot centers via `getSpotCenters()`. Root cause: renderer drew one bullseye at (175,175) while scoring engine checked offset centers → all arrows scored MISS.
- Fixed **BFX-02: NFAA Animal stop-on-hit** — wired `shouldStopOnHit()` in `handleArrowPlaced`; on first hit, `onAdvanceTarget()` fires after 400ms. Prevents scoring all 3 attempts when rules say advance on first hit.
- Test baseline: **79 suites / 544 tests, tsc clean** (+5 new tests)

## What's Next

- [ ] **Phase F** — Export / PDF scorecard ← START HERE
- [ ] **Phase G** — History / leaderboard
- [ ] **Phase H** — Test expansion
- [ ] **B17** — Android / Google Play setup (no DUNS required, can do now)
- [ ] **iOS submission** — Blocked on DUNS number (requested 2/11/2026, still pending)

## Open Questions / Notes

- Free tier limit is 7 sessions (confirmed in code)
- DUNS pending — iOS App Store submission blocked until it arrives
- USB-C cable for real device testing — status unknown

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟡 Pre-v1.0 bugs fixed, Phase F next | Phase F (export/PDF) |
| NRT Core | 🟡 Prototype built | Send to Ari for testing |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test → L: drive |
| SNF | 🔵 Design doc ready | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Fetch (cache-busting): https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fetch (fallback): https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
