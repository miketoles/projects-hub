# Active Projects

*Last updated: February 11, 2026*

What I'm actively working on right now.

---

## Currently Building

### 1. NRT (Neurorehabilitation Team Platform) - HIGH PRIORITY
- **Path:** `~/dev/NRT`
- **GitHub:** https://github.com/miketoles/NRT
- **Status:** Core app built (React 19 + Vite + Express + SQLite). Prototype installer working.
- **Next step:** Send prototype zip to Ari for extended testing

**Vision:** Bespoke ABA platform for Craig Hospital's TBI patients. Complete CentralReach replacement.

**Stack:**
- Frontend: React 19 + Vite 7 + TypeScript 5.9
- Backend: Node.js + Express + better-sqlite3
- Auth: Dev mode user picker, prod reads X-Remote-User header
- Prototype: Caddy reverse proxy, bundled Node.js, one-click `start.bat`

**Prototype:** `./scripts/build-prototype.sh` builds a 61MB zip. Tester unzips → clicks `start.bat` → done. All features working (patients, doctors/BCBAs, CHSA assessments, scatterplot data entry, admin settings).

**Architecture:** Dual-agent workflow (Claude=planner/reviewer, Codex=builder) via HANDOFF.md.

### 2. SNF (Skilled Nursing Facility Software) - NEW
- **Path:** `~/dev/SNF`
- **Status:** Design doc and customer discovery template drafted
- **Next step:** Schedule customer call, review CUSTOMER-DISCOVERY.md

**What it is:** A SNF has contacted Mike about building software. Design doc covers market landscape, product vision, feature tiers, technical architecture, HIPAA compliance, and business model. Survey readiness identified as strongest market gap opportunity.

**Key files:**
- `~/dev/SNF/DESIGN-DOC.md` — full business + product design
- `~/dev/SNF/CUSTOMER-DISCOVERY.md` — structured questions for the call

### 3. MikeText - Multiplatform Text Editor
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
**iOS-specific:** Settings sheet (gear button), compact iPhone status bar, iPad keyboard shortcuts

**Architecture:** Dual-agent workflow (Claude=planner/reviewer, Codex=builder) via HANDOFF.md. 4 phases completed. iCloud Drive sync testing deferred (Phase 3).

**Next:** Runtime test Phase 4 on iPhone simulator, then commit.

### 4. ScatterplotCreator
- **Path:** `~/dev/ScatterplotCreator`
- **GitHub:** https://github.com/miketoles/Scatterplot
- **Status:** v1.0.3 built (60-finding security remediation complete, 28 unit tests, 0 npm vulns)
- **Next step:** Windows smoke test, then deploy to hospital L: drive

### 5. Games (Active Development)
| Game | Path | Status | Port |
|------|------|--------|------|
| **Moon Rocks** | `~/dev/game-ideas/moon-rocks` | Playable (v21), mobile scaling issues | 8080 |
| **Shipwreck Explorer** | `~/dev/ShipwreckExplorer` | Playable MVP (v33) | 8081 |
| **Bulldozer** | `~/dev/bulldozer app` | Feature complete, grandson's favorite | 8082 |

### 6. STX Archery (3dArchery)
- **Path:** `~/dev/3dArchery`
- **GitHub:** https://github.com/miketoles/3darchery
- **Status:** Phase A complete (Steps 1-7). App runs on iOS simulator. 72 tests, 96 files committed.
- **Next step:** Review Codex's Step 8 (ASA engine + ring renderer), then Steps 9-10

**Stack:** Expo (React Native), TypeScript, @shopify/react-native-skia, react-native-gesture-handler, expo-sqlite
**Architecture:** Three-agent workflow (CC=planner/reviewer, Codex=builder, CD=strategic reviewer) via HANDOFF.md

### 7. hospital-mini-apps
- **Path:** `~/dev/hospital-mini-apps`
- **Status:** In development
- **Next step:** Continue building mini-app platform

---

## This Week's Goals

- [ ] STX Archery: Review Codex's Step 8 build (ASA engine + ring renderer) ← TOP PRIORITY
- [ ] Send NRT prototype zip to Ari for extended testing
- [ ] SNF: Schedule customer call, review discovery template
- [ ] MikeText: Runtime test Phase 4 on iPhone simulator, commit
- [ ] ScatterplotCreator: Windows smoke test v1.0.3, deploy

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
| STX Archery Phase A | Feb 11, 2026 | Steps 1-7 complete, 18 cycles, 72 tests, device verified |
| NRT Core prototype installer | Feb 8, 2026 | 5 cycles, fully working on Windows, lessons captured |
| SNF design documents | Feb 8, 2026 | DESIGN-DOC.md + CUSTOMER-DISCOVERY.md |
| MikeText multiplatform build | Feb 7, 2026 | 4 phases complete (macOS + iOS/iPad), pending runtime test |
| ScatterplotCreator v1.0.3 | Feb 7, 2026 | 60-finding security remediation, 8 phases, installer + portable ZIP |
| MikeText Mac Local | Jan 29, 2026 | Full-featured, ready for daily use |
| NRT Design Doc v2.2 | Jan 29, 2026 | 3,345 lines, comprehensive spec |
