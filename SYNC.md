# Sync File for Claude

*Last synced: Feb 18, 2026 by Claude Code*

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Branch:** main
**Run:** `cd ~/dev/3dArchery && npx expo run:ios`

## What We Did This Session

- Reviewed B14c (BugCatcher) spec — CC + Codex joint design review
- Finalized BugCatcher architecture: registry/bridge pattern for snapshot access
- Updated V1-COMPLETION-PLAN.md: B14c inserted before B15a, items renumbered
- Copied BugCatcher-Spec-v3.3.md into repo docs (from iCloud Drive)
- All planning docs committed to 3dArchery main branch

## What's Next

- [ ] Archive `docs/ADVANCED-MANAGEMENT.md` + `docs/PREMIUM-FEATURES.md` to `docs/archive/` ← START HERE (5 min, no build)
- [ ] B14c: Build BugCatcher (install deps first: react-native-view-shot, jszip, expo-file-system, expo-sharing)
- [ ] B15a: Promo code redesign (named codes + V5 migration for label column)
- [ ] B15b+c+d: GPS refactor (toggle + RDP + checkpoint saves + resume merge)
- [ ] B16: Target photos, B17: Android/Google Play, then final gate pass

## Open Questions

- Error boundary: add one as part of B14c (gives captureFrame site), or defer to post-v1.0?
- Free tier: 5 rounds (Mike confirmed) — still worth 1 more thought vs 7 (Codex preferred)

## Notes for Mobile Session

- **BugCatcher is B14c — build it BEFORE the promo code redesign (B15a)**
- Key insight: BugCatcher `core.ts` is a singleton; can't call hooks. Uses registry pattern — shoot screen registers GPS/round bridge while mounted, root layout registers premium bridge. Core merges at capture time.
- `promoLabel` will be null in BugCatcher snapshots until B15a ships — that's OK, handle gracefully.
- Pre-build fix: spec's premium source enum (`purchase|promo|legacy|none`) must match code (`revenuecat|promo-code|legacy-code|dev-override|none`).

## From Mobile Session

*(empty — paste mobile notes here)*

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟡 V1 planning done, building | Archive docs → B14c (BugCatcher) |
| NRT Core | 🟡 Prototype built | Send to Ari for testing |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test → L: drive |
| SNF | 🔵 Design doc ready | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Fetch (cache-busting): https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fetch (fallback): https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
