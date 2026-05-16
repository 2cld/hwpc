# HWPC Mobile Device Setup (Template)

**Based on:** [netstack device support pattern](https://github.com/2cld/netstack/tree/master/docs/lan/compute/workstation)
**Status:** Active (2026-05-16)
**Cross-reference:** [wip EPIC: HWPC Operations Setup](https://github.com/2cld/wip) | [ops-device-management.md](https://github.com/2cld/wip/blob/main/docs/ops-device-management.md)

> **This is the TEMPLATE.** Actual device data goes in `devices/[device-name].md` (gitignored, never pushed). Copy this template to create a new device instance file.

## Device Info

| Field | Value |
|-------|-------|
| Device | [PHONE_MODEL] |
| OS | [OS_VERSION] |
| SIM | [CARRIER] / [PHONE_NUMBER] |
| Purpose | HWPC field ops — Route Print, voicemail, customer communication |
| Assigned to | [PERSON] ([EMAIL]) |
| Setup date | [DATE] |

## Accounts Configured

| Account | Service | Purpose |
|---------|---------|---------|
| cat@hawkeyewestpestcontrol.com | Gmail / Google Workspace | LLC manager email |
| bug@hawkeyewestpestcontrol.com | Gmail / Google Workspace | Ops coordination (Mark + team) |
| [ZT_ACCOUNT] | ZeroTier | Remote network access ([ZT_IP]) |

## Services Accessible

| Service | URL / Access | Status |
|---------|-------------|--------|
| HWPC Route Print | [RP_URL] | [ ] |
| Voicemail | Phone native | [ ] |
| Email (cat@hwpc) | Gmail app | [ ] |
| Email (bug@hwpc) | Gmail app | [ ] |
| ZeroTier | ZeroTier app | [ ] |

## Network

| Network | IP | Purpose |
|---------|-----|---------|
| ZeroTier | [ZT_IP] (10.147.17.x) | Access to cf/sl/wf nodes |
| Local WiFi (HWPC office) | [WIFI_IP] | Office network access |
| Cellular | [CELL_IP] | Field access |

## Voicemail Setup

- Greeting: [DESCRIBE_GREETING]
- Forwarding: [DOES_VM_NOTIFY_EMAIL]
- Access: [HOW_TO_CHECK_REMOTELY]

## Route Print Mobile Access

- URL: [RP_URL]
- Auth: [AUTH_METHOD]
- Tested: [ ] [DATE]

## Backup / Recovery

- Phone backup method: [ICLOUD_OR_GOOGLE]
- Account recovery: All accounts use hawkeyewestpestcontrol.com domain
- If phone is lost/broken: [REPLACEMENT_PROCEDURE]

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
10. Document device in `devices/[device-name].md` (copy this template)
11. Update ZeroTier map in wip (ops-storage-management.md)

## Creating a Device Instance

```bash
# From the hwpc repo root:
cp docs/hwpc-ops/hwpc-mobile-device.md docs/hwpc-ops/devices/[device-name].md
# Edit the new file with actual values
# It will NOT be committed (gitignored)
```

## Related Docs

- [netstack device pattern](https://github.com/2cld/netstack/tree/master/docs/lan/compute/workstation) — template for device docs
- [wip ops-device-management.md](https://github.com/2cld/wip/blob/main/docs/ops-device-management.md) — device inventory
- [wip ops-storage-management.md](https://github.com/2cld/wip/blob/main/docs/ops-storage-management.md) — ZeroTier network map
- [hwpc.2cld.net](https://hwpc.2cld.net) — HWPC operations site
