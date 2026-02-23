# Sync Up Instructions for All Agents

These instructions apply to every AI agent working on Spirit Logic projects: Claude Code, Codex, Claude Desktop, or any future agent.

---

## When Mike says "sync up"

You will perform the following steps automatically, without asking for clarification.

---

## Step 1 — Read the full file

Read the entire contents of:
```
~/dev/projects-hub/SYNC.md
```

This orients you on all active projects and all other agents' current status. Read everything before writing anything.

---

## Step 2 — Identify yourself

Determine your section tag using this format:
```
AGENT: [Your Tool Name] | PROJECT: [Project You Are Working On]
```

**Tool name examples:**
- `Claude Code`
- `Codex`
- `Claude Desktop`

**Project name:** Use the project name you have been working on in this session. If you have not worked on anything yet this session, skip Step 3 and only report what you read.

**Example tag:** `AGENT: Claude Code | PROJECT: NRT Scatterplot V2`

---

## Step 3 — Write your section

Search SYNC.md for your matching tag block:
```
<!-- AGENT: [Your Tool Name] | PROJECT: [Your Project] -->
...
<!-- /AGENT: [Your Tool Name] | PROJECT: [Your Project] -->
```

- If your block **exists**: rewrite everything between your tags. Do not touch any other agent's block.
- If your block **does not exist**: append a new block at the end of the file (before the footer links).

Your block must include:
- `*Last synced: [today's date]*`
- **Active Build** — what is currently being built, or "No active build cycle"
- **Path** — file or repo path for this project
- **Decision Queue** — open decisions that need Mike's input
- **What We Did** — bullet summary of this session's work
- **What's Next** — prioritized next actions with `← START HERE` on the first item
- **Notes** — anything important Mike should know

Also update **your row** in the `## Active Projects Quick Status` table at the top.

---

## Step 4 — Report to Mike

After reading and writing, give Mike a clean sync up summary:

1. Quote the file's `*File last updated*` date
2. Summarize all other agents' sections briefly (project, status, start-here action)
3. State your own current status and start-here action
4. Surface your decision queue items

---

## Rules

- **Never modify another agent's section.** Only rewrite between your own tags.
- **Always read before writing.** Full situational awareness before any edits.
- **If you did no work this session**, still read and report — just skip the write step.
- **One section per tool+project combination.** If you switch projects mid-session, update your section to reflect the latest project.
- **Keep entries current.** Overwrite your section fully each sync — don't append to it.

---

## File locations

```
Primary sync file:  ~/dev/projects-hub/SYNC.md
Instructions:       ~/dev/projects-hub/SYNC-INSTRUCTIONS.md
CDN (read-only):    https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md
```
