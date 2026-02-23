# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-22*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT Scatterplot V2 | 🟢 Spec complete, Phase 1 GO | Committee decisions on D1/D6, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟡 v1.0.4 built | Windows smoke test + deploy | Claude Code |
| STX Archery | 🟡 Testing phase | GPS trail walk test, DUNS pending | Claude Code |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 | Codex |

---

<!-- AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->
## Claude Code — NRT Scatterplot V2
*Last synced: 2026-02-22*

**Active Build:** No active build cycle — design/spec only, no code yet.
**Path:** `~/dev/NRT/docs/SCATTERPLOT_TEMPLATE_V2_DESIGN_SPEC.md`

**Decision Queue:**
- D1 — confirm exact shift boundary time with committee (7AM/7PM assumed; spec parameterized via Appendix C)
- D6 — NP overwrite UX (overwrite-to-B vs block); backend defined, need committee UX confirmation
- D4 — rollout scope (all patients immediately vs new patients only)

**What We Did:**
- Completed 4-round adversarial review cycle with Codex — spec is now v0.4, Phase 1 GO, Phase 2 GO
- Resolved all 6 must-resolve items from Review #3: backfill detection query, UNIQUE constraint, SQLITE_BUSY handling, deactivation policy, §5.1 contradiction, notes content-fit
- Corrected D8: behavior definitions on BOTH pages (Day and Night identical), not Day-only
- Added Appendix C: `getV2TimeLabel` canonical algorithm + 13 golden test vectors
- Built HTML mock-up of v2 scatterplot (`docs/scatterplot-v2-mockup.html`)

**What's Next:**
- [ ] Get committee confirmation on D1 and D6 ← START HERE
- [ ] Begin Phase 1 implementation: ScatterplotCreator v2 PDF template
- [ ] Phase 0: run DB migrations (ALTER TABLE statements from §2.2) in NRT Core
- [ ] Send prototype zip to Ari (still pending)

**Notes:**
- Mock-up at `~/dev/NRT/docs/scatterplot-v2-mockup.html` — 2-page portrait layout
- D1 is the only remaining pre-Phase-1 risk
<!-- /AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->

---

<!-- AGENT: Codex | PROJECT: Goldmine -->
## Codex — Goldmine
*Last synced: 2026-02-23*

**Active Build:** No active build cycle — spec hardening / calibration branch.
**Path:** `~/dev/goldmine`
**Branch:** `spec/phase1-first-packet-calibration`

**Decision Queue:**
- Merge `spec/phase1-first-packet-calibration` into `main` now vs after one more `packet-r2` Claude critique pass
- Require direct buyer voice + operator evidence before any `implementation_first` packet handoff
- Decide whether to add `approved_with_conditions` packet status to template/spec

**What We Did:**
- Initialized and pushed `goldmine` to GitHub (`main`) with lightweight Git workflow conventions
- Built first real Build Handoff Packet calibration artifact for `healthcare-prior-authorization-automation-01`
- Ran Codex `design_first` calibration — scored review: `accept_with_edits`
- Ran Claude adversarial `critique_packet` review — captured scored reviews including blocked-run handling + successful `r1` critique
- Upgraded handoff spec/template with `critique_packet` support and stage-classified issues
- Produced packet revisions `r1` and `r2`; `r2` reflects stronger honesty and scoping

**What's Next:**
- [ ] Claude adversarial pass on `packet-r2` — verify discovery blockers reduced, stage classification holds ← START HERE
- [ ] Add direct operator evidence + buyer voice to strengthen workaround/buyer claims
- [ ] Rerun `design_first` (Codex + Claude) on revised packet and compare output quality
- [ ] Merge spec branch to `main` if calibration loop looks stable

**Notes:**
- Current best packet is `packet-r2` but still needs: direct operator workflow evidence, buyer voice/procurement signal, validated competitor/displacement evidence
- Deployment/compliance hurdles (e.g. HIPAA/BAA hosting) should not invalidate discovery-stage opportunity quality by default
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
