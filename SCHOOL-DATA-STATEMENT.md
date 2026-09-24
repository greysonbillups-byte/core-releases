# CORE — Data Privacy and Security Statement for Schools and Institutions

**Version 1.0 — 24 September 2026**
**Vendor:** Greyson Billups (sole proprietor), Alabama, USA · core.esportsbroadcast@gmail.com

This statement is for IT, privacy, and procurement reviewers evaluating CORE, a Windows desktop application for producing esports broadcasts with OBS Studio.

---

## Summary

| Question | Answer |
|---|---|
| Does CORE collect student personal information? | **No.** |
| Where is data entered into CORE stored? | Only on the institution's own computers, in the Windows user profile. |
| Does the vendor operate servers that receive institutional data? | **No.** |
| Does the vendor have access to rosters, names, photos, or results? | **No.** |
| Does CORE require student accounts or logins? | **No.** There are no user accounts. |
| Analytics, telemetry, advertising, or tracking? | **None.** |
| Does the vendor sell or share personal information? | **No.** |

---

## Data stored locally (never transmitted)

Teams, schools, player names and gamertags, rosters, photos and logos, brackets, schedules, match results, overlay files, settings, hotkeys, and saved replays. The institution controls this data entirely. Uninstalling CORE or deleting its profile folder removes it.

## Data transmitted, and to whom

| Purpose | Recipient | Data sent | When |
|---|---|---|---|
| Licence verification (paid tiers only) | Lemon Squeezy (licensing and payment provider) | Licence key; computer label (Windows hostname + OS); activation ID; IP address | Activation, periodic check, releasing a seat |
| Update check | GitHub (download host) | Standard web request only (IP address); no identifiers | App start, then about every 6 hours |

No student information is included in either request.

## Purchase information

Purchases are processed by Lemon Squeezy as merchant of record. The vendor receives the purchaser's name, email address, order details, and licence activation records. The vendor does not receive payment card details. For an institution, this is typically staff contact information, not student information.

---

## Regulatory position

- **FERPA:** CORE does not receive, store, or have access to education records. The vendor is not a recipient of student personally identifiable information.
- **COPPA:** CORE does not collect personal information from any user, including children under 13.
- **State student privacy laws:** Because no student data is collected or transmitted, the vendor does not use student data for advertising, profiling, or any other purpose.
- **Broadcast content:** Displaying student names or images in a broadcast is controlled by the institution. The institution is responsible for applying its own directory-information and media-release policies.

The vendor will review and, where appropriate, sign an institutional or state-standard data privacy agreement on request.

---

## Security notes

- **Local services:** CORE runs local HTTP and WebSocket servers to feed overlays to OBS. These bind to the loopback interface (127.0.0.1) only, on ports 3030 and 3031, and are not reachable from other machines on the network. There is no setting that exposes them.
- **Licence key storage:** The key is encrypted with Windows credential storage (DPAPI, via the OS keychain API).
- **Transport:** Licence and update traffic uses HTTPS.
- **Code signing:** CORE is **not yet code-signed**. Windows SmartScreen will show a publisher warning on first run, and the publisher will display as unknown. Code signing through Azure Trusted Signing is being put in place. If your institution requires a signed installer before deployment, contact the vendor before purchasing.
- **Updates:** Updates are downloaded in the background and installed when the app is closed, never during a live broadcast.
- **Accounts:** CORE has no user accounts, no sign-in, and no password to manage or reset.

## Accessibility

A VPAT is not currently available. CORE is an operator-facing production tool used by broadcast staff rather than a student-facing system. If your institution requires an accessibility review as part of procurement, contact the vendor to discuss what is needed.

## Contact

Questions, data privacy agreements, or a W-9: **core.esportsbroadcast@gmail.com**
