# Sync File for Claude

*Last synced: Feb 20, 2026 by Claude Code*

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Branch:** main
**Run:** `cd ~/dev/3dArchery && npx expo run:ios --device`

## What We Did This Session (Feb 20)

- Fixed **BFX-01: Vegas 3-spot 0-scoring** — `RingTarget` now renders rings at all 3 spot centers. Simulator verified ✅
- Fixed **BFX-02: NFAA Animal stop-on-hit** — auto-advances on first hit after 400ms. Simulator verified ✅
- Test baseline: **79 suites / 544 tests, tsc clean**

## What's Next

- [ ] **Phase F** — Export / PDF scorecard ← START HERE (PDF must match summary screen scorecard data — same `buildScorecardData()` source, confirmed)
- [ ] **NFAA Animal HIT feedback** — polish: bump delay to 700ms or add brief "HIT" overlay (deferred)
- [ ] **Phase G** — History / leaderboard
- [ ] **Phase H** — Test expansion
- [ ] **B17** — Android / Google Play setup (no DUNS required, can do now)
- [ ] **iOS submission** — Blocked on DUNS number (requested 2/11/2026, still pending)

## Open Questions / Notes

- Free tier limit is 7 sessions (confirmed in code)
- DUNS pending — iOS App Store submission blocked until it arrives
- Phase F: export PDF must match summary screen — `buildScorecardData()` and `scorecard-html.ts` scaffolding already exists, needs wiring to Export button

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
