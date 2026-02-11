# 🎯 Mike's Projects Hub

Central command for all my projects. Enables seamless context-switching between computer and phone.

## How This Works

```
┌─────────────────┐         ┌─────────────────┐
│  Claude Code    │         │   Claude.ai     │
│  (Computer)     │◄───────►│   (Phone)       │
│                 │  GitHub  │                 │
│  - Write code   │  Sync   │  - Brainstorm   │
│  - Update files │         │  - Plan         │
│  - Build stuff  │         │  - Write docs   │
└─────────────────┘         └─────────────────┘
         │                          │
         ▼                          ▼
    ┌─────────────────────────────────────┐
    │         Projects Hub (GitHub)        │
    │                                       │
    │  SYNC.md ← Current context           │
    │  ACTIVE.md ← Hot projects            │
    │  PROJECTS.md ← Everything            │
    └─────────────────────────────────────┘
```

## Quick Reference

| File | Purpose | When to Update |
|------|---------|----------------|
| `SYNC.md` | Current context for mobile sessions | Before leaving computer |
| `ACTIVE.md` | What's actively being worked on | When priorities change |
| `PROJECTS.md` | Master index of all projects | When adding/completing projects |

**Current focus (Feb 11):** STX Archery Phase A complete (Steps 1-7), Codex building Step 8 overnight

## Templates

Standard files for every project:

| Template | Purpose |
|----------|---------|
| `CLAUDE.md` | Context for Claude Code - project overview, architecture, commands |
| `FORMIKE.md` | Learning document - plain language explanations, lessons, bugs |
| `STATUS.md` | Quick status - what's done, what's next, blockers |

## Workflows

### Starting a Mobile Session

1. Tell Claude.ai: "Fetch my sync file at github.com/USER/projects-hub/blob/main/SYNC.md"
2. Claude reads current context
3. Continue brainstorming/planning where you left off

### Before Leaving Computer

Tell Claude Code:
> "Update my sync file and push to GitHub"

Claude will:
1. Update SYNC.md with current session context
2. Commit and push to this repo

### Starting a New Project

1. Create repo
2. Copy templates: `CLAUDE.md`, `FORMIKE.md`, `STATUS.md`
3. Fill in project basics
4. Add to `PROJECTS.md`
5. If actively working on it, add to `ACTIVE.md`

### Completing a Project

1. Update `FORMIKE.md` with final lessons learned
2. Move from Active to Completed in `PROJECTS.md`
3. Remove from `ACTIVE.md`
4. Celebrate! 🎉

## File Locations

```
projects-hub/
├── README.md          # You are here
├── SYNC.md            # Mobile session context
├── ACTIVE.md          # Currently active projects
├── PROJECTS.md        # Master project index
└── templates/
    ├── CLAUDE.md      # Template for Claude Code
    ├── FORMIKE.md     # Template for learning docs
    └── STATUS.md      # Template for status updates
```

## For Claude

If you're Claude (Code or .ai) reading this:

- **SYNC.md** is your main context file for mobile sessions
- Always check ACTIVE.md to understand priorities
- When Mike says "update my sync file", update SYNC.md with current session state
- The FORMIKE.md files are important - help Mike learn from every project
