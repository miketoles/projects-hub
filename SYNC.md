# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-24*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT Scatterplot V2 | 🟢 Spec complete, Phase 1 GO | Committee decisions on D1/D6, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟢 v1.0.5 built, ready to ship | Windows QA item 4 (offline dialog), then deploy | Claude Code |
| STX Archery | 🟡 Testing phase | GPS trail walk test, DUNS pending | Claude Code |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 | Codex |

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-02-24*

<!-- ACTIVE_BUILD_START -->
**Project:** ScatterplotCreator | **Cycle:** 23 | **Status:** complete — v1.0.5 built, ready to deploy
**Next agent:** mike (deploy to users)
**Building:** v1.0.5 release — post-adversarial-review hardening (Phases 1–4) + doctor/BCBA orphan fix
**Gates:** 69/69 tests passing, icon restored, desktop shortcut fixed, QA items 1–3 and 5 confirmed
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did:**
- Ran full dual adversarial review — found 4 Critical + 8 High findings; built ROADMAP.md + IMPLEMENTATION_PLAN.md
- Phases 1–4 all built by Codex and CC-signed-off: 4 data-loss fixes, CSS unification, close-guard hardening, multi-template scaffold
- P4-3 DESIGN.md reconciliation complete — 7 sections updated (core contracts, save paths, close guard, data durability, etc.)
- v1.0.5 built: desktop shortcut always created, icon restored, doctor/BCBA orphan value fix added
- New Critical bug found (doctor renamed → edit form silently corrupted patient) — fixed in v1.0.5

**What's Next:**
- [ ] Test item 4: offline/L: drive → edit → close → verify new read-only dialog wording ← WHEN CONVENIENT
- [ ] Deploy v1.0.5 to production users
- [ ] v2 template design — gate: Mike approval required before starting
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

<!-- AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->
## Claude Code — NRT Scatterplot V2
*Last synced: 2026-02-22*

**Active Build:** No active build cycle — design/spec only, no code yet.
**Path:** `~/dev/NRT/docs/SCATTERPLOT_TEMPLATE_V2_DESIGN_SPEC.md`

**Decision Queue:**
- D1 — confirm exact shift boundary time with committee (7AM/7PM assumed)
- D6 — NP overwrite UX (overwrite-to-B vs block)

**What's Next:**
- [ ] Get committee confirmation on D1 and D6 ← START HERE
- [ ] Begin Phase 1 implementation: ScatterplotCreator v2 PDF template
<!-- /AGENT: Claude Code | PROJECT: NRT Scatterplot V2 -->

---

<!-- AGENT: Codex | PROJECT: Goldmine -->
## Codex — Goldmine
*Last synced: 2026-02-23*

**Active Build:** No active build cycle — spec hardening / calibration branch.

**What's Next:**
- [ ] Claude adversarial pass on `packet-r2` ← START HERE
- [ ] Rerun `design_first` on revised packet and compare output quality
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
