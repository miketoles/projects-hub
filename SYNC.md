# Sync File for Claude

*Last synced: February 6, 2026 by Claude Code*

---

## Current Focus

**Project:** ScatterplotCreator (L-Drive Unavailable Handling)
**Path:** `~/dev/ScatterplotCreator`
**Run:** `npm start` (Electron app)

## What We Did This Session

- Reviewed and approved Codex's Phase 1 (Messaging + Error Handling), Phase 2 (Last-Known Snapshot), and Phase 3 (Support Diagnostics) implementations — all passed strict code review
- All acceptance criteria met across all 3 phases, no material findings
- Drafted email to users about Daniel's VMware/Okta credential issue (not the app)
- Confirmed both deferred Phase 1 items were also fixed by Codex in Phase 2 (persist-before-validate, retry/health-check race via promise queue)

## Current State

All 3 phases of L-drive unavailable handling are code-reviewed and approved. The patch is ready to ship. Features: graceful read-only mode on network disconnect, automatic detection/recovery (30s health check), last-known data cache for offline viewing, Connection Status + Copy Diagnostics in Settings for support triage.

## What's Next

- [ ] **Ship the L-drive patch** — build installer, distribute to users ← NEXT
- [ ] Full app review of ScatterplotCreator (security, code quality, UX) — plan first
- [ ] Return to Parkour Runner game (Phase 5 Combat parked)
- [ ] NRT Core: IT meeting Monday, continue triage feedback

## Open Questions

- When to schedule the full ScatterplotCreator app review
- Parkour Runner: pick up Phase 5 combat or revisit earlier phases first

## Notes for Mobile Session

The L-drive patch is fully reviewed and ready. Think about timing for the full app review vs getting back to the game. Daniel's credential issue email is drafted — send it out.

## From Mobile Session

*(empty — paste mobile notes here)*

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| ScatterplotCreator | :green_circle: | Ship L-drive patch, then full app review |
| Parkour Runner | :yellow_circle: | Phase 5 combat parked, resume when ready |
| NRT Core | :yellow_circle: | IT meeting Monday, collecting triage feedback |

---

*Fetch (cache-busting): https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fetch (fallback): https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
