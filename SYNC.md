# Sync File for Claude

*Last synced: 2026-02-22 by Claude Code*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
- NRT Scatterplot V2: D1 — confirm exact shift boundary time with committee (7AM/7PM assumed; spec is parameterized via Appendix C)
- NRT Scatterplot V2: D6 — NP overwrite UX (overwrite-to-B vs block); backend defined, need committee UX confirmation
- NRT Scatterplot V2: D4 — rollout scope (all patients immediately vs new patients only)
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** NRT Core — Scatterplot Template V2 Design Spec
**Path:** `~/dev/NRT/docs/SCATTERPLOT_TEMPLATE_V2_DESIGN_SPEC.md`
**Run:** design/spec only — no code yet

---

## What We Did This Session

- Completed 4-round adversarial review cycle with Codex — spec is now v0.4, Phase 1 GO, Phase 2 GO
- Resolved all 6 must-resolve items from Review #3: backfill detection query, UNIQUE constraint, GET SQLITE_BUSY handling, deactivation policy, §5.1 `all` contradiction, notes content-fit
- Corrected D8: behavior definitions on BOTH pages (Day and Night identical), not Day-only
- Added Appendix C: `getV2TimeLabel` canonical algorithm + 13 golden test vectors
- Built HTML mock-up of v2 scatterplot (`docs/scatterplot-v2-mockup.html`) matching reference image with spec changes applied

---

## What's Next

- [ ] Get committee confirmation on D1 (shift boundary) and D6 (NP overwrite UX) ← START HERE
- [ ] Begin Phase 1 implementation: ScatterplotCreator v2 PDF template
- [ ] Phase 0: run DB migrations (ALTER TABLE statements from §2.2) in NRT Core
- [ ] Send prototype zip to Ari (still pending from prior session)

---

## Open Questions / Notes

- Spec v0.4 is at `~/dev/NRT/docs/SCATTERPLOT_TEMPLATE_V2_DESIGN_SPEC.md` — all Codex reviews in same `docs/` folder
- Mock-up at `~/dev/NRT/docs/scatterplot-v2-mockup.html` — open in browser, 2-page portrait layout
- D1 is the only remaining pre-Phase-1 risk; Appendix C parameterizes it cleanly if boundary changes

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| NRT Scatterplot V2 | 🟢 Spec complete, Phase 1 GO | Committee decisions on D1/D6, then build |
| NRT Core | 🟡 Prototype working | Send zip to Ari |
| ScatterplotCreator | 🟡 v1.0.4 built | Windows smoke test + deploy |
| STX Archery | 🟡 Testing phase | GPS trail walk test, DUNS pending |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
