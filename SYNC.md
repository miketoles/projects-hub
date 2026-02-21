# Sync File for Claude

*Last synced: Feb 21, 2026 by Claude Code*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** Spirit Logic — Multi-Agent Process Redesign
**Path:** `~/dev/` (cross-project process work)
**Docs:** `~/dev/THREE-AGENT-PROCESS.md`, `~/dev/projects-hub/`

---

## What We Did This Session (Feb 21)

- Redesigned the three-agent process: two-tier model (Build Engine vs. Ruminators)
- Configured Claude Desktop MCP filesystem server → reads SYNC.md directly from disk
- Verified full Sync Up chain: CC-CLI writes → Desktop reads via MCP → Mobile sees via shared chat
- Updated `/sync` skill to include Active Build + Decision Queue sections
- Updated `handoff.sh` to auto-push build state after every send/review cycle
- Confirmed Claude Desktop custom instruction saved: "Sync Up" now works in any new chat

---

## What's Next

- [ ] **Test ChatGPT+ URL fetch** ← START HERE (verify passphrase with raw GitHub URL)
- [ ] **Update THREE-AGENT-PROCESS.md** — document two-tier model, Sync Up architecture, adversarial review mandate
- [ ] **STX Archery Phase F** — Export / PDF scorecard (scaffolding exists, needs wiring)
- [ ] **B17** — Android / Google Play setup (no DUNS required, can start now)

---

## Open Questions / Notes

- ChatGPT+ Sync Up: URL fetch likely works with browsing enabled — untested
- Claude Desktop "Sync Up" is now permanent via custom instructions + MCP filesystem
- handoff.sh auto-push: updates Active Build section after every Codex send/review cycle
- THREE-AGENT-PROCESS.md still needs updating to reflect today's architecture decisions

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟡 Pre-v1.0, Phase F next | Export / PDF scorecard |
| NRT Core | 🟡 Prototype built | Send to Ari for testing |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test → L: drive |
| SNF | 🔵 Design doc ready | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
