# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-25 (STX Archery PROMO-V2 approved)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟢 PROMO-V2 approved | Device test UX-P1 + PROMO-V2, then commit | Claude Code |
| NRT Scatterplot V2 | 🟢 Spec complete, Phase 1 GO | Committee decisions on D1/D6, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟢 v1.0.9 built, docs current | Deploy installer to production users | Claude Code |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 | Codex |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** PROMO-V2 | **Status:** approved ✅
**Next agent:** mike (device test + commit)
**Building:** Supabase promo code system — server-side one-time-use enforcement, redemption tracking
**Gates:** tsc PASS, 87/587 tests PASS — approved by CC architecture review
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
Ready for device testing. Two things to verify on device before committing:
1. UX-P1 changes — run through 11-item checklist in HANDOFF.md
2. PROMO-V2 — redeem a code (e.g. STX-LEGACY-FAMILY1), verify premium activates, check Supabase `promo_redemptions` table shows the row
Then commit everything and proceed to App Store prep.
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Confirmed Group A bugs (ME1-ME5, MD1) are already resolved from prior cycles
- Fixed MD2 app store copy ("drag to reposition" → "tap to reposition")
- Fixed ME4 line 1210: added __DEV__ console.error to silent saveActiveSession catch
- Set up Supabase CLI, deployed `redeem-promo` Edge Function, wrote `.env.local`
- PROMO-V2: Codex built app-side changes (promo.ts, usePremium.tsx, settings.tsx) — CC approved
- Rewrote `docs/PROMO-CODES.md` with full Supabase system documentation

**What's Next:**
- [ ] Device test UX-P1 (11-item checklist in HANDOFF.md) ← START HERE
- [ ] Device test PROMO-V2 (redeem code, verify Supabase row)
- [ ] Commit all changes (UX-P1 + PROMO-V2 + bug fixes)
- [ ] Await Apple Developer enrollment approval (DUNS obtained, submitted)
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: Process -->
## Claude Code — Global Process
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] No immediate action — process improvements are live
<!-- /AGENT: Claude Code | PROJECT: Process -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Deploy v1.0.9 installer to production users ← START HERE
- [ ] v2 template design — gate: committee D1/D6/D4 decisions
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
