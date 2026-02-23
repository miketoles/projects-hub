# Sync File for Claude

*Last synced: 2026-02-23 by Codex (Goldmine sync)*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle for Goldmine (spec hardening / calibration branch).
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
- Goldmine: merge `spec/phase1-first-packet-calibration` into `main` now vs after one more `packet-r2` Claude critique pass
- Goldmine: require direct buyer voice + operator evidence before any `implementation_first` packet handoff
- Goldmine: decide whether to add `approved_with_conditions` packet status to template/spec
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** Goldmine
**Path:** `~/dev/goldmine`
**Branch:** `spec/phase1-first-packet-calibration`
**Run:** `cd ~/dev/goldmine` (docs/spec project; no app runtime yet)

---

## What We Did This Session

- Initialized and pushed `goldmine` to GitHub (`main`) and added lightweight Git workflow conventions (`main`, `spec/*`, `build/*`)
- Built the first real `Build Handoff Packet` calibration artifact for `healthcare-prior-authorization-automation-01`
- Ran Codex `design_first` calibration and captured a scored review (`accept_with_edits`)
- Ran Claude adversarial `critique_packet` review and captured scored reviews (including blocked-run handling + successful `r1` critique)
- Upgraded handoff spec/template with `critique_packet` support, stage-classified issues (`discovery blocker` / `design constraint` / `implementation/deployment hurdle`), and explicit constraint staging (HIPAA/BAA hosting is not a discovery blocker)
- Produced packet revisions `r1` and `r2`; `r2` now reflects stronger honesty and scoping (`ready_for_review`, not premature export approval)

---

## What's Next

- [ ] **Claude adversarial pass on `packet-r2`** — verify discovery blockers are reduced and stage classification still holds ← START HERE
- [ ] **Add direct operator evidence + buyer voice** — strengthen workaround/buyer claims before next `design_first` handoff
- [ ] **Rerun `design_first` (Codex + Claude)** on revised packet and compare output quality against the first calibration
- [ ] **Merge spec branch to `main`** if calibration loop looks stable enough for Phase 1 baseline

---

## Open Questions / Notes

- Goldmine process rule now explicit: deployment/compliance hurdles (for example HIPAA/BAA hosting) should not invalidate discovery-stage opportunity quality by default.
- Current best packet is `packet-r2`, but it still needs:
  - direct operator workflow evidence
  - one buyer voice / procurement signal
  - validated competitor/displacement evidence
- Claude `critique_packet` was high-value for packet quality; continue using it before `implementation_first`.

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| Goldmine | 🟡 Phase 1 spec hardening + packet calibration active | Claude critique on `packet-r2`, then buyer/operator evidence pass |
| STX Archery | 🟡 DH-B4 built, device test pending | GPS trail walk test + triage 10 items |
| NRT Core | 🟡 Prototype working | Send zip to Ari |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
