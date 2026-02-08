# Active Projects

*Last updated: February 7, 2026*

What I'm actively working on right now.

---

## Currently Building

### 1. NRT (Neurorehabilitation Team Platform) - HIGH PRIORITY
- **Path:** `~/dev/NRT`
- **GitHub:** https://github.com/miketoles/NRT
- **Status:** Design complete (v2.2), ready to rebuild with lean stack
- **Next step:** Phase 0 - Create new project structure with Vite + Express + better-sqlite3
- **Design Doc:** `~/dev/NRT/docs/NRT Scatterplot System Design.md` (3,345 lines)

**Vision:** Bespoke ABA platform for Craig Hospital's TBI patients. Complete CentralReach replacement.

**Key Decision (Jan 30):** Rebuilding from scratch with lean open-source stack instead of continuing with Next.js/Prisma. The paint-it-in interface from `mockup/quick-entry.html` will be preserved exactly.

**New Stack:**
- Frontend: React 18 + Vite + TypeScript + Tailwind CSS
- Backend: Node.js + Express + better-sqlite3
- Auth: No login - dev mode user picker, prod reads X-Remote-User header
- Database: SQLite (SQLCipher for encryption later)

### 2. MikeText - Multiplatform Text Editor
- **Path:** `~/dev/MikeText`
- **Status:** Multiplatform build complete (macOS + iPhone + iPad), pending runtime testing
- **Tech:** Swift/SwiftUI, macOS 26.1 / iOS 26.1

**What it is:** A clean, minimal text editor that shows files as-is. No proprietary formats, no smart quotes, no surprises. Now runs on macOS, iPhone, and iPad.

**Features (all platforms):**
- Syntax highlighting for 12+ languages
- 6 monospace fonts, font size controls
- Dark/Light/Console color modes
- Line numbers, word wrap, show invisibles toggles

**macOS-specific:** Tabbed interface, session restore, Open Recent, invisibles layout manager
**iOS-specific:** Settings sheet (gear button), compact iPhone status bar, iPad keyboard shortcuts (Cmd+Shift+L/W/H/I, Cmd+Plus/Minus/0)

**Architecture:** Dual-agent workflow (Claude=planner/reviewer, Codex=builder) via HANDOFF.md. 4 phases completed (platform abstraction, iOS plain text, iOS highlighting, iOS polish). iCloud Drive sync testing deferred (Phase 3).

**Next:** Runtime test Phase 4 on iPhone simulator, then commit.

### 3. ScatterplotCreator
- **Path:** `~/dev/ScatterplotCreator`
- **GitHub:** https://github.com/miketoles/Scatterplot
- **Status:** v1.0.3 built (60-finding security remediation complete, 28 unit tests, 0 npm vulns)
- **Next step:** Windows smoke test, then deploy to hospital L: drive

### 4. Games (Active Development)
| Game | Path | Status | Port |
|------|------|--------|------|
| **Moon Rocks** | `~/dev/game-ideas/moon-rocks` | Playable (v21), mobile scaling issues | 8080 |
| **Shipwreck Explorer** | `~/dev/ShipwreckExplorer` | Playable MVP (v33) | 8081 |
| **Bulldozer** | `~/dev/bulldozer app` | Feature complete, grandson's favorite | 8082 |

### 5. 3dArchery
- **Path:** `~/dev/3dArchery`
- **Status:** Expanding to v2 (multi-discipline)
- **Next step:** Implement Indoor scoring (NFAA 300, Vegas)

### 6. hospital-mini-apps
- **Path:** `~/dev/hospital-mini-apps`
- **Status:** In development
- **Next step:** Continue building mini-app platform

---

## This Week's Goals

- [ ] MikeText: Runtime test Phase 4 on iPhone simulator, commit
- [ ] ScatterplotCreator: Windows smoke test v1.0.3, deploy
- [ ] Parkour Runner: Phase 1 scaffolding (Phaser 3 + Vite + TypeScript)
- [ ] NRT: Continue collecting triage feedback from IT meeting

---

## Parked (Will Resume Soon)

| Project | Why Parked | Resume When |
|---------|------------|-------------|
| Quiz App | Other priorities | After NRT Phase 1 |
| AbletonPlugins | Waiting on JUCE learning | Free weekend |
| polymarket-arb-bot | Running on Railway | Monitor only |

---

## Recently Completed

| Project | Completed | Notes |
|---------|-----------|-------|
| MikeText multiplatform build | Feb 7, 2026 | 4 phases complete (macOS + iOS/iPad), pending runtime test |
| ScatterplotCreator v1.0.3 | Feb 7, 2026 | 60-finding security remediation, 8 phases, installer + portable ZIP |
| MikeText Mac Local | Jan 29, 2026 | Full-featured, ready for daily use |
| NRT Design Doc v2.2 | Jan 29, 2026 | 3,345 lines, comprehensive spec |
| ScatterplotCreator v1 | Jan 2026 | All 6 UI changes done |
