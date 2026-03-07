# Lean v3 Runtime State

*Last updated: 2026-03-05*

This file is the cold-start recovery snapshot for the current Lean v3 runtime.
If either assistant appears to have lost context, read this file first.

---

## Current Architecture

Lean v3 now uses a runner + broker transport model for bidirectional execution.

- Runner: `/Users/miketoles/dev/lean_v3_full_test/lane.sh`
- Broker: `/Users/miketoles/dev/lean_v3_full_test/lane-broker.sh`
- Codex preamble: `/Users/miketoles/dev/lean_v3_full_test/.codex-preamble.md`
- Claude preamble: `/Users/miketoles/dev/lean_v3_full_test/.claude-preamble.md`
- Trigger table: `/Users/miketoles/dev/lean_v3_full_test/README.md`

Role prompts are transport-free.
Transport is owned by runner/broker.

Human decisions happen only at:
1. `PLAN_APPROVAL`
2. `FINAL_APPROVAL`

---

## Profiles

1. `claude-pr` = Claude Planner/Reviewer, Codex Builder
2. `codex-pr` = Codex Planner/Reviewer, Claude Builder

Optional override supported:
- `--planner-engine codex|claude`
- `--builder-engine codex|claude`
- `--reviewer-engine codex|claude`

---

## Natural-Language Trigger Contract

The active assistant should translate these phrases into runner commands automatically.

1. "Pass it to Claude to build"
   - `./lane.sh start --profile codex-pr --request "<objective>"`
2. "Pass it to Codex to build"
   - `./lane.sh start --profile claude-pr --request "<objective>"`
3. "Pass it to Codex to write an implementation plan"
   - `./lane.sh start --profile claude-pr --planner-engine codex --request "<objective>"`
4. "Looks good, have Claude build it" / "Looks good, have Codex build it"
   - `./lane.sh approve-plan`
5. "Ship it" / "approve final"
   - `./lane.sh approve-final`

No manual terminal relay should be required for routine transitions.

---

## Broker Autostart (macOS launchd)

Installed LaunchAgent:
- Label: `com.spiritlogic.lean-v3-broker`
- Env file: `/Users/miketoles/.config/lean-v3/claude-broker.env`
- Wrapper: `/Users/miketoles/.config/lean-v3/lean-v3-broker-daemon.sh`
- Plist: `/Users/miketoles/Library/LaunchAgents/com.spiritlogic.lean-v3-broker.plist`
- Logs:
  - `/Users/miketoles/Library/Logs/lean-v3/broker.out.log`
  - `/Users/miketoles/Library/Logs/lean-v3/broker.err.log`

Expected behavior:
- Starts at login (`RunAtLoad`)
- Restarts automatically (`KeepAlive`)
- Runs `./lane-broker.sh daemon --poll-sec 1` from `~/dev/lean_v3_full_test`
- Sources `CLAUDE_CODE_OAUTH_TOKEN` from the private env file outside any repo

---

## Health Checks

Run from any terminal:

```bash
launchctl print gui/$(id -u)/com.spiritlogic.lean-v3-broker
launchctl kickstart -k gui/$(id -u)/com.spiritlogic.lean-v3-broker
launchctl bootout gui/$(id -u) ~/Library/LaunchAgents/com.spiritlogic.lean-v3-broker.plist
tail -f ~/Library/Logs/lean-v3/broker.out.log ~/Library/Logs/lean-v3/broker.err.log
cd ~/dev/lean_v3_full_test && ./lane-broker.sh status
cd ~/dev/lean_v3_full_test && ./lane.sh status
```

Broker smoke jobs:

```bash
cd ~/dev/lean_v3_full_test
cat <<'EOF' >/tmp/claude-smoke.prompt.md
Reply EXACTLY: CLAUDE_BROKER_LIVE_OK
EOF
job_id=$(./lane-broker.sh enqueue --role reviewer --engine claude --prompt-file /tmp/claude-smoke.prompt.md --summary-file /tmp/claude-smoke.summary.md)
./lane-broker.sh run-until-done --job-id "$job_id" --timeout 45 --passive
cat /tmp/claude-smoke.summary.md
```

```bash
cd ~/dev/lean_v3_full_test
cat <<'EOF' >/tmp/codex-smoke.prompt.md
Reply EXACTLY: CODEX_BROKER_LIVE_OK
EOF
job_id=$(./lane-broker.sh enqueue --role planner --engine codex --prompt-file /tmp/codex-smoke.prompt.md --summary-file /tmp/codex-smoke.summary.md)
./lane-broker.sh run-until-done --job-id "$job_id" --timeout 45 --passive
cat /tmp/codex-smoke.summary.md
```

---

## Known Caveat

Interactive Claude login is not the reliable foundation for unattended broker work.
The launchd broker should use `CLAUDE_CODE_OAUTH_TOKEN` from the private env file.

Treat live broker smoke results as the primary truth. If broker Claude jobs fail with auth errors:

1. Refresh the token in `/Users/miketoles/.config/lean-v3/claude-broker.env`
2. Restart broker service:
   - `launchctl kickstart -k gui/$(id -u)/com.spiritlogic.lean-v3-broker`
3. Recheck with Claude smoke job

---

## Recovery Order (If Context Is Lost)

1. Read this file.
2. Read active prompt:
   - `/Users/miketoles/dev/projects-hub/CLAUDE_CODE_FOUNDATION_SETUP_PROMPT_LEAN_V3.md`
3. Read runtime implementation docs:
   - `/Users/miketoles/dev/lean_v3_full_test/README.md`
   - `/Users/miketoles/dev/lean_v3_full_test/AGENTS.md`
4. Verify broker and gate state:
   - `./lane-broker.sh status`
   - `./lane.sh status`

---

## Next Session Checklist (Carry Forward)

Updated after codex-pr smoke cycle on 2026-03-05.

Priority 1: codex-pr readiness hardening — COMPLETE
1. [x] `.codex-preamble.md` is role-neutral and includes codex-first trigger fallback command guidance.
2. [x] `lane.sh start` now archives stale `HANDOFF.md` and resets it before Planner stage.

Priority 2: codex-pr smoke validation — COMPLETE
1. [x] Full `codex-pr` cycle executed and closed:
   - `PLAN_APPROVAL: APPROVED`
   - `BUILD_COMPLETE: COMPLETE`
   - `REVIEWER_COMPLETE: COMPLETE`
   - `FINAL_APPROVAL: APPROVED`
2. [x] Validated both previously-untested paths:
   - Codex as Planner (full 14-section handoff packet)
   - Claude as Builder via broker (`claude -p`)
3. [x] Both profiles are now production-ready:
   - `claude-pr` and `codex-pr`

Priority 3: STX follow-up — OPEN
1. [ ] Resume STX Archery dangling items:
   - Android RC setup path
   - rebuild/upload sequence per existing STX notes
