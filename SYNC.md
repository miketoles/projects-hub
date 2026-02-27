# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-27 (Goldmine transition-history UX polish live on Railway)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT | 🟢 RBT Session spec complete | Adversarial review of Intelligence design + RBT Session spec | Claude Code |
| STX Archery | 🟢 GPS+photos verified on device | Await Apple Developer enrollment (DUNS pending) | Claude Code |
| Spirit Logic Website | 🟢 Logo system complete | No action needed | Claude Code |
| ScatterplotCreator | 🟡 v2 template prep | Field limits meeting, then build v2 | Claude Code |
| Goldmine | 🟡 Runtime v1 live (hardening) | Extraction/noise tuning with live counters | Codex |

---

<!-- AGENT: Claude Code | PROJECT: NRT -->
## Claude Code — NRT
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/NRT`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Created RBT Session Data Collection module spec (`core/docs/modules/RBT-Session.md`)
- Defined behavior taxonomy: CHSA categories vs scatterplot behaviors vs session behaviors
- Added BCBA Behavior Manager screen spec and session behavior API endpoints
- Updated roadmap F3B with spec reference

**What's Next:**
- [ ] Adversarial review: Intelligence design + RBT Session spec ← START HERE
- [ ] Fix 6 BLOCKING issues in NRT-INTELLIGENCE-DESIGN.md
- [ ] Write Codex implementation plan for Intelligence Phases 1–11
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
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
**Project:** Goldmine | **Cycle:** Runtime v1 Fast-Track Hardening | **Status:** live on Railway + hardening in progress 🟡
**Next agent:** Codex
**Building:** Runtime transition UX hardening, extraction/noise tuning, source-control polish, controlled expansion
**Gates:** Railway web/worker live ✅, HTTP Basic Auth + operator-key auth ✅, runtime hardening ongoing
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/goldmine`

<!-- DECISION_QUEUE_START -->
- When to merge `build/runtime-v1-fasttrack` into `main`
- Whether to add optional auth on read-only `/v1/*` endpoints
- Expand source coverage immediately after one more noise-tuning pass vs in parallel with control-panel polish
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Completed demotion/reopen UX polish for live Runtime v1:
  - transition reason prompts for ore/find/packet actions
  - selected `Ore` and `Find` transition-history panels in the UI
  - packet rows now show latest transition reason/timestamp context
- Added audit history endpoint for UI history surfaces: `GET /v1/audit-events?resource_type=&resource_id=`
- Extended ore/find/packet list payloads with transition context (`latest_transition_reason`, `latest_transition_at`)
- Deployed `goldmine-web` to Railway and validated live behavior with reversible ore/find transitions and recorded reasons
- Synced Goldmine roadmap/status/spec docs to mark this step complete and reprioritize next work

**What's Next:**
- [ ] Continue extraction/noise tuning using live worker counters (`snapshotItemsSkipped`, `dedupedSignalCandidates`) ← START HERE
- [ ] Add source-control polish across `Mines` / `Lanes` / `Shafts` (bulk actions, clearer gated/runnable status, optional read-only auth)
- [ ] Expand runtime source coverage beyond 6 lanes / 14 shafts in controlled increments
- [ ] Tighten `Refinery` from UI polish to stronger workflow gates (manual review states, assay/evidence linkage, portfolio readiness)
- [ ] Add cross-lane `Workflow Veins` coverage (2D lane × workflow-vein representation)
- [ ] Keep prior-auth packet calibration in parallel on `spec/phase1-first-packet-calibration` with `r6` hold gate intact (no `design_first` yet)

**Notes:**
- Runtime is live at `https://goldmine-web-production.up.railway.app`
- Entire site/API is behind HTTP Basic Auth; mutations additionally require `x-goldmine-key`
- UI message “Operator key required for actions” is expected; paste `GOLDMINE_OPERATOR_KEY` from Railway and click `Save Key`
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
