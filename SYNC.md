# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-25 (STX Archery PROMO-V2 planned)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | 🟡 PROMO-V2 planning | Mike: Supabase setup, then Codex builds | Claude Code |
| NRT Scatterplot V2 | 🟢 Spec complete, Phase 1 GO | Committee decisions on D1/D6, then build | Claude Code |
| NRT Core | 🟡 Prototype working | Send zip to Ari | Claude Code |
| ScatterplotCreator | 🟢 v1.0.9 built, docs current | Deploy installer to production users | Claude Code |
| Goldmine | 🟡 Packet calibration | Claude critique on packet-r2 | Codex |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-25*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** PROMO-V2 | **Status:** planning 📋
**Next agent:** mike (Supabase setup required before Codex build)
**Building:** Supabase-backed promo code system — server-side one-time-use enforcement, redemption tracking
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
Mike must set up Supabase before Codex can build. Steps in HANDOFF.md:
1. Create `promo_codes` + `promo_redemptions` tables (SQL in HANDOFF.md)
2. Add existing codes to `promo_codes` table
3. Deploy `redeem-promo` Edge Function (code in HANDOFF.md)
4. Add `.env.local` with `EXPO_PUBLIC_SUPABASE_URL` + `EXPO_PUBLIC_SUPABASE_ANON_KEY`
Then: send HANDOFF.md to Codex to build the app-side changes.
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- UX-P1 build (Codex) + CC architecture review → approved ✅
- Moved settings.test.tsx to src/__tests__/ — now discovered by Jest (87 suites / 587 tests)
- Investigated all Group A bugs: ME1, ME2, ME3 already fixed; ME5 already fixed (json_each in place)
- Fixed MD2: app store copy "drag to reposition" → "tap to reposition" (accurate)
- Fixed ME4 line 1210: added __DEV__ console.error to saveActiveSession silent catch
- Designed and wrote full PROMO-V2 plan in HANDOFF.md (Supabase schema, Edge Function, app changes)

**What's Next:**
- [ ] Mike: Supabase setup (tables + edge function + env vars) ← START HERE
- [ ] Mike: Device test UX-P1 (manual checklist in HANDOFF.md, 11 items)
- [ ] After Supabase ready: send HANDOFF.md to Codex for PROMO-V2 build
- [ ] After PROMO-V2: commit everything, then App Store prep
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
