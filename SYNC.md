# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-27 (STX Archery: adversarial review complete, pre-production ready)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| Goldmine | 🟢 Strata v3 approved + App Store design drafted | Mike reviews design docs before build | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning (Sunday) | Claude Code |
| STX Archery | 🟢 Adversarial review complete, 90 suites/604 tests | Mike: credentials + device test | Claude Code |
| ScatterplotCreator | 🟡 v2 committee decisions captured | Build v1 Bx limit + v2 template (Sunday) | Claude Code |
| Spirit Logic Website | 🟢 Logo system complete | No action needed | Claude Code |

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
- Mike to review App Store Opportunity Research design doc (v1) — send to Codex for adversarial review?
- 4 open architectural decisions in Strata implementation plan (lane tie-break, liveness priority, badge mapping, runtime budget)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Completed 3-cycle adversarial review of API Signal Strata design (v1→v2→v3, 14→3→0 blockers)
- Key v3 change: moved strata processing to web process, eliminating fetch_jobs FK and worker starvation issues
- Codex produced 8-phase implementation plan at `docs/upgrade-designs/api-signal-strata-implementation-plan.md`
- Researched app store data sources (iTunes Search API, Apple RSS, google-play-scraper, DataForSEO)
- Drafted App Store Opportunity Research design doc at `docs/upgrade-designs/app-store-opportunity-research.md`

**What's Next:**
- [ ] Mike reviews both design docs ← START HERE
- [ ] Send App Store design to Codex for adversarial review
- [ ] Resolve 4 open decisions in Strata implementation plan
- [ ] Begin Strata Phase 1 build (schema + migration)
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
- [ ] RBT Session implementation planning sprint ← Sunday
- [ ] Fix 6 BLOCKING issues in NRT-INTELLIGENCE-DESIGN.md
- [ ] Phase D deploys when Craig IT responds
<!-- /AGENT: Claude Code | PROJECT: NRT -->

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** ADV-2 | **Status:** approved ✅
**Next agent:** mike
**Building:** Pre-production adversarial review complete — waiting on credentials + device test
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
- Mike: Create RevenueCat products + set EAS secrets (iOS + Android API keys)
- Mike: Create Google Maps API key in Google Cloud Console
- Mike: Get Apple Team ID + create App Store Connect API key
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Committed 7 pending export fixes (multi-archer PDF, share card crash, branding URL)
- ADV-1: Custom rounds + Quick Shoot test coverage (Codex handoff, 10 new tests)
- ADV-2: Export consistency tests + multi-archer gating (Codex handoff, 7 new tests)
- App config: ITSAppUsesNonExemptEncryption, EAS production profile
- Store metadata: iOS + Android en-US files written to spirit-logic-submit
- Smoke test checklist: added Quick Shoot + Custom Round sections
- Baseline: 90 suites / 604 tests, tsc clean

**What's Next:**
- [ ] RevenueCat products + API keys → EAS secrets ← START HERE
- [ ] Google Maps API key → EAS secrets
- [ ] Apple Team ID + ASC API key
- [ ] Dev build + device smoke test (23 sections)
- [ ] Screenshots from TestFlight build
- [ ] Submission pipeline gates 1-11
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`

<!-- DECISION_QUEUE_START -->
(none — field limits resolved, CNA field test blocking v2 final approval)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Build v1 Bx description 400-char limit ← Sunday
- [ ] Build v2 template into ScatterplotCreator ← Sunday
- [ ] Await CNA field test results before v2 final approval
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
