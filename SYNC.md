# Spirit Logic — Multi-Agent Sync File

*File last updated: 2026-02-27 (Multi-project session: roadmap updates, tech stack, committee decisions)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| NRT | 🟢 RBT Session spec v0.3 ready | RBT impl planning (Sunday) | Claude Code |
| STX Archery | 🟡 ADV-2 built | Claude review of Codex build | Claude Code |
| ScatterplotCreator | 🟡 v2 committee decisions captured | Build v1 Bx limit + v2 template (Sunday) | Claude Code |
| Spirit Logic Website | 🟢 Logo system complete | No action needed | Claude Code |
| Goldmine | 🟡 Runtime v1 live (hardening) | Extraction/noise tuning | Codex |

---

<!-- AGENT: Claude Code | PROJECT: NRT -->
## Claude Code — NRT
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/NRT`

<!-- DECISION_QUEUE_START -->
(none — all decisions resolved)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Added preferred tech stack to global CLAUDE.md (React 18, Vite, Tailwind, shadcn/ui, SQLite/Postgres/MS SQL)
- Added shadcn/ui adoption to F4 (UI/UX Polish) as project-wide component library
- Added `/web-ui-tasteful` + unicode animations as F3B (RBT module) build notes
- Updated F12 to include MS SQL as production DB option alongside PostgreSQL
- Added Puppeteer server-side PDF rendering to backlog

**What's Next:**
- [ ] RBT Session implementation planning sprint ← Sunday
- [ ] Fix 6 BLOCKING issues in NRT-INTELLIGENCE-DESIGN.md
- [ ] Phase D deploys when Craig IT responds
<!-- /AGENT: Claude Code | PROJECT: NRT -->

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
**Project:** STX Archery | **Cycle:** ADV-2 | **Status:** built
**Next agent:** claude
**Building:** Export consistency tests + multi-archer gating
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Review ADV-2 Codex build ← START HERE
- [ ] Await Apple Developer enrollment (DUNS pending) ← BLOCKER
- [ ] When enrolled: EAS Build → TestFlight → submission
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-02-27*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`

<!-- DECISION_QUEUE_START -->
(none — field limits resolved, CNA field test blocking v2 final approval)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Resolved all v2 committee decisions from Abby meeting (Bx limit 400, rationale 200, NP far left, dynamic sizing, instructions boxed, heading = patient only)
- Added v1 Bx description limit increase to 400 (Sally's request, ready to build)
- Added Electron printToPDF roadmap item to replace jsPDF
- v2 blocked on CNA field test (committee testing our v2 vs their Excel version)

**What's Next:**
- [ ] Build v1 Bx description 400-char limit ← Sunday
- [ ] Build v2 template into ScatterplotCreator ← Sunday
- [ ] Send v2 mockup PDF to Abby
- [ ] Await CNA field test results before v2 final approval
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
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Continue extraction/noise tuning using live worker counters ← START HERE
- [ ] Source-control polish across Mines / Lanes / Shafts
- [ ] Expand runtime source coverage in controlled increments
<!-- /AGENT: Codex | PROJECT: Goldmine -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
