# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-26 (Goldmine Runtime v1 live hardening active, STX Archery GEA-B awaiting device test)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟢 GEA-B committed | Device test GEA-B tomorrow | Claude Code |
| Spirit Logic Website | 🟢 Logo system complete | No action needed | Claude Code |
| NRT Scatterplot V2 | 🟢 Spec complete | Committee D1/D6 decisions, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟢 v1.0.9 built | Deploy installer to production users | Claude Code |
| Goldmine | 🟡 Runtime v1 live (hardening) | Demotion/reopen UX polish | Codex |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
**Project:** namegen | **Cycle:** DR-01 (Design Doc Adversarial Review) | **Status:** reviewed
**Next agent:** claude
**Building:** **Task:** Adversarial review of DESIGN-DOC.md (version 0.1, pre-review draft)
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
(none — committed, ready for device testing)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Confirmed GEA-B fully implemented (all 5 UX issues resolved by Codex build)
- Added white-bird/green-text logo variant — now live on spiritlogic.dev
- Built full logo generation system: 2 clean source files, PIL scripts, LOGO-INSTRUCTIONS.md
- Created transparent-background black logo (Source B) for bold-stroke variants
- All logo files + instructions committed to spiritlogic repo

**What's Next:**
- [ ] Device test GEA-B tomorrow (multi-bow select, bow notes, free rounds countdown, no 10-tap) ← START HERE
- [ ] GPS trail testing (walk a real round — still pending)
- [ ] Await Apple Developer enrollment (DUNS submitted, pending)
- [ ] When enrolled: Copy Device ID → EAS Build → TestFlight → submission
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
**Project:** namegen | **Cycle:** DR-01 (Design Doc Adversarial Review) | **Status:** reviewed
**Next agent:** claude
**Building:** **Task:** Adversarial review of DESIGN-DOC.md (version 0.1, pre-review draft)
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Deploy v1.0.9 installer to production users ← START HERE
- [ ] v2 template — gate: committee D1/D6/D4 decisions
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

<!-- AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->
## Claude Code — NRT Scatterplot V2
*Last synced: 2026-02-22*

<!-- ACTIVE_BUILD_START -->
**Project:** namegen | **Cycle:** DR-01 (Design Doc Adversarial Review) | **Status:** reviewed
**Next agent:** claude
**Building:** **Task:** Adversarial review of DESIGN-DOC.md (version 0.1, pre-review draft)
<!-- ACTIVE_BUILD_END -->

<!-- DECISION_QUEUE_START -->
- D1 — confirm shift boundary time with committee (7AM/7PM assumed)
- D6 — NP overwrite UX (overwrite-to-B vs block)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Get committee confirmation on D1 and D6 ← START HERE
<!-- /AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->

---

<!-- AGENT: Codex | PROJECT: Goldmine -->
## Codex — Goldmine
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
**Project:** namegen | **Cycle:** DR-01 (Design Doc Adversarial Review) | **Status:** reviewed
**Next agent:** claude
**Building:** **Task:** Adversarial review of DESIGN-DOC.md (version 0.1, pre-review draft)
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/goldmine`

<!-- DECISION_QUEUE_START -->
- When to merge `build/runtime-v1-fasttrack` into `main` as the new runtime baseline
- Whether to add optional auth on read-only `/v1/*` endpoints before broader sharing
- Resume source expansion immediately after demotion/reopen UX polish vs after one more noise-tuning pass
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Built and deployed Goldmine Runtime v1 on Railway (`goldmine-web` + `goldmine-worker` + Postgres); validated end-to-end runs -> artifacts -> signals -> ore -> finds -> packet draft rows
- Reused and upgraded the existing `ui/` shell into a live operator dashboard with glossary-stage labeling and ordered pipeline sections
- Added live controls for `Lanes`, `Mines`, and `Shafts` (enable/disable) with reversible Railway validation
- Added stage homes for `Veins`, `Assays`, `Refinery`, `Portfolio`, and `Build Handoff Packets`
- Implemented demotion/reopen paths for `Ore`, `Finds`, and `Build Handoff Packets`
- Added manual `Refinery` classification overrides (save/clear) and validated propagation to `Refinery` + `Portfolio`
- Added global HTTP Basic Auth on `goldmine-web` (static UI + all `/v1/*`) while retaining `x-goldmine-key` for mutations
- Expanded live runtime coverage to `6 lanes / 14 shafts` (`Health services`, `Technology`, `Insurance`, `Retail`, `Banking and capital markets`, `Real estate`)
- Hardened worker extraction/noise handling (anti-bot/captcha/access-denied/boilerplate detection, skip-extraction manifests, per-artifact dedupe/caps, live counters)
- Polished `Refinery` workflow UX: proxy/manual/review-queue filtering, review-cue badges and click-through from `Refinery`/`Portfolio`, clean manual rationale vs evidence-basis separation

**What's Next:**
- [ ] Demotion/reopen UX polish (reason prompts, packet transition polish beyond `draft` reopen, clearer UI affordances/history) ← START HERE
- [ ] Continue extraction/noise tuning with live worker counters (`snapshotItemsSkipped`, `dedupedSignalCandidates`) and source-specific heuristics
- [ ] Add control-panel polish across `Mines` / `Lanes` / `Shafts` (bulk actions, clearer gated/runnable status, optional read-only auth)
- [ ] Expand runtime source coverage beyond 6 lanes / 14 shafts in controlled increments (row-by-row from `V0-SOURCE-SCOPE-DETAILS.md`)
- [ ] Tighten `Refinery` from UI polish toward workflow rigor (manual review states, NUGGET evidence/assay linkage, non-proxy portfolio readiness gates)
- [ ] Add cross-lane `Workflow Veins` coverage (2D lane × workflow-vein representation)
- [ ] Keep prior-auth packet calibration in parallel on `spec/phase1-first-packet-calibration`, but maintain the current `r6` hold gate (no `design_first` yet)

**Notes:**
- Goldmine Runtime v1 is live on Railway and working; `goldmine-web` is protected by HTTP Basic Auth and mutating routes also require `x-goldmine-key`
- Prior-auth packet calibration remains active on a separate branch (`spec/phase1-first-packet-calibration`) with `packet-r6` hold gate still in effect pending higher-confidence overlap validation
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
