# Sync File for Claude

*Last synced: January 29, 2026 by Claude Code*

---

## Current Focus

**Project:** MikeText
**Path:** `~/dev/MikeText`
**Run:** Open `~/dev/MikeText/MikeText/MikeText.xcodeproj` in Xcode, Cmd+R

---

## What We Did This Session

### MikeText - Text Editor for Mac (Complete)

Built a full-featured, minimal text editor with these features:

**Core Features:**
- Basic text editing with monospace font
- Open/Save/Create documents
- Tabbed interface (multiple documents in tabs)
- Opens with new document (no file dialog on launch)

**Visual Options:**
- Color modes: Dark (black/white), Light (white/black), Console (grey/neon green)
- Font picker: Courier New, Menlo, Monaco, SF Mono, Andale Mono, Consolas
- Font size controls (Cmd+/-, Cmd+0 reset)
- Line numbers toggle (Cmd+Shift+L)
- Word wrap toggle (Cmd+Shift+W)
- Syntax highlighting for 12+ languages (Cmd+Shift+H)
- Show invisibles: Space (·), Tab (→), LF (↵), CR (←) - Cmd+Shift+I

**Other:**
- Status bar with full file path, file type, line/char count
- Open Recent persists across sessions
- Session restore (reopens last open documents)
- No auto-substitutions (no smart quotes, dashes, or double-space-to-period)
- All settings persist via UserDefaults

**Installed:** Exported to Applications folder, pinned to Dock

**Known Issue:** Window size/position persistence works on app launch, but opening a new document mid-session reverts to original launch size. Documented for future fix.

### Also This Session

- Added preferred "Lean Open-Source" tech stack to main CLAUDE.md
- Updated MikeText DESIGN.md and STATUS.md with all features

---

## Current State

**MikeText is ready for daily use.**

Key files:
- `~/dev/MikeText/MikeText/MikeText/` - Xcode project source
- `~/dev/MikeText/SourceFiles/` - Backup copies
- `~/dev/MikeText/DESIGN.md` - Design document
- `~/dev/MikeText/STATUS.md` - Current status

---

## Preferred Tech Stack (Added to CLAUDE.md)

For new web apps:
- **Frontend:** React 18, Vite, TypeScript, Tailwind CSS
- **Backend:** Node.js, Express, better-sqlite3
- **Database:** SQLite (single file, portable)
- **Auth:** Dev user picker / Prod header-based (IIS/nginx)
- **Exports:** Recharts, ExcelJS, jsPDF, pptxgenjs

All MIT/Apache/Public Domain licensed, no corporate lock-in, no subscriptions.

---

## Notes for Next Session

- MikeText window frame issue to fix later (documented in STATUS.md)
- NRT Scatterplot Data Entry ready to build with lean stack
- Shipwreck Explorer game plan exists at `~/.claude/plans/ticklish-wobbling-volcano.md`

---

## From Mobile Session

*(empty - paste mobile notes here)*

---

*For all projects: see ACTIVE.md*
