# Sync File for Claude

*Last synced: Feb 19, 2026 by Claude Code*

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Branch:** main
**Run:** `cd ~/dev/3dArchery && npx expo run:ios --device`

## What We Did This Session (Feb 19)

- Completed Phase E simulator validation — all 11 scorecard formats tested and passing
- Fixed WA Match Recurve "No match data available." — root cause was `buildMatchState` never existed; no code computed set points from arrow data
- Built `src/logic/scoring/build-match-state.ts` — new pure function, 8 tests
- Fixed v10 migration healing — `CREATE TABLE IF NOT EXISTS session_match_state` now runs unconditionally at startup
- Fixed legacy v9 backfill + explicit column SELECT to avoid match_state collision
- Pre-v1.0 cleanup sprint (Groups A–D): equipment filter exact-match bug, error handling, performance (N+1 query fix), dead code removal, doc archive/consolidation
- Test baseline: **79 suites / 539 tests, tsc clean**

## Phase E Results (all ✅)

1. IBO 3D, 2. ASA 3D, 3. NFAA Animal, 4. WA Indoor, 5. NFAA 300, 6. Vegas, 7. WA 720, 8. WA 1440, 9. NFAA Field, 10. WA Match Recurve, 11. WA Match Compound

## What's Next

- [ ] **Phase F** — Export / PDF scorecard
- [ ] **Phase G** — History / leaderboard
- [ ] **Phase H** — Test expansion
- [ ] **B17** — Android / Google Play setup (no DUNS required, can do now)
- [ ] **iOS submission** — Blocked on DUNS number (requested 2/11/2026, still pending)
- [ ] Vegas 3-spot 0-scoring bug (backlog)
- [ ] NFAA Animal stop-on-hit not enforced (backlog)

## Open Questions / Notes

- Free tier limit is 7 sessions (confirmed in code)
- DUNS pending — iOS App Store submission blocked until it arrives
- USB-C cable for real device testing — status unknown from last session

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟡 Phase E done, v1.0 nearly ready | Phase F (export/PDF) or Android setup |
| NRT Core | 🟡 Prototype built | Send to Ari for testing |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test → L: drive |
| SNF | 🔵 Design doc ready | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Fetch (cache-busting): https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fetch (fallback): https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
