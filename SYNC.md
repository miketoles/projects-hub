# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-26 (NRT document consolidation complete, unified roadmap written)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT | 🟢 Roadmap consolidated | Fix Intelligence design BLOCKING findings, then Codex builds | Claude Code |
| STX Archery | 🟢 GEA-B committed | Device test GEA-B tomorrow | Claude Code |
| Spirit Logic Website | 🟢 Logo system complete | No action needed | Claude Code |
| ScatterplotCreator | 🟢 v1.0.9 built | Deploy installer to production users | Claude Code |
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

**What We Did This Session:**
- Created `docs/NRT-ROADMAP.md` — single source of truth for all NRT planning (Phase D, Intelligence 1–11, 13 future phases F1–F12+F3B)
- Archived 14 superseded docs + app-scatterplot/ to `docs/archive/`
- Ran adversarial reviews on roadmap (fixes applied) and Intelligence design (6 BLOCKING logged)
- Updated tasks/todo.md and SYNC.md to current state
- Deleted empty legacy/, moved mockup/ to archive

**What's Next:**
- [ ] Fix 6 BLOCKING issues in NRT-INTELLIGENCE-DESIGN.md (auth header, CORS PATCH, migration version, PDF parsing, cross-DB atomicity, re-ingest safety) ← START HERE
- [ ] Write Codex implementation plan for Intelligence Phases 1–11
- [ ] Codex adversarial review of implementation plan
- [ ] Codex builds Intelligence Phases 1–11
- [ ] Phase D deploys when Craig IT responds (everything else ready)
<!-- /AGENT: Claude Code | PROJECT: NRT -->

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-26*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
(none — committed, ready for device testing)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Device test GEA-B tomorrow (multi-bow select, bow notes, free rounds countdown, no 10-tap) ← START HERE
- [ ] GPS trail testing (walk a real round — still pending)
- [ ] Await Apple Developer enrollment (DUNS submitted, pending)
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

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
- [ ] v2 template — gate: committee D1/D6/D4 decisions
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
- When to merge `build/runtime-v1-fasttrack` into `main` as the new runtime baseline
- Whether to add optional auth on read-only `/v1/*` endpoints before broader sharing
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Demotion/reopen UX polish ← START HERE
- [ ] Continue extraction/noise tuning with live worker counters
- [ ] Expand runtime source coverage beyond 6 lanes / 14 shafts
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
