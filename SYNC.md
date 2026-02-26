# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-26 (STX GPS+photos fully working; map type toggle added)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT | 🟢 Roadmap consolidated | Fix Intelligence design BLOCKING findings, then Codex builds | Claude Code |
| STX Archery | 🟢 GPS+photos verified on device | Await Apple Developer enrollment (DUNS pending) | Claude Code |
| Spirit Logic Website | 🟢 Logo system complete | No action needed | Claude Code |
| ScatterplotCreator | 🟡 v2 template prep | Field limits meeting, then build v2 | Claude Code |
| Goldmine | 🟡 Runtime v1 live (hardening) | Demotion/reopen UX polish | Codex |

---

<!-- AGENT: Claude Code | PROJECT: NRT -->
## Claude Code — NRT
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/NRT`

<!-- DECISION_QUEUE_START -->
(none — roadmap approved, Intelligence design fixes queued for Codex)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Fix 6 BLOCKING issues in NRT-INTELLIGENCE-DESIGN.md ← START HERE
- [ ] Write Codex implementation plan for Intelligence Phases 1–11
- [ ] Codex builds Intelligence Phases 1–11
- [ ] Phase D deploys when Craig IT responds
<!-- /AGENT: Claude Code | PROJECT: NRT -->

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios --device "MLT iPhone" --configuration Release`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Fixed camera permission bug that silently blocked photo capture on device
- Camera now falls back to photo library when unavailable (also fixes simulator testing)
- GPS trail zoom: proportional padding so trail fills map correctly (58 track points verified)
- Map type toggle: Map / Satellite / Hybrid switcher on Course Map card
- GPS premium gate in Settings + free rounds counter stale state fix

**What's Next:**
- [ ] Await Apple Developer enrollment (DUNS submitted, pending) ← BLOCKER
- [ ] When enrolled: Device ID → EAS Build → TestFlight → submission
- [ ] Pre-launch: truncate promo_redemptions in Supabase before App Store
- [ ] v2 backlog: NFAA Animal stop-on-hit, Vegas 3-spot scoring 0-bug
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`

<!-- DECISION_QUEUE_START -->
- Field limits meeting: patient-spec, behavior description, rationale char limits
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Field limits meeting: get char limits ← START HERE
- [ ] Build v2 template code
- [ ] Add template selector to Settings
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

<!-- AGENT: Codex | PROJECT: Goldmine -->
## Codex — Goldmine
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/goldmine`

<!-- DECISION_QUEUE_START -->
- When to merge `build/runtime-v1-fasttrack` into `main`
- Whether to add optional auth on read-only `/v1/*` endpoints
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Demotion/reopen UX polish ← START HERE
- [ ] Expand runtime source coverage
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
