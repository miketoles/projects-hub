# Sync File for Claude

*Last synced: February 8, 2026 by Claude Code*

---

## Current Focus

**Project:** NRT Core Prototype Installer + SNF Design
**Path:** `~/dev/NRT` and `~/dev/SNF`
**Run:** `./scripts/build-prototype.sh` → `prototypes/nrt-core-prototype.zip` (61MB)

## What We Did This Session

- Fixed prototype installer (5 cycles): CJS build, CORS fix, batch variable bugs, server diagnostics
- Tester-verified on Windows: unzip → start.bat → fully working (patients, doctors, CHSA, settings)
- build-prototype.sh now downloads Windows better-sqlite3 prebuild on Mac — no Windows build step
- Wrote comprehensive lessons to `tasks/lessons.md` (global + NRT-specific)
- Established mandatory lessons-check procedure for both Claude and Codex
- Drafted SNF design documents (DESIGN-DOC.md + CUSTOMER-DISCOVERY.md)

## Current State

NRT prototype installer is complete and working. Single Mac command builds a 61MB zip. Tester unzips and clicks start.bat. SNF design doc is drafted, pending customer call. All other projects unchanged from yesterday.

## What's Next

- [ ] Send updated zip to Ari for extended testing ← START HERE
- [ ] SNF customer call prep (review ~/dev/SNF/CUSTOMER-DISCOVERY.md)
- [ ] MikeText: runtime test Phase 4 on iPhone simulator, commit
- [ ] ScatterplotCreator: smoke test v1.0.3 on Windows, deploy

## Open Questions

- SNF facility contacted Mike — design doc ready, need to schedule the call
- NRT prototype lessons captured — future prototypes should build in one pass
- MikeText Phase 4 still uncommitted (pending runtime verification from yesterday)

## Notes for Mobile Session

Review SNF customer discovery questions before the call. Think about which module to propose first (survey readiness recommended in design doc as biggest market gap).

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| NRT Core | :green_circle: | Prototype working, send to tester |
| SNF | :yellow_circle: | Design doc drafted, schedule customer call |
| MikeText | :green_circle: | Runtime test Phase 4, then commit |
| ScatterplotCreator | :green_circle: | Smoke test on Windows, deploy v1.0.3 |
| Parkour Runner | :yellow_circle: | Phase 1 scaffolding ready to start |

---

*Fetch: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
