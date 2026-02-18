# Sync File for Claude

*Last synced: Feb 17, 2026 by Claude Code*

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Branch:** main
**Run:** `cd ~/dev/3dArchery && npx expo run:ios`

## What We Did This Session

- Reviewed + approved B14a (GPS round tracking) and B14b (target location adjustment + GPS rounds indicator)
- Fixed splash screen + adaptive icon (were white placeholders, now navy/gold STX)
- Wrote full v1.0 completion plan: `docs/V1-COMPLETION-PLAN.md`
- Wrote full pricing + product strategy: `docs/PRICING-STRATEGY.md`
- Triangulated pricing with CC + Codex + ChatGPT — unanimous verdict: **$19.99 launch**
- Resolved all v1.0 build decisions (GPS checkpoints, promo label migration, free tier, Android)

## What's Next

- [ ] Archive `docs/ADVANCED-MANAGEMENT.md` + `docs/PREMIUM-FEATURES.md` to `docs/archive/` ← START HERE (5 min, no build)
- [ ] B15a: Promo code redesign (named codes + V5 migration for label column)
- [ ] B15b+c+d: GPS refactor (toggle + RDP simplification + checkpoint saves + resume merge)
- [ ] B16: Target photos (expo-image-picker + V5 migration)
- [ ] B17: Android / Google Play setup
- [ ] DUNS → Apple Developer enrollment → TestFlight → iOS submission

## Open Questions

- Free tier: 5 rounds (Mike confirmed) vs 7 rounds (Codex preferred) — Mike said 5, but worth one more thought
- Price raise trigger: Tiny Coach + 25-50 ratings + ≥3-5% paid conversion — all confirmed

## Notes for Mobile Session

- **Pricing is locked: $19.99 launch → $29.99 when Tiny Coach ships (with market gates)**
- Free tier = 5 rounds across all formats, full shot placement visible (not hidden behind paywall)
- The key build insight to ponder: B15b+c+d are one combined GPS cycle — GPS toggle, path simplification (RDP), and checkpoint saves at each target transition all go together
- "Session" in the codebase = a round of play — user-facing copy should always say "rounds"
- App Store subtitle locked: "Shot Placement. Course Maps. GPS Rounds."
- Best copy line: "Less than the cost of one arrow. Tracks every arrow you'll ever shoot."

## From Mobile Session

*(empty — paste mobile notes here)*

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟡 V1 planning done, building | Archive docs → B15a (promo) |
| NRT Core | 🟡 Prototype built | Send to Ari for testing |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test → L: drive |
| SNF | 🔵 Design doc ready | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Fetch (cache-busting): https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fetch (fallback): https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
