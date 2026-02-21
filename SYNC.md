# Sync File for Claude

*Last synced: 2026-02-21 by Claude Code*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
**STX Archery** — Phase H (Test Expansion) complete. Moving to Device Hardening.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
- Android setup (B17) — no DUNS needed, can run in parallel with device hardening. Do it?
- DUNS still pending — requested 2026-02-11, no Apple response yet
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Run:** `cd ~/dev/3dArchery && npx expo run:ios`

---

## What We Did This Session

- Reviewed and approved H-Batch-1 (VP/EQ/FT tests), H-Batch-2 (RSM/CUM), H-Batch-3 (SCO/MIG + IX display)
- Phase H fully complete: 85 suites / 578 tests, tsc clean (+5 suites, +30 tests vs baseline)
- Committed all accumulated phase work — Phases F, W, H-Batch-1+2+3 (97 files + 10 files)
- Reviewed full roadmap — Device Hardening is the next gate before iOS submission
- Using Claude Code CLI (VS Code plugin had memory/crash issues)
- Established and verified three-agent sync process across all models

---

## What's Next

- [ ] **Device Hardening** ← START HERE (see `docs/DEVICE-SMOKE-TEST-CHECKLIST.md`)
  - Cold start + kill+resume mid-round (schema v10 migration is a risk)
  - RevenueCat purchase + restore (HIGH RISK — never tested on real device)
  - Camera + GPS permissions, PDF share sheet on real iOS device
- [ ] **B17 Android setup** (can run in parallel — no DUNS required)
  - Google Play Console ($25), Maps API key, RevenueCat Android entitlement, EAS build
- [ ] **iOS Submission** — blocked on DUNS + hardening complete

---

## Three-Agent Process

All agents (Claude Code CLI, Claude Desktop, Claude Mobile, Claude VS Code plugin, ChatGPT, Codex CLI, Codex VS Code plugin) use this file to stay in sync.

### Roles

| Agent | Role |
|-------|------|
| **Claude Code CLI** | Planner + reviewer. Writes specs, reviews builds, updates SYNC.md. Never writes implementation code. |
| **Codex CLI / Codex VS Code** | Builder. Reads plan from HANDOFF.md, builds, reports back with PROMPT FOR CLAUDE block. |
| **Claude Mobile / Desktop / ChatGPT** | Brainstorming, planning, mobile continuity. Reads this file for context. |

### Sync Up — Start of Every Session

Every agent should fetch this file at session start:
- **Primary:** `https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md`
- **Fallback:** `https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md`

**Verified working on:** Claude VS Code plugin ✅, Claude Desktop ✅, Claude Mobile ✅, ChatGPT ✅, Claude Code CLI ✅

### Handoff Loop (Claude Code ↔ Codex)

1. Claude Code writes plan to `.codex-prompt.md`, runs `handoff send` from project dir
2. Codex fetches SYNC.md → reads HANDOFF.md in project root → builds
3. Codex runs gates (`npm test -- --watchAll=false` + `npx tsc --noEmit`)
4. Codex updates HANDOFF.md with build status + PROMPT FOR CLAUDE block
5. Claude Code reviews → approves or requests revision → updates SYNC.md on next sync

### Key Files

| File | Where | Purpose |
|------|-------|---------|
| `SYNC.md` | projects-hub repo | Cross-session, cross-agent context |
| `HANDOFF.md` | project root | Active build spec + history |
| `.codex-prompt.md` | project root | Current build prompt (gitignored) |
| `.codex-result.md` | project root | Codex last result (gitignored) |

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟢 Phase H done, 85/578 tests | Device Hardening |
| NRT Core | 🟡 Prototype working | Send zip to Ari |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test |
| SNF | 🔵 Design phase | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
