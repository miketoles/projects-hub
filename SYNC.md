# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-01 by Claude Code (STX Archery — Build 10 submitted, BFX-06d)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟡 Build 10 in TestFlight, awaiting John's review | Review archer colors + centering on device | Claude Code |
| Goldmine | 🟢 Strata v3 approved + App Store design drafted | Mike reviews design docs before build | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning | Claude Code |
| ScatterplotCreator | 🔴 Description limit 300→400 not reflected in PDF template | Fix pdf-template.html truncation | Claude Code |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-01*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** BFX-06d | **Status:** submitted ✅
**Next agent:** mike
**Building:** John feedback fixes — archer color + two-digit score centering
**Gates:** 91 suites / 626 tests, tsc clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
- Mike: Review Build 10 on device — cyan archer + dark rings + centered two-digit scores
- Mike: IAP product setup in App Store Connect ($14.99 non-consumable) — required before submission
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- BFX-06: Fixed two-digit score centering (measureText-based), archer color #4 iterated through amber→pumpkin→cyan→yellow→cyan+dark rings
- Added `archerRingColors` — permanent ~50% darker ring on every archer marker for readability against any target zone
- Committed all changes, built/submitted Builds 7–10 to TestFlight

**What's Next:**
- [ ] John reviews Build 10 (cyan + dark rings + centering) ← WAITING
- [ ] IAP product setup in App Store Connect
- [ ] B15a: named promo codes (before external TestFlight invites)
- [ ] App Store submission when testing + IAP complete
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-03-01*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`
**Run:** `npm start`

<!-- DECISION_QUEUE_START -->
- Committee approval needed to flip v2 as default (1-line change in main.js)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Fix pdf-template.html description truncation — raised to 400 chars in UI but PDF still truncates at 300 ← ACTIVE
- [ ] Await committee v2 approval ← BLOCKED
- [ ] Distribute v1.0.9 installer to users
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
