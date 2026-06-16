# HWPC QBOL Migration Notes

**Operational detail lives at:** [https://hwpc.2cld.net/](https://hwpc.2cld.net/)

## Project: qb_migration
**Location:** Account/_tools/qb_migration
**Repo:** [ns-account gitea](https://gitea.cat9.me/nsadmin/ns-account)
**Status:** ✅ Migration complete - paycheck issued 2026-03-31

### Key Milestones
 - 2026-03-14: route-ticket-printing spawned from qb_migration testing
 - 2026-03-21: Production customer/route import working, full month auto-scheduled
 - 2026-03-22: QB2024→QBOL migration started (Mar 22 backup)
 - 2026-03-27: Final QBOL migration failed (8hr import timeout)
 - 2026-03-28: QB2020 up + customers imported as alternative path
 - 2026-03-31: HWPC migration to QBOL complete - paycheck issued

## Project: route-ticket-printing
**Status:** ✅ Complete (EPIC closed 2026-05-06)

### Goal
Prepare and manage the HWPC field service team's route tickets outside of QBOL.

### Outcome
Mark running Route Print independently. All old-system payments recorded in QBOL.

### Links
 - [hwpc.2cld.net QBOL section](https://hwpc.2cld.net/) - print ticket procedures, tax reports, ToDo
 - [ns-account gitea](https://gitea.cat9.me/nsadmin/ns-account) - dev repo

---
*Migrated from [2cld/wip](https://github.com/2cld/wip) wip-detail/ on 2026-06-16. Historical reference for HWPC public support docs.*
