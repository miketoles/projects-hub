# Sync File for Claude

*Last synced: 2026-02-21 by Claude Code*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle. Phase H complete ✅ (85 suites / 578 tests, tsc clean). Awaiting Device Hardening plan.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
- **Android setup (B17)** — no DUNS needed, can run in parallel with device hardening. Do it?
- **DUNS** still pending — requested 2026-02-11, no Apple response yet
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Run:** `cd ~/dev/3dArchery && npx expo run:ios`

---

## What We Did This Session

- Synced state at session start (no new implementation this session)
- Phase H fully complete: 85 suites / 578 tests, tsc clean (+5 suites, +30 tests vs baseline)
- All accumulated phase work committed — Phases F, W, H-Batch-1+2+3

---

## What's Next

- [ ] **Device Hardening** ← START HERE (see `docs/DEVICE-SMOKE-TEST-CHECKLIST.md`)
  - Cold start + kill+resume mid-round (schema v10 migration is a risk)
  - RevenueCat purchase + restore (HIGH RISK — never tested on real device)
  - Camera + GPS permissions, PDF share sheet on real iOS device
- [ ] **B17 Android setup** (can run in parallel — no DUNS required)
  - Google Play Console ($25), Maps API key, RevenueCat Android entitlement, EAS build
- [ ] **iOS Submission** — blocked on DUNS + hardening complete

---

## Open Questions / Notes

- Device Hardening is the last gate before iOS submission
- Three-agent process verified working across all clients

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟢 Phase H done, 85/578 tests | Device Hardening |
| NRT Core | 🟡 Prototype working | Send zip to Ari |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test |
| SNF | 🔵 Design phase | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Primary: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
*Fallback: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
