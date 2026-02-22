# Sync File for Claude

*Last synced: 2026-02-21 by Claude Code*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** DH-B4 | **Status:** built — awaiting device test (GPS trail)
**Next agent:** mike (device test) → then commit pass
**Building:** GPS walk trail fix + Map Course hidden + settings fixes (redeem reset, mode label)
**Gates:** 86 suites / 583 tests, tsc clean ✅
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
- 10 bugs/items from today's testing session — discuss tomorrow: v1 vs v1.1 priority
- GPS walk trail device test pending (need outdoor space, daytime)
- DUNS still pending — no Apple response yet
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Run:** `cd ~/dev/3dArchery && npx expo run:ios --device`

---

## What We Did This Session

- Full device testing sprint on iPhone 16 Pro (DH-B2 + B3 + B4)
- DH-B3: Fixed tap-7 scroll blocking developer options unlock at tap 10
- DH-B4: Fixed GPS walk trail (two root causes), hid Map Course feature, settings mode label + redeem reset
- Clarified GPS architecture: v1 = walk trail polyline only, target pins deferred to v1.1
- Logged 10 new items from device testing for tomorrow's triage

---

## What's Next

- [ ] **GPS walk trail device test** — unplug phone, walk a round, check gold polyline on summary ← START HERE
- [ ] **Triage 10 new items** — v1 vs v1.1 (PDF URL, archer names, JSON premium flag, target transition jank, etc.)
- [ ] **Commit pass** — large backlog: Phase H, F, W, DH-B1/B2/B3/B4 all uncommitted
- [ ] **DUNS follow-up** — Apple Developer enrollment blocked

---

## Open Questions / Notes

- 10 items from today's testing (full list in session):
  1. PDF footer URL: `spiritlogic.app` → `stx-archery.com`
  2. Archer names missing in regular rounds (works in quick practice)
  3. Exported JSON shows `free-tier-start-approved` even for premium
  4. Target transition jank (circle redraws before animal appears)
  5. Animal slide transition jarring
  6. Practice shoot back-nav lands on quick shoot screen — correct?
  7. Custom round — confirm categories/format/target type match design
  8. Share card colors don't match app navy/gold (v1.1)
  9. Edit arrow hidden under thumb — needs elegant precision solution (v1.1)
  10. Animal backgrounds inconsistent color — needs image regen (v1.1, white tail deer = reference)

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟡 DH-B4 built, device test pending | GPS trail walk test + triage 10 items |
| NRT Core | 🟡 Prototype working | Send zip to Ari |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
