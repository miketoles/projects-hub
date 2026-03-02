# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-02 by Claude Code (ScatterplotCreator v1.0.10 — archive feature + BUG-008)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟡 Build 21 in TestFlight | Await John feedback on pinch zoom | Claude Code |
| Goldmine | 🟢 Strata v3 approved + App Store design drafted | Mike reviews design docs before build | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning | Claude Code |
| ScatterplotCreator | 🟢 v1.0.10 — archive feature + BUG-008 fix, active testing | Await committee v2 approval | Claude Code |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-02*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** BFX-06 | **Status:** submitted ✅
**Next agent:** mike
**Building:** John feedback — archer colors, pinch-to-zoom, ring label hide
**Gates:** 91 suites / 626 tests, tsc clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
- Waiting on John's feedback on Build 21 before any further work
- IAP product setup in App Store Connect ($14.99 non-consumable) — not yet done
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Fixed anchor-point pinch-to-zoom — content now stays pinned under fingers (Build 18)
- Bumped MAX_ZOOM 4→6→8 for deeper zoom range
- Fixed hardcoded `6` cap in pinch gesture (was ignoring MAX_ZOOM constant) — Build 21
- Documented EAS build→TestFlight one-liner workflow in spirit-logic-submit SUBMISSION-NOTES.md

**What's Next:**
- [ ] John reviews Build 21 ← WAITING
- [ ] IAP product setup in App Store Connect
- [ ] B15a: named promo codes before external TestFlight invites
- [ ] App Store submission when testing + IAP complete
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-03-02*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`
**Run:** `npm start`

<!-- DECISION_QUEUE_START -->
- Committee approval needed to flip v2 as default (1-line change in main.js)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Fixed v2 template column widths (BUG-008) — time/NP col now pinned to 12% of page, beh cols 9.5% each; readable at N=1
- Replaced Delete with Archive on patient list — patients move to archived.json, not lost
- Added Archived Patients screen with Restore + permanent Delete
- Fixed restore bug — patient list now re-renders on Back from archived screen
- All 100 tests passing throughout

**What's Next:**
- [ ] Mike testing v1.0.10 in active use ← IN PROGRESS
- [ ] Await committee v2 approval ← BLOCKED
- [ ] Flip default to v2 when approved (1-line change in main.js)
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
