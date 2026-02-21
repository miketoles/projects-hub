# Sync File for Claude

*Last synced: 2026-02-21 by Claude Code*

---

## Active Build

<!-- ACTIVE_BUILD_START -->
**STX Archery** — Device Hardening in progress. DH-B1 + DH-B2 complete, awaiting device verification of B2 fixes.
<!-- ACTIVE_BUILD_END -->

---

## Decision Queue

<!-- DECISION_QUEUE_START -->
- DH-05 Haptics still not firing on device — iOS 26 / debug build issue, needs dedicated debug session
- DH-06 Target transition animation — deferred to dedicated canvas pass
- Android B17 setup — can run in parallel with hardening, no DUNS needed. Start now?
- DUNS still pending — requested 2026-02-11, no Apple response yet
<!-- DECISION_QUEUE_END -->

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Run:** `cd ~/dev/3dArchery && npx expo run:ios --device`

---

## What We Did This Session

- First real-device testing session on iPhone 16 Pro Max (iOS 26.2.1)
- Found and logged 23 bugs across critical, high, and medium priority
- DH-B1: Fixed 15 of 16 bugs (free tier data loss, camera crash, scorecard, export naming, DNS for unshot targets, share card redesign, etc.)
- DH-B2: Fixed 8 more bugs (share card crash regression, promo code keyboard fix, airplane mode blank canvas, crosshair on share card target)
- Fixed handoff process bug: `handoff review` was reading stale `.codex-result.md` — now reads fresh `.codex-summary.md`
- Three-agent sync process fully verified across all agents
- Gates: 86 suites / 583 tests, tsc clean

---

## What's Next

- [ ] **Rebuild on device + verify DH-B2 fixes** ← START HERE (Mike testing)
  - Share card no longer crashes
  - Promo code accepts hyphens without smart punctuation
  - Airplane mode renders target correctly
  - Share card crosshair looks good
- [ ] **Continue device hardening checklist** — remaining untested sections
- [ ] **DH-B3** — collect any new bugs from B2 device verification, send to Codex
- [ ] **B17 Android setup** — Google Play Console, Maps API key, RevenueCat Android entitlement, EAS build

---

## Three-Agent Process

All agents use this file to stay in sync.

### Roles

| Agent | Role |
|-------|------|
| **Claude Code CLI** | Planner + reviewer. Writes specs, reviews builds, updates SYNC.md. |
| **Codex CLI / VS Code** | Builder. Fetches SYNC.md → reads HANDOFF.md → builds → reports back. |
| **Claude Mobile / Desktop / ChatGPT** | Brainstorming, planning, mobile continuity. |

### Sync Up — Start of Every Session

- **Primary:** `https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md` ← always fresh
- **Fallback:** `https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md` ← may be cached up to 12h

### Handoff Loop (Claude Code ↔ Codex)

1. Claude Code writes plan to `.codex-prompt.md`, runs `handoff send`
2. Codex fetches SYNC.md → reads HANDOFF.md → builds → runs gates
3. Codex updates HANDOFF.md with results + PROMPT FOR CLAUDE block
4. Claude Code reviews → approves or requests revision → syncs on session end

---

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟡 Device Hardening, DH-B2 built | Verify B2 on device |
| NRT Core | 🟡 Prototype working | Send zip to Ari |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test |
| SNF | 🔵 Design phase | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Primary: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
*Fallback: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
