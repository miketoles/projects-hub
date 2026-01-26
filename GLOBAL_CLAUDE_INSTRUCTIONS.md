# Global Claude Code Instructions for Mike

> Add this to your global Claude config (~/.claude/CLAUDE.md) or include in each project's CLAUDE.md

---

## Who I'm Working With

Mike is a technically-oriented developer who uses projects as learning opportunities. He works across multiple devices:
- **Computer:** Claude Code CLI + Claude Desktop for building
- **Phone:** Claude.ai for brainstorming, planning, writing docs

## The Projects Hub System

Mike has a central **projects-hub** repo that coordinates everything:
- **Repo:** github.com/[USERNAME]/projects-hub
- **Purpose:** Unified context across all Claude instances

### Key Files in the Hub

| File | Purpose |
|------|---------|
| `SYNC.md` | Current context for mobile sessions - UPDATE THIS before Mike leaves computer |
| `ACTIVE.md` | What's actively being worked on |
| `PROJECTS.md` | Master index of all projects |

## Standard Files for Every Project

Each of Mike's projects should have:

1. **CLAUDE.md** - Context for you (Claude Code)
2. **FORMIKE.md** - Plain-language learning document (see below)
3. **STATUS.md** - Quick status snapshot
4. **design.md** - Design specifications (Mike usually creates these)

## The FORMIKE.md Requirement (Important!)

Mike wants to learn from every project. For every project, write a detailed **FORMIKE.md** file that explains the whole project in plain language.

Include:
- Technical architecture explained simply
- Codebase structure and how parts connect
- Technologies used and why we chose them
- **Bugs we hit and how we fixed them**
- Pitfalls to avoid in the future
- New technologies learned
- How good engineers think and work
- Best practices demonstrated

**Make it engaging to read** - not boring documentation. Use analogies and anecdotes. Write like you're explaining to a smart friend, not writing a textbook.

## Workflows

### When Mike Says "Update My Sync File"

1. Update `projects-hub/SYNC.md` with:
   - What we just worked on
   - Current state of the project
   - What's next
   - Any open questions or decisions
2. Commit and push to GitHub

### When Starting a Session

1. Check if there's a CLAUDE.md in the current project
2. Check STATUS.md for where things left off
3. Ask if Mike wants to continue from last session or start something new

### When Finishing a Session

1. Update STATUS.md with current state
2. Update FORMIKE.md with any new learnings
3. Offer to update the sync file if Mike is leaving the computer

### When Starting a New Project

1. Create from templates in projects-hub/templates/
2. Set up CLAUDE.md, FORMIKE.md, STATUS.md
3. Add to PROJECTS.md and ACTIVE.md in the hub

## Mike's Learning Goals

- Understanding technical architecture deeply
- Learning why decisions are made, not just what to do
- Building mental models through analogies
- Avoiding repeated mistakes by documenting pitfalls
- Thinking like a senior engineer

## Communication Style

- Explain the "why" not just the "what"
- Use analogies to make concepts stick
- Be direct and practical
- When hitting bugs, explain the debugging process
- Highlight patterns that apply across projects
