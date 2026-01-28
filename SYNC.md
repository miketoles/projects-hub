# Sync File for Claude

*Last synced: January 28, 2026 by Claude Code*

---

## Current Focus

**Project:** CR (Scatterplot Data Platform)
**Repo:** https://github.com/miketoles/CR
**Path:** `~/dev/CR`
**Run:** `cd ~/dev/CR && npm run dev` → http://localhost:3000
**Demo logins:** admin@example.com / admin123, bcba@example.com / bcba123

---

## What We Did This Session

- Improved sync workflow between Claude Code and Mobile Claude
- Restructured SYNC.md to be more focused (~60 lines vs 124)
- Added verification step to prevent placeholder patterns
- Created three clear commands: "update my sync file", "sync up", "catch me up"

---

## Current State

Phase 1 of CR is complete. Working app with:
- User authentication (NextAuth)
- Client/behavior management
- ScatterplotGrid (96 intervals, click+drag)
- REST API with SQLite database

Ready to start Phase 2 (offline sync).

---

## What's Next

- [ ] Phase 2: IndexedDB offline storage ← START HERE
- [ ] Background sync with retry logic
- [ ] Service worker for full offline support
- [ ] Sync status indicator in UI

---

## Open Questions / Mental Context

- Future auth change: switch to Windows/AD auth (no manual login) in Phase 4
- Thinking about sync conflict resolution strategy for Phase 2
- Need to decide: last-write-wins vs manual merge?

---

## Notes for Mobile Session

Would like to brainstorm the offline sync architecture for Phase 2.
Key questions:
- What happens when two devices edit the same session?
- How should conflicts be resolved?

---

## From Mobile Session

*[Paste notes here when returning to desktop]*

---

*For all projects: see ACTIVE.md | Fetch: raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
