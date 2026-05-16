# HWPC Mobile Device Setup

**Based on:** [netstack device support pattern](https://github.com/2cld/netstack/tree/master/docs/lan/compute/workstation)
**Status:** Active (2026-05-16)
**Cross-reference:** [wip EPIC: HWPC Operations Setup](https://github.com/2cld/wip) | [ops-device-management.md](https://github.com/2cld/wip/blob/main/docs/ops-device-management.md)

## Device Info

| Field | Value |
|-------|-------|
| Device | TBD (phone model) |
| OS | TBD (iOS / Android version) |
| SIM | TBD (carrier, number) |
| Purpose | HWPC field ops — Route Print, voicemail, customer communication |
| Assigned to | HWPC operations (bug@hawkeyewestpestcontrol.com) |
| Setup date | 2026-05-15 |

## Accounts Configured

| Account | Service | Purpose |
|---------|---------|---------|
| cat@hawkeyewestpestcontrol.com | Gmail / Google Workspace | LLC manager email |
| bug@hawkeyewestpestcontrol.com | Gmail / Google Workspace | Ops coordination (Mark + team) |
| TBD | ZeroTier | Remote network access (10.147.17.x) |

## Services Accessible

| Service | URL / Access | Status |
|---------|-------------|--------|
| HWPC Route Print | hwpc-rp (via browser) | ✅ Working |
| Voicemail | Phone native | ✅ Set up |
| Email (cat@hwpc) | Gmail app | TBD |
| Email (bug@hwpc) | Gmail app | TBD |
| ZeroTier | ZeroTier app | TBD |

## Network

| Network | IP | Purpose |
|---------|-----|---------|
| ZeroTier | TBD (10.147.17.x) | Access to cf/sl/wf nodes |
| Local WiFi (HWPC office) | TBD | Office network access |
| Cellular | TBD | Field access |

## Voicemail Setup

- Greeting: TBD (document what was recorded)
- Forwarding: TBD (does voicemail notify via email?)
- Access: TBD (how to check remotely)

## Route Print Mobile Access

- URL: TBD (hwpc-rp address accessible from phone)
- Auth: TBD (how does the phone authenticate)
- Tested: ✅ 2026-05-15

## Backup / Recovery

- Phone backup method: TBD (iCloud / Google backup)
- Account recovery: All accounts use hawkeyewestpestcontrol.com domain
- If phone is lost/broken: TBD (document replacement procedure)

## Setup Procedure (for future devices)

1. Activate SIM / carrier setup
2. Configure WiFi (HWPC office + home networks)
3. Add Google account (cat@hawkeyewestpestcontrol.com)
4. Add Google account (bug@hawkeyewestpestcontrol.com)
5. Install Gmail app, configure both accounts
6. Install ZeroTier, join network d5e5fb65371eb4a4
7. Test Route Print access via browser
8. Set up voicemail greeting
9. Test inbound/outbound calls
10. Document device in this file + update ZeroTier map in wip

## Related Docs

- [netstack device pattern](https://github.com/2cld/netstack/tree/master/docs/lan/compute/workstation) — template for device docs
- [wip ops-device-management.md](https://github.com/2cld/wip/blob/main/docs/ops-device-management.md) — device inventory
- [wip ops-storage-management.md](https://github.com/2cld/wip/blob/main/docs/ops-storage-management.md) — ZeroTier network map
- [hwpc.2cld.net](https://hwpc.2cld.net) — HWPC operations site
