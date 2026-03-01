[edit](https://github.com/2cld/hwpc/edit/master/README.md) 

- [github rustdesk](https://github.com/rustdesk/rustdesk/releases/tag/1.4.3) - [web remote](https://rustdesk.com/web/)

# Chris's conclusion
- Keep using old QB2024 for this week
- Chris figures out the batch Invoice Route Print shit
- Mark keeps running tickets this week the old way
- Quickbooks suggests to just delete and re-import
- Mark and Chris runs Tax Reports on QB2024 (TODAY)
- We do more cleanup...
  - Chris understands how Mark is doing Invoice Route Print
  - Chris and Mark get Tax Reports ran for Accountant
  - Chris backs it up and moves to new machine
  - We do new Import to QBOL from new machine
  - Repeat until Mark actually runs Tickets from the new Machine
 
# Update on QB2024 to QBOL
- The format for the Invoices (printing) did not import
- QBOL has Service Ticket Batch stuff, but they want to charge mo-money... f-that
- I did look into reformating the invoice print.  It is possible...
- I started looking at the export and import of the "all ready" printed tickets
- I did get to the screen to import tickets via cvs
- When looking deeper into invoice generation, most people use another QBOL plugin
- WELL...FUCK, I can write a plugin...

# ToDo
- [ ] Contact Google [instructions hwpc-google](./docs/hwpc-google/) (chris mark)
- [ ] Chris verifies reports and database to move to full mobile
- [ ] Mark prints Routes (computer and phone hopefully)
- [ ] Work through Online access... make sure mark can access and cat9fin and HWPCMain computer can access
- [ ] On HWPCMain Quickbooks push the OnLine import button..
- [ ] Import 2026-preQBOnline-HWPCLLC verify account status
- [ ] Backup HWPCMain Quickbooks (chris) post 2026-preQBOnline-HWPCLLC file (mark chris) and share via candy@hawkeyewestpestcontrol.com
- [ ] Final HWPCMain QBooks file cleanup (chris mark)
- [ ] Take reports and Tax shit to your Accountant (mark - should be easy for them, but they should review)
- [ ] Finalize 2025 tax plan
- [ ] Setup printing test from cat9fin (chris)
- [ ] Final cleanup customer balances (chris mark)
- [ ] Final cleanup "banks" (chris mark)
- [ ] Final cleanup "categories" (chris mark)
- [ ] Review possible distribution changes
- [ ] 2025 RC 1040 Tax
- [ ] 2025 Mark 1040 Tax
- [ ] 2025 HWPC 1065 Tax Report print
- [ ] -->GOTO-REPEATStart: until TurboTax 2025 HWPC 1065 is ready to File
- [ ] -->REPEAT: Make QBooks corrections with Mark on HWPCMain (chris mark)
- [ ] -->REPEAT: 2025 HWPC, Tax to Actual Filed PDF HWPC, LLC 2025 1065 (chris)
- [ ] -->REPEATStart: Backup HWPCMain Quickbooks (chris) post Mark/Chris Cleanup and share via candy@hawkeyewestpestcontrol.com
- [ ] 2025 TurboTax Business import for HWPC
- [ ] -->GOTO-REPEATStart: until TurboTax 2024 HWPC matches actual PDF 2024 TurboTax file
- [ ] -->REPEAT: Make QBooks corrections with Mark on HWPCMain (chris mark)
- [ ] -->REPEAT: Match 2024 HWPC, Tax to Actual Filed PDF HWPC, LLC 2024 1065 (chris)
- [ ] -->REPEATStart: Backup HWPCMain Quickbooks (chris) post Mark/Chris Cleanup and share via candy@hawkeyewestpestcontrol.com
- [X] Review customer balances (chris mark)
- [X] Review "banks" (chris mark)
- [X] Review "categories" (chris mark)
- [X] PDF of HWPC, LLC 2024 1065 (mark)
- [X] TurboTax 2024 import from QBooks 2024 test (chris)
- [X] TurboTax 2025 personal on cat9fin EOY Quickbooks (chris)
- [X] TurboTax 2024 personal on cat9fin EOY Quickbooks (chris)
- [X] TurboTax 2025 business on cat9fin EOY Quickbooks (chris)
- [X] TurboTax 2024 business on cat9fin EOY Quickbooks (chris)
- [X] QBooks 2024  on cat9fin an HWPC import Quickbooks (chris)
- [X] Cleanup pass one (Mark) DONE - 20250219 
- [X] Call Quickbooks (Mark) DONE - Desktop expires in March
- [X] Backup HWPCMain Quickbooks (chris) move to catwin11 and restore DONE - login with hwpc to view
- [X] Don't burn everything down and dance naked in the ashe
- tbd

## from wip.2cld.net
- [hwpc](https://hwpc.2cld.net) stuff [github repo](https://github.com/2cld/hwpc)
  - hwpc Ops Agreement (in md)
  - hwpc Buy Sell Agreement (in md)
  - hwpc export attempt
  - hwpc qb backup
  - hwpc account
  - qbooks cleanup
  - qbooks online
- candybot va nsadmin
  - https://dashboard.vapi.ai/login
  - https://platform.openai.com/settings/organization/usage
  - https://platform.openai.com/docs/quickstart
  - https://horseoffworkspace.slack.com/account/settings
  - https://app.slack.com/client/T09QXQ57BPT/platform
  - https://github.com/settings/security
  - manual
  - sync workflow
  - simple build workflow

# hwpc weekly Sunday 3-5pm CST
- this document [https://hwpc.2cld.net/](https://hwpc.2cld.net/)
- HWPCmain 10.147.17.96 Account [zt](https://my.zerotier.com/network/d5e5fb65371eb4a4)
- cat9fin 10.147.17.218 cat [zt](https://my.zerotier.com/network/d5e5fb65371eb4a4)
- GoogleMeet [HWPC-meeting](https://meet.google.com/zrf-racv-dgt)
- Agenda
  - HWPC LLC Operation Agreement
  - HWPC LLC Buy Sell Agreement
  - Confirm HWPC Property ? 2026 Depreiation ??
  - Review Customer Invoices
  - Review Banking
  - Review Witholding

## mvp
- Fix Google Ads [https://hwpc.2cld.net/](https://hwpc.2cld.net/)
- rebuild win11vm (ran out of space in installs) (250GB next time??)
- Install TurboTax 2023, 2024, 2025
- Install quickbooks
- 2025 Tax Planning - based off of LLC Template
- callbot - Answer phone 
- callbot - Take message
- callbot - Message notification
- callbot - Callback planning
- Route Scheduling

# hwpc cleanup
- Goals
  - Mark can run from phone
    - [https://github.com/grasshorse/hwpc-gs](https://github.com/grasshorse/hwpc-gs)
  - Automatic phone, chat and email response / attendent ( Candy-bot )
    - [https://gitea.cat9.me/nsadmin/nscallbot](https://gitea.cat9.me/nsadmin/nscallbot)
    - cat9bot - test main • ‪(605) 205-3234‬
  - Continuious tax ?? nstaxbot ??
    - christrees - [Trust Template](https://drive.google.com/drive/folders/1ZkjBa23OeKdM0mG6DxISU7uZqUqZDMoX)
    - quickbooks backup
    - Tax pre-planning
    - Auto tax reports
- Time: 20hr / week to 1/25
- Evaluation metrics
  - Mark uses it
  - Mark can manage dailies from his phone
  - Reduce taxes
  - continious accounting
  - Increase google rating [google business](https://business.google.com/create?skipLandingPage&service=ome&original_intent=GMB&omesrcexp=97643701&omec=ELXZxy4YAiIBATIBAUABShMIzKPruOWukAMVTdZLAx3GtRi0)

# hwpc test
- Test [http://10.147.17.219:3000/](http://10.147.17.219:3000/)
  - Tickets [http://10.147.17.219:3000/tickets](http://10.147.17.219:3000/tickets)
  - Customers [http://10.147.17.219:3000/customers](http://10.147.17.219:3000/customers)
  - Routes [http://10.147.17.219:3000/routes](http://10.147.17.219:3000/routes)
  - Reports [http://10.147.17.219:3000/reports](http://10.147.17.219:3000/reports)
- [docs](./docs)
  - [hwpc-gs](./docs/hwpc-gs) or [gh hwpc-gs repo](https://github.com/grasshorse/hwpc-gs)
  - [hwpc-bug](./docs/hwpc-bug) or [gh hwpc-bug repo](https://github.com/grasshorse/hwpc-bug)
- [https://www.hawkeyewestpestcontrol.com/](https://www.hawkeyewestpestcontrol.com/) site holder [hawkeyewestpestcontrol.com repo](https://github.com/christrees/hawkeyewestpestcontrol.com)
- [https://hwpest.com/](https://hwpest.com/) site holder [hwpest.com repo](https://github.com/christrees/hwpest.com)
- [https://hwpc.net/](https://hwpc.net/) site holder [hwpc.net repo](https://github.com/christrees/hwpc.net)
- repo https://github.com/2cld/hwpc
- Old js attempt https://github.com/2cld/CAT_HWPC_Bug
- Old code https://github.com/2cld/HWPCold
- ct sites.google.com hawkeyewestpestcontrol
- ct sites.google.com Routes HWPC
- ct [noetbooklm - Routes](https://notebooklm.google.com/notebook/a8276b19-1b41-4887-850f-c7f4b2b9ae75?pli=1)

# hwpc n8n research
- now at [https://gitea.cat9.me/nsadmin/nscallbot](https://gitea.cat9.me/nsadmin/nscallbot)

## hwpc from wip.2cld.net
- Review HWPC
  - Review email setup
    - really only need to save candy@hawkeyewestpestcontrol.com
    - Document how to get [https://business.google.com/add](https://business.google.com/add) google maps [claim business on google](https://www.google.com/search?q=get+my+business+on+google+maps&sca_esv=97f87ef5af16174d&rlz=1C1CHFX_enUS1166US1166&sxsrf=AE3TifN0-lmBWcnGGNLM3CL-SPc6RJUOlQ%3A1760819332216&ei=hPjzaPD-DOTMp84P-amcyQ0&ved=0ahUKEwjw0L2Wy66QAxVk5skDHfkUJ9kQ4dUDCBE&uact=5&oq=get+my+business+on+google+maps&gs_lp=Egxnd3Mtd2l6LXNlcnAiHmdldCBteSBidXNpbmVzcyBvbiBnb29nbGUgbWFwczIFEAAYgAQyBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB5I3dkBUIB5WOzMAXAFeAGQAQCYAasBoAG1E6oBBDI4LjS4AQPIAQD4AQGYAiWgAs0VwgIKEAAYsAMY1gQYR8ICChAjGIAEGCcYigXCAgQQIxgnwgILEAAYgAQYkQIYigXCAgoQABiABBhDGIoFwgINEAAYgAQYsQMYQxiKBcICEBAuGIAEGNEDGEMYxwEYigXCAggQABiABBixA8ICDhAuGIAEGLEDGIMBGIoFwgIOEC4YgAQYxwEYjgUYrwHCAgsQLhiABBixAxiDAcICCxAuGIAEGMcBGK8BwgILEAAYgAQYsQMYgwHCAgsQLhiABBjRAxjHAcICDhAuGIAEGLEDGNEDGMcBwgIIEAAYBRgNGB7CAggQABgIGA0YHsICCxAAGIAEGIYDGIoFwgIIEAAYFhgKGB6YAwCIBgGQBgiSBwQzMC43oAfJggKyBwQyNS43uAedFcIHBjItMzIuNcgH4QE&sclient=gws-wiz-serp)
    - prepare to abandon google (backup and re-direct)
  - Review google business stuff
    - could use google voice attendance right now
    - Extend what I'm doing with my LLC accounting to quickbooks?
  - write-up work plan
- cat9do simple pwa with calendar ?? on nsdockerhv need to put in gitea.cat9.me
  - [hwpc bookmarks](chrome://bookmarks/?id=1473)
  - [google/aimode simple pwa svelite](https://www.google.com/search?udm=50&aep=11&q=I%27m+a+dev+starting+a+mobile+first+project+for+a+Pest+Control+company.++I%27m+looking+to+do+a+PWA+that+uses+tailwinds+css+and+an+sqlite+server+side+back-end+that+the+mobile+apps+can+sync+to+but+work+offline.++I%27m+looking+at+svelte+as+a+possible+framework%2C+can+you+suggest+or+generate+a+template+with+basic+CRUD+and+css%3F&mtid=RY3aaNawCMy8ptQPrd-Y0Qc&mstk=AUtExfC39cwVHTrgodPbpG5Km4Xuhg1wYJbNzRiLdEHvMEdb7C7zJrCy4cO-WLev0ml3QvDWTP1W12NEBEuVCEJ5o0A6QEYuEW0VyzV4FHRJBRoU2hK9DI_Vfbn9DOpv-yC90zjmZ9ErH78vU1eAU-_gwTcSs-3RLKzUiSkjNjYFCOBwIGB6P-TosFFSNpK7arsEWWBEqrkX-KW9fmAYfyW4s01-nrC9rM_JVISo2gV5C92pskbRqYqzL4f-Nb8zwaJgSbgOmVTtMaeOeSNp4eCfAtktqkpnM1XJ-oRstTG0J4upn9NrJC1KauPx-s_h5uFSZfMPODZ0YVqMfw&csuir=1)
  - [google/aimode n8n calendar](https://www.google.com/search?udm=50&aep=11&q=I%27m+a+dev+using+n8n+and+I+want+to+pull+my+google+calendar+events+and+put+them+in+a+table%2C+filter+by+the+title%2C+then+put+them+back+in+a+google+sheet+to+generate+an+invoice+for+time+on+various+projects.++Can+you+help+me+with+step+by+step+instructions+%3F&mtid=SdfbaIKJLZugw8cPouLs4QE&mstk=AUtExfCa_Jd7WCIIaqje_fyYwe1GMaC83Lp54WRc86MDK_qYS319Yp4V4F9SnMvCtZrLaPN_noK_4Z3kgsm6gkUSkv0RRZa5w68ZGQNmTNa2_kHbhar5db_Cnz5gcQIhUOlXRANZww_stkt-Ic50VT5B8jtPF8VzMpaGB595MdO1dLoN6urwaFf7n2yaxqeVAMsunba69G1c7KUqaOzVzpFp00TWKMhqcgqiwh5KDrao0qm8COvSsBp8UZxTy6hl6nH7PdP6N-aauzKLt9mwdhhn_yA_DRpWN-YWpmQ&csuir=1)
- ICS on [CAT9-TimeSheet](https://docs.google.com/spreadsheets/d/13J7sXSwUnMzZElgEAnDN1p5x-nMsJe13yQDOE27rnSc/edit?gid=0#gid=0) doc in cat9do
- Figure out hwpc old db data
  - review old code on [https://hwpc.2cld.net/](https://hwpc.2cld.net/)
  - look for old dev vm ?
  - setup google sheet like old db and get import / export working
  - use n8n to export old hwpc data to google sheets ??
- Cleanup Keep notes ghadmin
- wip for me, steve, candy, brian, kenton
- Setup Steve Testing
- Setup Candy Testing
- [hwpc-bug](https://github.com/grasshorse/hwpc-bug)
- [hwpc-gs](https://github.com/grasshorse/hwpc-gs)
- tbd
# WIP
- Fix main site FooBar (wix shit, dupe and put on ct sites.google.com hawkeyewestpestcontrol
  - cat@hwpc sent contacted google to claim ownership mainly for google maps
  - Need to validate ownership with a call to website listed number
- Convert HWPC Tickets to mobile
  - CustomerDB
  - TicketDB
  - TicketView
  - RoutePrint
- Bare min conversion from old db to google sheets

# Test
- Sheets [HWPC Routes](https://docs.google.com/spreadsheets/d/1XZotISYBmbW1XCl1l35aHwgtgXDwfI_IXkaPK4ER8kU/edit?gid=0#gid=0)
- Maps [HWPC Route Test](https://www.google.com/maps/d/edit?mid=1mfA1dAilxp2wea3IAS_KqlikhIT1s4M&ll=29.208292828150825%2C-92.41699249999999&z=4)
- Sites ct [HWPC Routes](https://sites.google.com/d/1NbvzB_bl3_YaKf51wuDTwRkfWK02mf66/p/1fHVpcTcqRd48am7FHr46LdQECa2Z6obb/edit)
- tbd
  
# Reference
- Accounting Finance - [yt](https://www.youtube.com/@Robuilt/videos)
- [test ai search](https://www.google.com/search?udm=50&aep=46&source=25q2-US-SearchSites-Site-CTA&q=my+bluetooth+mouse+on+windows+10+keeps+failing.++If+I+go+to+bluetooth+connections+and+just+click+the+mouse+it+starts+working.++Any+clue+why+it+drops%3F&mstk=AUtExfCAKg-8oRbA9FPwqQrBqGCH2k-yviw2RELXNBH3V2jWc8mCf2bVf1JlWMOLlMKSLPO0FcYHasbZYBXwJ_Ed2ntgiwrGPvlUnI78ZkQkb_3gUSLDerpEn3vuRVVsh1rFEyOswAy_7hVrBwAUK9-bO7A6r5v0c4ganr0&csuir=1)
- [Code with Curt - google webapp youtube](https://www.youtube.com/@CodeWithCurt/videos)
  - [Invoice Generator](https://www.youtube.com/watch?v=JPcMLmVQdkU)
- [Sheets Ninja - youtube](https://www.youtube.com/@SheetsNinja/videos)
  - [Time Track and Invoice](https://www.youtube.com/watch?v=-MeR_rEHftA)
- [Create Routes With Google Maps Routes API On Your Wix Velo Site - Wix Velo Tutorial](https://www.youtube.com/watch?v=lnx1n1ZM6Bc&list=TLGG_KoWpKkFtt0xMzA3MjAyNQ&t=11s)
- [Google Sheets invoice templates, step by step](https://www.youtube.com/watch?v=Jwy6mVAQiww&t=177s)
- [How to Make an Invoice Tracker in Google Sheets](https://www.youtube.com/watch?v=o0OHdpRFYIc)
- [Import bank statement to google sheets](https://www.google.com/search?q=import+my+bank+statement+to+google+sheets&rlz=1C1CHBF_enUS1075US1091&oq=import+my+bank+statement+to+gogl&gs_lcrp=EgZjaHJvbWUqCQgBECEYChigATIGCAAQRRg5MgkIARAhGAoYoAEyCQgCECEYChigATIJCAMQIRgKGKABMgkIBBAhGAoYoAEyBwgFECEYjwIyBwgGECEYjwLSAQkyMzM3MWowajeoAgCwAgA&sourceid=chrome&ie=UTF-8)
- tbd
