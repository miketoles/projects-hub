# Sync File for Claude

*Last synced: January 27, 2026 by Claude Code*

Hey Claude! Mike stepped away from the CR project. Here's everything you need to know:

---

## Current Project: CR (Scatterplot Data Platform)

**Path:** `~/dev/CR`
**GitHub:** https://github.com/miketoles/CR
**Run it:** `cd ~/dev/CR && npm run dev` → http://localhost:3000
**Demo logins:** admin@example.com / admin123, bcba@example.com / bcba123

### What Is This?

A behavior data tracking platform for BCBAs and RBTs at Mike's hospital. Staff use paper scatterplots to track patient behaviors in 15-minute intervals throughout the day (96 intervals total). This app replaces the tedious manual data entry into CentralReach.

### What's Built (Phase 1 Complete)

**Tech Stack:**
- Next.js 16 + React 19 + TypeScript
- Tailwind CSS for styling
- Prisma ORM with SQLite (dev) / PostgreSQL (production)
- NextAuth.js for authentication

**Features Working:**
- User authentication (login/logout)
- Client management (add/edit clients)
- Behavior management (add behaviors per client with colors)
- ScatterplotGrid component - the core data entry UI:
  - 96 intervals (15-min each, 7 AM to 7 AM)
  - Click to toggle behavior occurred (shaded cell)
  - Click+drag to fill ranges
  - Check column for marking entire rows observed/skipped
  - Live totals (observed count, IND count, ERR count)
  - Keyboard shortcuts: I (ind), E (err), S (skip), C (clear)
- REST API for all CRUD operations
- Session save/load to database

**Database Schema:**
```
User → Sessions
Client → Behaviors → Intervals
       → Sessions → Intervals
```

**Key Files:**
- `components/ScatterplotGrid.tsx` - The 96-interval grid
- `app/entry/page.tsx` - Data entry page
- `lib/auth.ts` - NextAuth config
- `prisma/schema.prisma` - Database schema

---

## IMPORTANT: Future Auth Change

Mike wants **NO manual login**. Users are already logged into hospital computers - the app should auto-authenticate from Windows/network credentials.

**Approach:** NextAuth + LDAP/Active Directory integration
**When:** Phase 4 (deployment)
**Don't implement yet** - wait for hospital IT coordination

---

## What's Next

### Phase 2: Offline-First Sync
- IndexedDB storage (idb library already installed)
- Save to IndexedDB first, sync to server in background
- Queue failed requests, retry on reconnect
- Sync status indicator in UI
- Service worker for full offline support

### Phase 3: Reports & Export
- Report builder UI (select client, date range, behaviors)
- Trend charts with Recharts (already installed)
- Heat map (when behaviors occur by time of day)
- Excel export with embedded charts (ExcelJS installed)

### Phase 4: Deployment + Auth
- Switch to Windows/AD authentication
- Docker container for hospital server
- PostgreSQL for production
- Hospital IT coordination

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    Scatterplot Platform                      │
│                   (Next.js Web App)                          │
├─────────────────────────────────────────────────────────────┤
│   Quick Entry UI  │   Reports Builder  │   Client Admin     │
├─────────────────────────────────────────────────────────────┤
│              Offline-First Data Layer                        │
│         (IndexedDB + Background Sync) [Phase 2]              │
└──────────────────────────┬───────────────────────────────────┘
                           │ REST API
              ┌────────────▼────────────┐
              │   Hospital VPN Server   │
              │   PostgreSQL + Next.js  │
              └─────────────────────────┘
```

---

## Other Active Projects

| Project | Status | Next Action |
|---------|--------|-------------|
| **CR** | Phase 1 Complete | Phase 2: Offline sync |
| ScatterplotCreator | In stakeholder review | Address feedback |
| 3dArchery | Expanding to v2 | Add Indoor scoring |
| hospital-mini-apps | In development | Continue building |
| polymarket-arb-bot | Running on Railway | Monitor |

---

*Mobile Claude: This is the primary handoff file. All context is here.*
