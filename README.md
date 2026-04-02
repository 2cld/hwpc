[edit](https://github.com/2cld/hwpc/edit/master/README.md)

# HWPC - Hawkeye West Pest Control

Project coordination site for HWPC development and operations.

> This is a public site. Private operational details, credentials, and internal network info are maintained in authenticated resources linked below.

## Active Projects

| Project | Description | Repo | Status |
|---------|-------------|------|--------|
| hwpc-gs | Mobile-first route/ticket/customer app (replacing old Delphi program) | [grasshorse/hwpc-gs](https://github.com/grasshorse/hwpc-gs) | Active |
| hwpc-test | Playwright/Cucumber testing for hwpc-gs | [grasshorse/hwpc-test](https://github.com/grasshorse/hwpc-test) | Active |
| QBOL Migration | QB2024 Desktop to QuickBooks Online migration | [QBOL Notes](./docs/hwpc-QBOL-notes/) | In Progress |
| Google Business | Google Maps / Business Profile cleanup | [Google Notes](./docs/hwpc-google/) | In Progress |
| Candy-bot | Automated phone/chat/email attendant | [nscallbot](https://gitea.cat9.me/nsadmin/nscallbot) | Research |

## Documentation

- [Project Docs Index](./docs/) — all project documentation
- [hwpc-rpdev Developer Guide](./docs/hwpc-rpdev/) — RoutePrint dev setup, architecture, and workflow
- [hwpc-gs App Demo & Screenshots](./docs/hwpc-gs/) — mobile app screenshots and demo info
- [QBOL Migration Notes](./docs/hwpc-QBOL-notes/) — QuickBooks Online migration research
- [Google Business Setup](./docs/hwpc-google/) — Google Maps and Business Profile instructions
- [Testing](./docs/hwpc-test/) — test framework and approach
- [Operations](./docs/hwpc-ops/) — internal ops notes (requires authenticated access)
- [Ecosystem Map](./docs/hwpc-ecosystem/) — all repos, sites, machines, and services across the project
- [wip ↔ hwpc Sync Guide](./docs/hwpc-wip-sync/) — how info flows between wip.2cld.net and this site
- [Review Queue](./docs/hwpc-review/) — research links and WIP notes to triage

## Related Sites

| Site | Purpose | Repo |
|------|---------|------|
| [hawkeyewestpestcontrol.com](https://www.hawkeyewestpestcontrol.com/) | Main business site | [repo](https://github.com/christrees/hawkeyewestpestcontrol.com) |
| [hwpest.com](https://hwpest.com/) | Alternate domain | [repo](https://github.com/christrees/hwpest.com) |
| [hwpc.net](https://hwpc.net/) | Alternate domain | [repo](https://github.com/christrees/hwpc.net) |
| [hwpc.2cld.net](https://hwpc.2cld.net/) | This dev coordination site | [repo](https://github.com/2cld/hwpc) |

## Legacy Code

- [CAT_HWPC_Bug](https://github.com/2cld/CAT_HWPC_Bug) — old JS attempt
- [HWPCold](https://github.com/2cld/HWPCold) — original codebase

## QBOL - Route Ticket Printing (Quick Reference)

The core workflow for generating route tickets in QuickBooks Online:

1. Memorized Transaction → Route Group
2. Pick Date of Route → generates new invoices (not yet printed)
3. File → Print Forms → Invoices (Accounts Receivable)
4. Select Template from list → print to "deliver" the invoice to customer statement
5. Templates can be edited via Layout (positioning) and Customization (data fields)

See [QBOL Notes](./docs/hwpc-QBOL-notes/) for detailed steps on custom invoices, recurring invoices, and batch printing.

## Goals

- Mark can run daily routes from his phone
- Automated phone/chat/email response (Candy-bot)
- Continuous accounting and tax reporting
- Increase Google rating and Maps presence

## Weekly Sync

Sundays 3-5pm CST — see [Operations](./docs/hwpc-ops/) for meeting link and agenda details.

## MVP Roadmap

- [ ] Fix Google Ads / Business Profile
- [ ] Route printing from QBOL (batch invoice workflow)
- [ ] Mobile route management (hwpc-gs)
- [ ] Candy-bot phone attendant
- [ ] Route scheduling
- [ ] Continuous tax reporting

## Current ToDo

- [ ] Contact Google — [instructions](./docs/hwpc-google/)
- [ ] Verify reports and database for full mobile
- [ ] Mark prints routes (computer and phone)
- [ ] Work through QBOL online access
- [ ] Import and verify account status in QBOL
- [ ] Final customer balance cleanup
- [ ] Final bank and category cleanup
- [ ] 2025 tax reports and filing
- [x] Review customer balances
- [x] Review banks and categories
- [x] QB2024 on cat9fin import and restore
- [x] Initial cleanup pass
