# Sync File for Claude

*Last synced: January 27, 2026 by Claude Code*

Hey Claude! Mike stepped away from the CR project. Here's where things stand:

---

## What I Was Just Working On

**Project:** CR (Scatterplot Data Platform)
**Path:** `~/dev/CR`

**Completed in this session:**
- Built complete Phase 1 of the Scatterplot Data Platform
- Next.js 16 app with TypeScript, Tailwind, Prisma
- User authentication (NextAuth with credentials)
- Client/behavior management pages
- ScatterplotGrid component (96 intervals, click+drag)
- REST API for all CRUD operations
- SQLite database with seed data

**The app is runnable:** `cd ~/dev/CR && npm run dev`

**Demo accounts:**
- admin@example.com / admin123
- bcba@example.com / bcba123

---

## IMPORTANT: Future Auth Change

Mike wants to change authentication to use **network/Windows credentials**:
- Users are already logged into hospital computers
- App should auto-authenticate from system credentials
- No separate login step - seamless experience
- Look into: NextAuth + LDAP/Active Directory integration

**Don't change this now** - just note for Phase 2+

---

## What's Next for CR

### Phase 2: Offline-First Sync
- IndexedDB storage layer for offline data entry
- Background sync to hospital database
- Sync status indicator
- Service worker

### Phase 3: Reports & Export
- Trend charts with Recharts
- Heat map visualization
- Excel export with ExcelJS

### Phase 4: Deployment
- Docker container for hospital server
- PostgreSQL for production
- Coordinate with hospital IT

---

## Quick Status: Active Projects

| Project | Status | Next Action |
|---------|--------|-------------|
| **CR** | Phase 1 Complete | Phase 2: Offline sync |
| ScatterplotCreator | In stakeholder review | Address feedback |
| 3dArchery | Expanding to v2 | Add Indoor scoring modes |
| hospital-mini-apps | In development | Continue building |
| polymarket-arb-bot | Running | Monitor |

---

## Project Files to Check

When resuming CR:
1. `~/dev/CR/STATUS.md` - Full project status
2. `~/dev/CR/docs/design-plan.md` - Original design doc (if exists)
3. `~/dev/CR/mockup/quick-entry.html` - Original prototype reference

---

## Quick Links

- **Projects Hub:** ~/dev/projects-hub
- **Active Projects:** [ACTIVE.md](./ACTIVE.md)
- **All Projects:** [PROJECTS.md](./PROJECTS.md)

---

*To update this file: Ask Claude Code to "update my sync file" before leaving your computer.*
