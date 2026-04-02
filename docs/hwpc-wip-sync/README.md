[edit](https://github.com/2cld/hwpc/edit/master/docs/hwpc-wip-sync/README.md)

# HWPC ↔ wip.2cld.net Sync Guide

## The Deal

- [wip.2cld.net](https://wip.2cld.net/) is the daily capture tool — fast, messy, stream-of-consciousness. It should stay that way.
- [hwpc.2cld.net](https://hwpc.2cld.net/) is the canonical home for all HWPC project info — organized, reviewable, shareable.
- Wip captures. HWPC absorbs. Wip links back. Nobody maintains info in two places.

## Tags wip Already Uses

These `@project` tags on wip.2cld.net identify HWPC-related items:

| Tag | Meaning | Absorb Into |
|-----|---------|-------------|
| `@project:cat9-hwpc-qbol` | QuickBooks / QBOL migration work | [QBOL Notes](../hwpc-QBOL-notes/) |
| `@project:cat9-hwpc-*` | Any HWPC-tagged project | Appropriate hwpc doc |

Other tags that may contain HWPC-relevant items:
| Tag | Check For |
|-----|-----------|
| `@project:accounting` | Tax filing items related to HWPC LLC |
| `@project:nsadmin` | nsqbooks, nscallbot, nspwa work that touches HWPC |

## How to Sync (Manual — Do This Weekly)

### 1. Scan wip for HWPC items

Check these sections on [wip.2cld.net](https://wip.2cld.net/):
- **Today / History** — look for hwpc/QBOL/RoutePrint mentions
- **Epics** — the QBOL HWPC epic and its Definition of Done
- **Inbox** — items tagged `hwpc:` or `@project:cat9-hwpc-*`
- **Open code Projects** — hwpc section

Also check:
- [wip docs/hwpc-notes](https://wip.2cld.net/docs/hwpc-notes) — should be just a pointer
- [wip docs/business-research](https://wip.2cld.net/docs/business-research) — tax links may be HWPC-relevant

### 2. Absorb into hwpc.2cld.net

| What you find | Where it goes here |
|---------------|-------------------|
| QBOL how-to, research, Q&A | [docs/hwpc-QBOL-notes/](../hwpc-QBOL-notes/) |
| Migration status, timeline events | [docs/hwpc-QBOL-notes/](../hwpc-QBOL-notes/) migration status section |
| RoutePrint epic tasks / progress | [docs/hwpc-QBOL-notes/](../hwpc-QBOL-notes/) or main README todo |
| Repo/tool/service discoveries | [docs/hwpc-ecosystem/](../hwpc-ecosystem/) |
| Random research links, ideas | [docs/hwpc-review/](../hwpc-review/) review queue |
| Ops procedures, machine notes | [docs/hwpc-ops/](../hwpc-ops/) |
| Google business / social media | [docs/hwpc-google/](../hwpc-google/) |
| App dev (hwpc-gs) notes | [docs/hwpc-gs/](../hwpc-gs/) |

### 3. Update wip to link back

Once info is absorbed here, wip entries can be simplified to a link:

```
hwpc: RoutePrint invoice import → https://hwpc.2cld.net/docs/hwpc-QBOL-notes/
```

Wip doesn't need to delete the history entries (those are a log). But inbox items and epic details that have been absorbed can be replaced with a pointer.

### 4. What wip should NOT remove

- **History/log entries** — these are a timeline, leave them
- **Epic status line** — keep the one-liner status + link to hwpc for details
- **@project tags** — these are how we find things, keep tagging

### 5. What wip CAN simplify after sync

- **Inbox items** tagged hwpc — replace with link once captured in hwpc review queue
- **Epic Definition of Done details** — replace with link to hwpc.2cld.net tracking
- **Inline QBOL research** — replace with link to hwpc QBOL notes

## Future: Automation Ideas

The manual sync above could eventually be scripted:

- Scrape wip.2cld.net for `@project:cat9-hwpc-*` tagged items
- Diff against what's already in hwpc review queue
- Auto-generate new review queue entries
- n8n workflow or GitHub Action on a schedule

For now, the weekly manual scan during Sunday sync is fine.

## Quick Reference for wip Contributors

If you're working on wip.2cld.net and touching HWPC stuff:

1. Tag it `@project:cat9-hwpc-qbol` (or appropriate `cat9-hwpc-*` tag)
2. Capture freely — don't worry about formatting or where it goes
3. HWPC sync will pick it up and absorb it
4. Canonical HWPC info lives at [hwpc.2cld.net](https://hwpc.2cld.net/)
5. When in doubt, just drop a link: `https://hwpc.2cld.net/docs/hwpc-QBOL-notes/`
