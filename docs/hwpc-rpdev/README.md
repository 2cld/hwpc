[edit](https://github.com/2cld/hwpc/edit/master/docs/hwpc-rpdev/README.md)

# HWPC RoutePrint Development Guide

> This doc points developers to the right repo and gets them oriented. The actual code lives in a private Gitea repo — you'll need access granted by ghadmin.

## What Is RoutePrint?

RoutePrint is the system that generates pest control route tickets (invoices) for HWPC. The old workflow used QuickBooks 2024 Desktop memorized transactions to batch-print route tickets. The new system replaces that with a Python/Flask web app that can:

- Import customer and invoice data from QB2024 CSV exports
- Generate route ticket invoices matching the old QB2024 print format
- Export invoices as CSV for import into QuickBooks Online (QBOL)
- Manage the full ticket lifecycle (draft → review → dispatch → print → reconcile)
- Provide a monthly dashboard, schedule calendar, and reporting

## Where's the Code?

| What | Where | Access |
|------|-------|--------|
| Migration toolkit + route ticket system | [nsadmin/ns-account](https://gitea.cat9.me/nsadmin/ns-account) `_tools/qb_migration/` | Private Gitea — request access from ghadmin |
| HWPC dev instance (data + scripts) | [nsadmin/ns-account](https://gitea.cat9.me/nsadmin/ns-account) `hwpc-rpdev/` | Same repo |
| Google Sheets RoutePrint (alternate approach) | [nsadmin/ns-account](https://gitea.cat9.me/nsadmin/ns-account) `_tools/qb_gsheets/` | Same repo |
| Kiro specs (requirements, design, tasks) | [nsadmin/ns-account](https://gitea.cat9.me/nsadmin/ns-account) `.kiro/specs/` | Same repo |
| QB2024 reference route prints (PDFs) | [nsadmin/ns-account](https://gitea.cat9.me/nsadmin/ns-account) `RCFjetlandTrust/hwpc/RoutePrintFeature/` | Same repo |
| Mobile app (future) | [grasshorse/hwpc-gs](https://github.com/grasshorse/hwpc-gs) | Private GitHub |

Local path on cat9fin: see team channel for machine-specific paths.

## Quick Start (on cat9fin)

```bat
REM path is machine-specific — check .env or team channel
cd <ns-account-path>\hwpc-rpdev
start-dev.bat
```

Opens at `http://localhost:5001` — default dev credentials are in the `.env` file (not committed to repo).

If no database exists, `start-dev.bat` creates one from the QB2024 exports in `data/QB2024-Exports/`.

## Architecture

The tooling follows a generic-tools-plus-account-data pattern:

```
Account/
├── _tools/qb_migration/       ← reusable tool (no account-specific data)
│   ├── qb_migration/
│   │   ├── migration/         ← CSV parsing, transformation, validation
│   │   ├── route_tickets/     ← customer import, invoices, scheduling, reports
│   │   ├── tax_integration/   ← tax export, audit, year-over-year
│   │   ├── web/               ← Flask app (dashboard, print, review, export)
│   │   └── cli.py             ← command-line interface
│   ├── tests/                 ← full test suite
│   └── config/                ← config templates
│
├── hwpc-rpdev/                ← HWPC-specific dev instance
│   ├── data/                  ← QB2024 exports, QBOL imports, test data
│   ├── scripts/               ← setup, seed, verify scripts
│   ├── start-dev.bat          ← run the server
│   └── run-import.bat         ← rebuild DB from QB2024 exports
│
└── RCFjetlandTrust/hwpc/      ← HWPC account data (backups, tax, reference PDFs)
```

## Development Workflow

The debug loop (see `hwpc-rpdev/docs/README-DEBUG-WORKFLOW.md` in the repo):

1. Export CSVs from QB2024 → `hwpc-rpdev/data/QB2024-Exports/`
2. `run-import.bat` — builds SQLite DB from exports
3. `start-dev.bat` — start Flask server, generate drafts, print
4. `python scripts\verify-route-print.py --route R1 --date 2026-06-01` — compare output vs QB2024 reference
5. Fix issues in `_tools/qb_migration/` → repeat

## Kiro Specs

The project uses Kiro spec-driven development. Specs live in `.kiro/specs/`:

| Spec | What it covers |
|------|---------------|
| `route-ticket-printing/` | Core RoutePrint feature — print format, templates, PDF generation |
| `ticket-lifecycle-workflow/` | Draft → review → dispatch → print → reconcile flow |
| `batch-flow-diagram/` | Batch invoice generation and processing |
| `monthly-draft-generation/` | Monthly draft auto-generation |
| `quickbooks-migration-tooling/` | QB2024 → QBOL data migration pipeline |

## Key Pages (when server is running)

| Page | URL |
|------|-----|
| Monthly Dashboard | http://localhost:5001/routes/monthly-dashboard |
| Ticket List | http://localhost:5001/routes/tickets/view |
| Invoice Review | http://localhost:5001/routes/invoices/review |
| Invoice Export | http://localhost:5001/routes/invoices/export |
| Route Print (QB2024 style) | http://localhost:5001/routes/print?route_id=1&date=2026-06-01&format=oldqb2024 |
| Schedule Calendar | http://localhost:5001/routes/schedules/calendar |
| Reports | http://localhost:5001/routes/reports |
| Route Definitions | http://localhost:5001/routes/route-definitions |

## Test Data

The project uses "Looney Tunes" (LT) characters as safe demo data:
- Route R20 with Looney Tunes test invoices in `data/memorized-transactions/`
- `seed_demo_data.py` creates LT demo data
- `seed_hwpc_data.py` creates real HWPC data (not committed to repo)

## Running Tests

```bash
cd _tools/qb_migration
pip install -r requirements.txt
pip install -e .
pytest
```

## Requirements

- Python 3.9+
- SQLite (dev) / PostgreSQL (production)
- Flask
- Access to QB2024 CSV exports (in `hwpc-rpdev/data/`)

## Related Docs

- [QBOL Migration Notes](../hwpc-QBOL-notes/) — migration status, timeline, research
- [Ecosystem Map](../hwpc-ecosystem/) — full repo and service map
- [HWPC Main Page](../../) — project overview and todo list
