# All Projects

*Last updated: February 12, 2026*

A complete index of all Mike's projects in `~/dev/`, organized by status.

---

## Active Development

| Project | Description | Tech Stack | Status |
|---------|-------------|------------|--------|
| **NRT** | Neurorehabilitation Team Platform (TBI/ABA) | React 19, Vite 7, Express, SQLite | Core built, prototype installer working |
| **SNF** | Skilled Nursing Facility software | TBD (design phase) | Design doc + customer discovery drafted |
| **MikeText** | Multiplatform text editor (macOS + iOS/iPad) | Swift, SwiftUI | Multiplatform build complete, testing |
| **ScatterplotCreator** | Electron app for BCBAs to manage patient scatterplots | Electron 40, Node.js, HTML/CSS/JS | v1.0.3 built, pending smoke test |
| **STX Archery** | Multi-discipline archery scoring app | Expo, React Native, Skia, TypeScript | PNG renderer migration (Cycle 45), Codex building |
| **hospital-mini-apps** | PWA platform for hospital iPhone mini-apps | Next.js 16, React 19, TypeScript | In development |

---

## Games

| Game | Description | Tech | Status |
|------|-------------|------|--------|
| **Moon Rocks** | Lunar rock collection with bouncy astronaut | HTML5 Canvas, JavaScript | Playable (v21) |
| **Shipwreck Explorer** | Underwater treasure hunting | HTML5 Canvas, JavaScript | Playable MVP (v33) |
| **Bulldozer** | Satisfying digging game for toddlers | HTML5 Canvas, JavaScript | Feature complete |
| **SpaceAttack** | Space Invaders arcade shooter | HTML5 Canvas, JavaScript | Complete |
| **CatGame** | 3D stealth game (cat hunting prey) | Godot 4.x | Planning/Design |
| **Parkour Runner** | Survival parkour runner (zombie theme) | Phaser 3, Vite, TypeScript | Plan approved, Phase 1 ready |
| **TrashTruckGame** | 2D trash truck simulator | HTML5 Canvas | Planning |

---

## Planning / Design Phase

| Project | Description | Tech Stack | Notes |
|---------|-------------|------------|-------|
| **SNF** | Skilled Nursing Facility software | React SPA + Node.js (proposed) | DESIGN-DOC.md, CUSTOMER-DISCOVERY.md at `~/dev/SNF` |
| **ABA-Platform** | Role-based ABA patient data platform | Web-based (TBD) | PRD.md, DATA_MODEL.md |
| **SpiritlogicDB** | Mobile database app for non-technical users | Mobile (TBD) | Comprehensive DESIGN.md |
| **Pantry** | Photo-to-grocery-list app | Web/Mobile | PRD.md, ROADMAP.md |

---

## Learning / Experimental

| Project | Description | What I'm Learning |
|---------|-------------|-------------------|
| **AI Local** | Running LLMs locally | Local inference, privacy-focused AI |
| **Roblox** | Roblox game development | Roblox Studio, Lua scripting |
| **RBT99** | Python tools for RBT training | Django, Jupyter, Python |
| **Sandbox** | Experimental prototypes | Various (lag arbitrage, etc.) |

---

## Completed / Maintenance

| Project | Description | Status |
|---------|-------------|--------|
| **SpaceAttack** | Space Invaders arcade shooter | Complete |
| **polymarket-arb-bot** | Polymarket arbitrage trading bot | Running on Railway |
| **Spiritlogic Shared UI** | JUCE UI theme module | Active (reusable) |
| **UI Schemas** | Color/theme gallery | Reference |

---

## Paused / On Hold

| Project | Description | Why Paused |
|---------|-------------|------------|
| **Quiz App** | Kahoot-like training app for RBTs | Waiting for NRT work |
| **AbletonPlugins** | JUCE audio plugins (Arp, Distortion) | Waiting on JUCE learning |
| **ABA Tracker** | Web app for ABA patient tracking | Superseded by NRT |
| **LuckySnap** | Photo-based app | Low priority |
| **Scatterplot Printer** | Earlier scatterplot tool | Superseded by ScatterplotCreator |

---

## Reference / Meta

| Project | Description |
|---------|-------------|
| **meta** | Project index and local paths |
| **Protocols** | ABA protocol templates (Word docs) |
| **projects-hub** | This repo - central command |
| **spiritlogic** | Main brand/landing site (spiritlogic.dev) — updated for Apple Developer enrollment |
| **agent-workflow** | HANDOFF_TEMPLATE.md for dual-agent (Claude+Codex) workflow |

---

## By Technology

**Swift/SwiftUI:** MikeText
**JavaScript/TypeScript:** 3dArchery, Quiz App, hospital-mini-apps, Moon Rocks, Shipwreck Explorer, Bulldozer, SpaceAttack, TrashTruckGame, Parkour Runner
**React/Vite:** NRT Core, SNF (proposed)
**Electron:** ScatterplotCreator
**Python:** polymarket-arb-bot, RBT99
**C++/JUCE:** AbletonPlugins, Spiritlogic Shared UI
**Godot:** CatGame
**HTML5/Canvas:** Moon Rocks, Shipwreck Explorer, Bulldozer, SpaceAttack, TrashTruckGame, UI Schemas

---

## Project Locations

All projects live in `~/dev/`:
- Games in `~/dev/game-ideas/` (Moon Rocks) or `~/dev/` (others)
- 15+ are git repos
- Design docs exist for 20+ projects

---

## Quick Start Commands

```bash
# NRT Core (development)
cd ~/dev/NRT/core/frontend && npm run dev   # Frontend at localhost:5175
cd ~/dev/NRT/core/backend && npm run dev    # Backend at localhost:3003

# NRT Core (build prototype)
cd ~/dev/NRT && ./scripts/build-prototype.sh  # Creates prototypes/nrt-core-prototype.zip

# MikeText
open ~/dev/MikeText/MikeText/MikeText.xcodeproj

# Games
cd ~/dev/game-ideas/moon-rocks && python3 -m http.server 8080
cd ~/dev/ShipwreckExplorer && python3 -m http.server 8081
cd ~/dev/bulldozer\ app && python3 -m http.server 8082

# ScatterplotCreator
cd ~/dev/ScatterplotCreator && npm start
```
