[edit](https://github.com/2cld/hwpc/edit/master/docs/hwpc-ops/README.md)

# HWPC Operations (Internal)

> **WARNING:** This document contains internal network addresses, file paths, and operational details. Do NOT put credentials, passwords, or API keys here — this repo is public. Use this for procedural notes that reference authenticated resources.

## Weekly Meeting

- Sundays 3-5pm CST
- Coordination page: [hwpc.2cld.net](https://hwpc.2cld.net/)
- Meeting link: requires authenticated access (check team channel)
- Agenda:
  - HWPC LLC Operation Agreement
  - HWPC LLC Buy Sell Agreement
  - Confirm HWPC Property depreciation
  - Review Customer Invoices
  - Review Banking
  - Review Withholding

## Internal Network Access

Access to dev/test environments requires ZeroTier network approval. Contact ghadmin for access.

- Remote access tool: [rustdesk releases](https://github.com/rustdesk/rustdesk/releases/tag/1.4.3) / [web remote](https://rustdesk.com/web/)

## QB2024 Backup Procedure

### Backup from HWPCmain
1. Go to HWPCmain
2. Start QuickBooks → Close all windows
3. File → Company → Create local backup
4. Browse to local backup folder
5. Run Backup

### Transfer via Google Drive
1. Login to HWPC Google account
2. Go to drive.google.com
3. My Drive → HWPC-Export → HWPC-toQBOnline → BackupToGoQBOL
4. Upload the .QBB backup file

### Restore on cat9fin
1. Go to cat9fin
2. Login to HWPC Google account → download .QBB from Drive
3. Start QuickBooks → Open or Restore a Company → Restore a backup
4. Browse to downloaded .QBB file
5. Restore to Company Files directory

## 2025 Tax Reports Status

- QB2024 on HWPCmain — current working copy
- QB2024 restored on cat9fin — for migration testing
- TurboTax 2024/2025 installed on cat9fin

### Tax Filing Workflow
1. Make QBooks corrections with Mark on HWPCmain
2. Backup and share via HWPC Google account
3. Run tax reports → compare to prior year filed returns
4. Repeat until TurboTax matches actual filed PDFs
5. File 2025 HWPC LLC 1065
6. File 2025 personal 1040s

## Migration Plan (QB2024 → QBOL)

Current status: Invoice print formats did not import cleanly to QBOL.

### Known Issues
- QBOL batch invoice/service ticket features require additional subscription
- Invoice formatting needs to be rebuilt in QBOL
- Exploring custom plugin development as alternative

### Migration Steps
1. Keep using QB2024 for current operations
2. Chris works on batch Invoice Route Print in QBOL
3. Mark continues tickets the old way during transition
4. Run tax reports from QB2024
5. Continue cleanup passes (customers, banks, categories)
6. Import to QBOL from clean QB2024 data
7. Repeat until Mark runs tickets from new system

## Research & Tools

- Google Sheets route data: [HWPC Routes sheet](https://docs.google.com/spreadsheets/d/1XZotISYBmbW1XCl1l35aHwgtgXDwfI_IXkaPK4ER8kU/edit?gid=0#gid=0)
- Google Maps route test: [HWPC Route Test map](https://www.google.com/maps/d/edit?mid=1mfA1dAilxp2wea3IAS_KqlikhIT1s4M)
- NotebookLM Routes: [notebook](https://notebooklm.google.com/notebook/a8276b19-1b41-4887-850f-c7f4b2b9ae75?pli=1)
- n8n callbot: [nscallbot repo](https://gitea.cat9.me/nsadmin/nscallbot)
- cat9bot test line: check team channel for number
