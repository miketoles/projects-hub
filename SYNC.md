# Spirit Logic — Multi-Agent Sync File

*Last synced: 2026-03-04 by Claude Code (STX Archery iOS submitted — Waiting for Review)*

> **For agents:** See `SYNC-INSTRUCTIONS.md` in this repo for sync up protocol.

---

## Active Projects Quick Status

| Project | Status | Next Action | Last Agent |
|---------|--------|-------------|------------|
| STX Archery | ✅ iOS submitted — Waiting for Review | Android: RC key + rebuild + Play Console | Claude Code |
| OneDoc | 🟢 M10.1 UX polish live; DOCX+Excel printing stable | Install EXE on work laptop | Codex |
| ScatterplotCreator | 🟢 v1.0.10 — archive + BUG-008 fix | Await committee v2 approval | Claude Code |
| NRT | 🟡 RBT Session spec v0.3 ready | RBT impl planning | Claude Code |

---

<!-- AGENT: Claude Code | PROJECT: STX Archery -->
## Claude Code — STX Archery
*Last synced: 2026-03-04*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/3dArchery`
**Run:** `npx expo run:ios`

<!-- DECISION_QUEUE_START -->
(none)
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Framed 5 iPhone + 5 iPad App Store screenshots using Python/Pillow script (no Figma)
- Filled all ASC metadata: description, subtitle, keywords, promotional text, URLs, copyright
- Completed App Privacy (Precise Location + Purchase History), age rating (4+), category, pricing
- Fixed all "Unable to Add for Review" blockers; attached IAP and build
- **Submitted STX Archery iOS 1.0 to App Store — Waiting for Review (10:24 PM)**

**What's Next:**
- [ ] Await Apple review (1-3 business days) ← WAITING
- [ ] Android: create Premium Lifetime product in Google Play Console
- [ ] Android: add RC Android app, store `EXPO_PUBLIC_REVENUECAT_ANDROID_API_KEY` as EAS secret
- [ ] Android: rebuild .aab with RC key → manual first upload to Play Console
- [ ] Post-launch: UX-DELETE-01 (arrow deletion discoverability — v1.1)

**Notes:**
- NEXT-APP-PLAYBOOK.md fully updated with all submission lessons (screenshots, IAP, ASC forms, iPad)
- SUBMISSION-NOTES.md updated with submission confirmation + Android checklist
- Submission ID: fa548694-7165-4a25-ad64-7af5ae30dd63
<!-- /AGENT: Claude Code | PROJECT: STX Archery -->

---

<!-- AGENT: Claude Code | PROJECT: OneDoc -->
## Claude Code — OneDoc
*Last synced: 2026-03-02*

<!-- ACTIVE_BUILD_START -->
**Project:** OneDoc Print Manager | **Cycle:** M5 | **Status:** feature-complete ✅
**Next agent:** mike
**Building:** Windows integration testing — install EXE, verify UI loads
**Gates:** 8 suites / 37 tests, tsc clean, installer built (84MB NSIS)
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/OneDoc`
**Run:** `npm run dev`

<!-- DECISION_QUEUE_START -->
- Install `dist-installer/OneDoc Print Manager Setup 0.1.0.exe` on work laptop and confirm UI loads
- If it works: v1 is done, ready for real-world testing with Word + network drive
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Install new EXE on work laptop ← START HERE
- [ ] Verify UI renders (full dark UI, no blank screen)
- [ ] Test with real Word + L-drive if UI works
<!-- /AGENT: Claude Code | PROJECT: OneDoc -->

---

<!-- AGENT: Claude Code | PROJECT: ScatterplotCreator -->
## Claude Code — ScatterplotCreator
*Last synced: 2026-03-02*

<!-- ACTIVE_BUILD_START -->
No active build cycle.
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/ScatterplotCreator`
**Run:** `npm start`

<!-- DECISION_QUEUE_START -->
- Committee approval needed to flip v2 as default (1-line change in main.js)
<!-- DECISION_QUEUE_END -->

**What's Next:**
- [ ] Mike testing v1.0.10 in active use ← IN PROGRESS
- [ ] Await committee v2 approval ← BLOCKED
- [ ] Flip default to v2 when approved (1-line change in main.js)
<!-- /AGENT: Claude Code | PROJECT: ScatterplotCreator -->

---

<!-- AGENT: Codex | PROJECT: OneDoc -->
## Codex — OneDoc
*Last synced: 2026-03-03*

<!-- ACTIVE_BUILD_START -->
**Project:** OneDoc Print Manager | **Cycle:** M10.1 | **Status:** shipping-ready ✅
**Next agent:** mike
**Building:** No active build cycle
**Gates:** 11 suites / 58 tests; typecheck, lint, build all clean; NSIS installer built
<!-- ACTIVE_BUILD_END -->

**Path:** `~/dev/OneDoc`
**Run:** `npm run dev`

<!-- DECISION_QUEUE_START -->
- Decide whether to patch the done-state double-checkmark now or batch with next UI polish cycle
<!-- DECISION_QUEUE_END -->

**What We Did This Session:**
- Implemented M10.1 UX polish: printer preference persistence, status timestamp summary
- Built and verified latest installer: `dist-installer/OneDoc Print Manager Setup 0.1.0.exe`
- SHA-256: `eaf5ea7be1cb116019eec43c4e6fecb33f5bda4e309127d67141337badab2dab`

**What's Next:**
- [ ] Install latest EXE on work laptop and smoke-test ← START HERE
- [ ] Fix done-state button duplicate checkmark and rebuild installer
- [ ] Begin M8 planning for additional formats (pdf, image, text)
<!-- /AGENT: Codex | PROJECT: OneDoc -->

---

*Primary: https://cdn.jsdelivr.net/gh/miketoles/projects-hub@main/SYNC.md*
*Fallback: https://raw.githubusercontent.com/miketoles/projects-hub/main/SYNC.md*
