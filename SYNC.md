# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-01 by Claude Code (ScatterplotCreator v1.0.10 built + STX Build 10 submitted)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟡 Build 10 in TestFlight | John reviews cyan+rings+centering | Claude Code |
| Goldmine | 🟢 Strata v3 approved + App Store design drafted | Mike reviews design docs before build | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning | Claude Code |
| ScatterplotCreator | 🟢 v1.0.10 built — word-break fix in both PDF templates | Distribute installer | Claude Code |

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

**What We Did This Session:**
- Fixed `word-break: break-word` on description cells in both pdf-template.html and pdf-template-v2.html — 400-char no-space strings now wrap instead of overflowing
- Bumped to v1.0.10, built portable + NSIS installer (both signed)

**What's Next:**
- [ ] Distribute v1.0.10 installer to users
- [ ] Await committee v2 approval ← BLOCKED
- [ ] Flip default to v2 when approved
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-01*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** BFX-06d | **Status:** submitted ✅
**Next agent:** mike
**Building:** John feedback — cyan archer + dark rings + two-digit score centering
**Gates:** 91 suites / 626 tests, tsc clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
- Mike: Review Build 10 on device (cyan archer, dark rings, centered scores)
- Mike: IAP product setup in App Store Connect ($14.99 non-consumable)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] John reviews Build 10 ← WAITING
- [ ] IAP product setup in App Store Connect
- [ ] B15a: named promo codes
- [ ] App Store submission when testing + IAP complete
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
