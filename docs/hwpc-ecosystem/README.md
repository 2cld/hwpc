[edit](https://github.com/2cld/hwpc/edit/master/docs/hwpc-ecosystem/README.md)

# HWPC Ecosystem Map

> A map of all repos, sites, machines, and services related to HWPC. Use this to orient yourself or point collaborators to the right resource.

## 2cld.net Sites

| Site | Purpose | Repo | Access | HWPC Relationship |
|------|---------|------|--------|-------------------|
| [hwpc.2cld.net](https://hwpc.2cld.net/) | HWPC dev coordination | [2cld/hwpc](https://github.com/2cld/hwpc) | Public | This site — source of truth for HWPC |
| [wip.2cld.net](https://wip.2cld.net/) | 2cld work-in-progress dashboard | [2cld/wip](https://github.com/2cld/wip) | Public | Tracks HWPC epics — should link here, not duplicate |
| [2cld.net](https://2cld.net/) | Parent org site | 2cld org | Public | Parent |

> Pattern: wip.2cld.net is the daily dashboard across all projects. HWPC-specific info lives here at hwpc.2cld.net. Wip should link to hwpc, not duplicate content.

## HWPC Public Sites

| Site | Purpose | Repo |
|------|---------|------|
| [hawkeyewestpestcontrol.com](https://www.hawkeyewestpestcontrol.com/) | Main business site (Wix) | [christrees/hawkeyewestpestcontrol.com](https://github.com/christrees/hawkeyewestpestcontrol.com) |
| [hwpest.com](https://hwpest.com/) | Alternate domain | [christrees/hwpest.com](https://github.com/christrees/hwpest.com) |
| [hwpc.net](https://hwpc.net/) | Alternate domain | [christrees/hwpc.net](https://github.com/christrees/hwpc.net) |

## Application Repos (GitHub — grasshorse org)

| Repo | Purpose | Access |
|------|---------|--------|
| [grasshorse/hwpc-gs](https://github.com/grasshorse/hwpc-gs) | Mobile-first route/ticket/customer app | Private |
| [grasshorse/hwpc-test](https://github.com/grasshorse/hwpc-test) | Playwright/Cucumber test suite for hwpc-gs | Private |
| [grasshorse/hwpc-bug](https://github.com/grasshorse/hwpc-bug) | Bug tracking | Private |

## Gitea Repos (cat9.me — nsadmin)

| Repo | Purpose | Relevance to HWPC | Access |
|------|---------|-------------------|--------|
| [nsadmin/ns-account](https://gitea.cat9.me/nsadmin/ns-account) | Multi-entity accounting, RoutePrint dev, QB migration tooling | Direct — primary HWPC dev repo | Private |
| [nsadmin/nsqbooks](https://gitea.cat9.me/nsadmin/nsqbooks) | Tax reconciliation system (TypeScript) — Form 1065 parsing, QB data reconciliation, audit reports | Direct — HWPC 1065 tax reconciliation | Private |
| [nsadmin/nscallbot](https://gitea.cat9.me/nsadmin/nscallbot) | Phone/chat bot (Candy-bot) | Direct — HWPC phone attendant | Private |
| [nsadmin/nspwa](https://gitea.cat9.me/nsadmin/nspwa) | PWA framework | Potential — mobile app foundation | Private |
| [nsadmin/nspwa-test](https://gitea.cat9.me/nsadmin/nspwa-test) | PWA test suite | Potential | Private |
| [nsadmin/nsgctime](https://gitea.cat9.me/nsadmin/nsgctime) | Google Calendar time tracking | Indirect — invoicing workflow | Private |
| [nsadmin/ns-site-template](https://gitea.cat9.me/nsadmin/ns-site-template) | Site deployment template | Infrastructure | Private |
| [nsadmin/docker-compose](https://gitea.cat9.me/nsadmin/docker-compose) | Docker configs | Infrastructure | Private |

### ns-account Repo Structure (HWPC-relevant areas)

The `ns-account` repo is a multi-entity accounting repo hosted on private Gitea. HWPC is one of several entities. Key HWPC areas:

```
Account/
├── .kiro/specs/                    # Kiro spec-driven development
│   ├── batch-flow-diagram/         # Batch invoice flow spec
│   ├── monthly-draft-generation/   # Monthly draft generation spec
│   ├── quickbooks-migration-tooling/ # QB migration spec
│   ├── route-ticket-printing/      # RoutePrint spec (primary HWPC feature)
│   └── ticket-lifecycle-workflow/  # Ticket lifecycle spec
├── hwpc-rpdev/                     # *** HWPC RoutePrint dev environment ***
│   ├── data/
│   │   ├── memorized-transactions/ # Looney Tunes test data (R20)
│   │   ├── QB2024-Exports/         # Exported QB2024 data (customers, invoices, items)
│   │   ├── QB2024-Imports/         # Import staging
│   │   ├── QBOL-Exports/          # QBOL export data
│   │   ├── QBOL-Imports/          # QBOL import CSVs (RLT test invoices)
│   │   └── verify-output/         # Route print PDF verification (old vs new)
│   ├── docs/                      # HWPC team docs, QBOL research, debug workflow
│   └── scripts/                   # seed_hwpc_data.py, setup-from-qb2024.py, verify-route-print.py
├── RCFjetlandTrust/hwpc/          # HWPC QB data and backups
│   ├── 2026QBOL-Testing/          # QBOL testing artifacts (PDFs, sample CSVs)
│   ├── BackupHWPC/                # QB .QBB backup files
│   ├── QBooks-Downgrade/          # QB2020 downgrade path (migration workaround)
│   │   ├── HWPC2024-Exports/      # Full QB2024 export set (chart of accounts, customers, etc.)
│   │   └── QuickbooksInstalls/    # QB2017 and QB2020 installers
│   ├── RoutePrintFeature/         # Route print screenshots, PDFs, QBOL artifacts
│   │   └── Routes_R1-17_QB2024/   # All 17 route prints from QB2024 (reference PDFs)
│   ├── Tax2024/                   # HWPC LLC 1065 tax return
│   └── Tax2025/                   # (in progress)
├── _tools/
│   ├── qb_gsheets/                # Google Sheets RoutePrint integration (gcode scripts)
│   └── qb_migration/              # *** Python migration toolkit ***
│       ├── qb_migration/          # Core modules (CLI, migration, route_tickets, web, tax)
│       ├── tests/                 # Full test suite (migration, route_tickets, web, tax, smoke)
│       ├── docs/                  # Batch process guide, lifecycle docs, migration walkthrough
│       └── examples/              # Demo scripts for each module
└── route_tickets.db               # SQLite database for route ticket system
```

Other entities in the repo (not HWPC): ATreesTrust, BFletcherTrust, BHaymondTrust, CTreesTrust, TurboTax.

## Legacy Repos (GitHub)

| Repo | Purpose |
|------|---------|
| [2cld/CAT_HWPC_Bug](https://github.com/2cld/CAT_HWPC_Bug) | Old JS ticket attempt |
| [2cld/HWPCold](https://github.com/2cld/HWPCold) | Original HWPC codebase (Delphi era) |

## Physical Machines

| Machine | Role | Access |
|---------|------|--------|
| HWPCmain | QB2024 Desktop, current production | ZeroTier + RustDesk |
| cat9fin | QB2024 restore target, migration testing, TurboTax | ZeroTier + RustDesk |
| nsUb2404hv | Dev server — nsadmin code projects | ZeroTier |
| nsdockerhv | Docker host — n8n, services | ZeroTier |

## Cloud Services

| Service | Purpose | Account |
|---------|---------|---------|
| QuickBooks Online (QBOL) | Target accounting system | HWPC Google account |
| Google Drive | QB backup transfer, shared docs | HWPC Google account |
| Google Business Profile | Maps listing, reviews | Ownership claim in progress |
| Google Sheets | Route data, time tracking | HWPC Google account |
| Google Maps | Route test maps | HWPC Google account |
| Vapi | Candy-bot voice AI | nsadmin |
| OpenAI | Candy-bot AI backend | nsadmin |
| Slack | Team comms (horseoff workspace) | Team |

## Active Epics (from wip.2cld.net)

These are tracked on [wip.2cld.net](https://wip.2cld.net/) — listed here for cross-reference:

| Epic | Project Tag | Status |
|------|-------------|--------|
| QBOL HWPC Route Print with Invoice import/export | cat9-hwpc-qbol | Migration complete, RoutePrint in progress |
| Wip repo + issue integration | wip-integration | In progress |
