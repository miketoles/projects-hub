# Sync File for Claude

*Last synced: Feb 18, 2026 by Claude Code*

---

## Current Focus

**Project:** STX Archery (3dArchery)
**Path:** `~/dev/3dArchery`
**Branch:** main
**Run:** `cd ~/dev/3dArchery && npx expo run:ios --device`

## What We Did This Session

- Fixed BugCatcher 🐛 button position (moved to upper-right, uses `useSafeAreaInsets`)
- Fixed NSCameraUsageDescription crash via `expo prebuild` (app.json infoPlist + native rebuild)
- Created `scripts/get-bugreport.sh` + added `bug-reports/` to .gitignore
- Confirmed iOS 26 simulator has broken text input — not a code bug, device testing needed
- USB-C cable ordered (Anker), arrives tomorrow — will install on iPhone 16 Pro Max
- Planned crosshair reticle for zoom mode (saved as future feature, not built)
- Researched + documented 5 expansion packs: NA Extended, African Safari, European Hunt, Dinosaur, Fantasy
- Created `docs/STX-Expansion-Pack-Roadmap.md` with full animal lists + batch ChatGPT prompts
- Updated `docs/STX-Animal-Art-Generation-Playbook.md` (17 animals complete, added fantasy/dino notes)
- Designed + documented What's New modal feature (`docs/STX-WhatsNew-Feature-Design.md`)

## What's Next

- [ ] USB-C cable arrives → `npx expo run:ios --device` ← START HERE
- [ ] Test camera, text input, GPS, BugCatcher frame capture on real device
- [ ] Review first real-device bug reports
- [ ] Build What's New modal (pre-v1.1, feature doc ready)
- [ ] Build NA Extended pack (art gen + data entry, ~3–4 hrs)

## Open Questions

- Discord server: set one up before v1.1 so What's New CTA has a real URL
- Free tier limit confirmed at 7 sessions

## Notes for Mobile Session

- **Device setup:** plug iPhone, run `npx expo run:ios --device`, trust Mac on iPhone, trust dev cert in Settings → VPN & Device Management
- Expansion packs all documented — no decisions needed yet, just art generation when ready
- What's New modal is designed and ready for Codex — impl before v1.1 ship

## From Mobile Session

*(empty — paste mobile notes here)*

## Active Projects Quick Status

| Project | Status | Next Action |
|---------|--------|-------------|
| STX Archery | 🟡 v1.0 nearly done | Real device testing (cable arrives tomorrow) |
| NRT Core | 🟡 Prototype built | Send to Ari for testing |
| ScatterplotCreator | 🟡 v1.0.3 built | Windows smoke test → L: drive |
| SNF | 🔵 Design doc ready | Schedule customer call |
| MikeText | 🟡 Multiplatform built | Runtime test on iPhone sim |

---

*Fetch (cache-busting): https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fetch (fallback): https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
