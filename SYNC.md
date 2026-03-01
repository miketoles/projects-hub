# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-01 by Claude Code (ScatterplotCreator — v1.1 features shipped, v2 PDF working on Windows)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟡 Build 6 in TestFlight, John testing | Wait for John's feedback, then IAP setup | Claude Code |
| Goldmine | 🟢 Strata v3 approved + App Store design drafted | Mike reviews design docs before build | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning | Claude Code |
| ScatterplotCreator | 🟢 v1.0.9 shipped — all v1.1 features working on Windows | Await committee v2 approval to flip default | Claude Code |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-01*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** BFX-05 | **Status:** built ⏳
**Next agent:** claude
**Building:** Device testing bug batch #2 — awaiting CC review
**Gates:** 91 suites / 626 tests, tsc clean
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
- Mike: Gather John's feedback from Build 6 testing (Format Rules + archer colors)
- Mike: IAP product setup in App Store Connect required before App Store submission
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Built Format Rules feature — bottom sheet from create screen + shoot screen header tap (all 22 formats)
- Fixed archer 6 color: teal → hot pink (#E91E8C) — no longer clashes with archer 3 green
- Built + submitted Build 6 to TestFlight (build number auto-incremented to 6)
- Updated Gate 5 ✅ in submission pipeline

**What's Next:**
- [ ] Collect John's testing feedback on Build 6 ← WAITING
- [ ] IAP product setup in App Store Connect ($14.99 non-consumable)
- [ ] B15a: named promo codes (required before external TestFlight invites)
- [ ] App Store submission when testing complete
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: Goldmine -->
## Claude Code — Goldmine
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
**Project:** Goldmine | **Cycle:** 3 | **Status:** review-complete
**Next agent:** mike
**Building:** Infrastructure Signal Strata — adversarial review passed, implementation plan produced
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/goldmine`

<!-- DECISION_QUEUE_START -->
- Mike to review finished API Signal Strata design doc (v3) + implementation plan before build starts
- Mike to review App Store Opportunity Research design doc (v1)
- 4 open architectural decisions in Strata implementation plan
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Mike reviews both design docs ← START HERE
- [ ] Send App Store design to Codex for adversarial review
- [ ] Resolve 4 open decisions in Strata implementation plan
<!-- /AGENT: Claude Code | PROJECT: Goldmine -->

---

<!-- AGENT: Claude Code | PROJECT: NRT -->
## Claude Code — NRT
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/NRT`

<!-- DECISION_QUEUE_START -->
(none — all decisions resolved)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] RBT Session implementation planning sprint
- [ ] Fix 6 BLOCKING issues in NRT-INTELLIGENCE-DESIGN.md
- [ ] Phase D deploys when Craig IT responds
<!-- /AGENT: Claude Code | PROJECT: NRT -->

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
- Committee approval needed to flip v2 as default (1-line change in main.js: `|| 'v1'` → `|| 'v2'`)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Shipped Settings UI template version selector (v1/v2 toggle, persists)
- v1 description limit 300→400 chars (Sally confirmed at 2026-02-27 meeting)
- L-drive Phase 2: stale-data banner shows cache timestamp; Connection Status shows Last Cached
- v2 PDF via puppeteer-core (temp-file ASAR extraction) — pixel-perfect, confirmed working on Windows
- v2 instructions block: actual checked boxes NP☑ Y☑ N☑ matching data grid style, same font/weight/size

**What's Next:**
- [ ] Await committee v2 approval ← BLOCKED
- [ ] Flip default to v2 when approved (main.js `getTemplateVersion` fallback)
- [ ] Distribute v1.0.9 installer to users
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
