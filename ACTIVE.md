# Active Projects

*Last updated: February 14, 2026*

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
- **Status:** B11 complete (button-based precision shot placement). 45 suites / 279 tests. 11 builds done (B1-B11). Sim-tested: "feels much better." DUNS pending.
- **Next step:** More sim-testing → weather warning color fix → DUNS → TestFlight → App Store submission

**Stack:** Expo (React Native), TypeScript, @shopify/react-native-skia, react-native-gesture-handler, expo-sqlite, react-native-purchases (RevenueCat)
**Architecture:** Three-agent workflow (CC=planner/reviewer, Codex=builder) via HANDOFF.md
**Landing page:** https://stx-archery.com (Netlify) + spiritlogic.dev updated

### 7. hospital-mini-apps
- **Path:** `~/dev/hospital-mini-apps`
- **Status:** In development
- **Next step:** Continue building mini-app platform

---

## This Week's Goals

- [ ] STX Archery: More sim-testing of B11 precision modes ← TOP PRIORITY
- [ ] STX Archery: Weather warning color fix (red → green)
- [ ] DUNS → Apple Developer enrollment → TestFlight
- [ ] STX Archery: Address remaining deferred UX items
- [ ] Send NRT prototype zip to Ari for extended testing
- [ ] SNF: Schedule customer call, review discovery template

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
| STX Archery B11 sim-tested | Feb 14, 2026 | Button-based precision shot placement (Zoom/Edit modes), KISS approach, 45 suites / 279 tests |
| STX Archery B5-B10 | Feb 13-14, 2026 | Craft polish, feedback intensity, session resume, precision gestures (rebuilt as B11) |
| STX Archery B4 approved | Feb 12, 2026 | UX audit fixes: navigation safety, confirmation dialogs, save feedback, tab refresh, dedup |
| STX Archery B3 merged | Feb 12, 2026 | Animal names in summary/export, target navigation, export message fix |
| STX Archery B2 merged | Feb 12, 2026 | Animal Selector + Course Templates: 51 cycles, 37 suites / 223 tests |
| STX Archery PNG spec review | Feb 12, 2026 | Architecture review of PNG-RENDERER-SPEC, 5 patches applied, v1.1 FINAL |
| STX Archery feature-complete | Feb 11, 2026 | 44 cycles, 22 engines, 171 tests, landing page + animal art deployed |
| spiritlogic.dev update | Feb 11, 2026 | Real company landing page for Apple Developer enrollment |
| STX Archery Phase A | Feb 11, 2026 | Steps 1-7 complete, 18 cycles, 72 tests, device verified |
| NRT Core prototype installer | Feb 8, 2026 | 5 cycles, fully working on Windows, lessons captured |
| SNF design documents | Feb 8, 2026 | DESIGN-DOC.md + CUSTOMER-DISCOVERY.md |
| MikeText multiplatform build | Feb 7, 2026 | 4 phases complete (macOS + iOS/iPad), pending runtime test |
| ScatterplotCreator v1.0.3 | Feb 7, 2026 | 60-finding security remediation, 8 phases, installer + portable ZIP |
| MikeText Mac Local | Jan 29, 2026 | Full-featured, ready for daily use |
| NRT Design Doc v2.2 | Jan 29, 2026 | 3,345 lines, comprehensive spec |
