# Active Projects

*Last updated: January 30, 2026*

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

### 2. MikeText - Mac Local Edition
- **Path:** `~/dev/MikeText`
- **Status:** Complete and ready for daily use
- **Tech:** Swift/SwiftUI, macOS 14+

**What it is:** A clean, minimal text editor that shows files as-is. No proprietary formats, no smart quotes, no surprises.

**Features:**
- Syntax highlighting for 12+ languages
- 6 monospace fonts, font size controls
- Dark/Light/Console color modes
- Show invisibles (spaces, tabs, line endings)
- Line numbers, word wrap toggles
- Tabbed interface, session restore
- Open Recent, all settings persist

**Known issue:** Window size/position can reset when opening new docs mid-session.

### 3. ScatterplotCreator
- **Path:** `~/dev/ScatterplotCreator`
- **GitHub:** https://github.com/miketoles/Scatterplot
- **Status:** In stakeholder review
- **Next step:** Continue gathering feedback, address any issues

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

- [ ] NRT Phase 0: Project setup with lean stack
- [ ] Port ScatterplotGrid preserving paint-it-in behavior
- [ ] Present ScatterplotCreator to stakeholders
- [ ] Fix Moon Rocks mobile scaling issues
- [ ] Add Indoor scoring to 3dArchery

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
| MikeText Mac Local | Jan 29, 2026 | Full-featured, ready for daily use |
| NRT Design Doc v2.2 | Jan 29, 2026 | 3,345 lines, comprehensive spec |
| Shipwreck Explorer animations | Jan 28, 2026 | 2.5D diver with smooth flip transitions |
| Moon Rocks v21 | Jan 28, 2026 | Footprints, aliens, oxygen warning |
| ScatterplotCreator v1 | Jan 2026 | All 6 UI changes done |
