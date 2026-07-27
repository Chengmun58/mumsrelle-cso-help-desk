# Make.com + Respond.io Automation Blueprint

## Primary Source
Google Drive: `Mumsrelle Automation Blueprint Reference`, created and modified on 2026-06-03.

## Live Scenarios

| Scenario | Name | Platform | Trigger | Status |
|---|---|---|---|---|
| 1 | Final Part 1 A–L — Lead Capture to CSO | Make.com | Scheduled polling | LIVE |
| 2 | Final Part 2 W–Z — Status Initialisation | Make.com | Scheduled polling | LIVE |
| 3 | Final Part AK–AL — Appointment Tracking | Make.com | Gmail Watch | LIVE |
| 4 | Part W–Z Cold Lead — Cold Lead Sync | Make.com | Instant webhook | LIVE |
| 5 | Sheet31 → Respond.io Contact + Lifecycle Sync | Make.com | Scheduled polling | LIVE |
| 6 | KIV — Respond.io Sync | Make.com | Scheduled polling | LIVE |
| 7 | KIV — Follow-Up Logic | Google Apps Script | Time-based trigger | LIVE |

## Scenario 1 — Lead Capture to CSO
Purpose: Detect new leads in `Filter (All Data)` and copy only Timestamp Code Column A into CSO. Columns B–L are formula-driven and must not be touched by Make.com.

Rules:
- Source: Filter (All Data)
- Destination: CSO
- Duplicate check: Timestamp Code
- Batch limit: 200 rows per run

## Scenario 2 — W–Z Status Initialisation
Purpose: Initialise PRHB Status, PRHB Status Date, SC Status, and SC Status Date for new leads.

Columns:
- W = PRHB Status
- X = PRHB Status Date
- Y = SC Status
- Z = SC Status Date

Route logic:
- PRHB source/package → Interested + today date
- SC Main Website → Interested + today date
- Promotion 8 sources such as PEM / PEM Nanny / PNSG / TWSIG / Bliss Helper → Interested + today date
- Bliss Helper Leads Form / Physical Fair → Interested + today date

## Scenario 3 — Appointment Attendance Tracker
Purpose: Monitor `EMAIL_REDACTED` for booking confirmation emails and mark appointment attendance automatically.

Email detection:
- Subject: `[Mumsrelle] Thank You for your submission`
- Unread emails only
- INBOX
- Batch limit: 50 emails per run

Output:
- AK = Attended
- AL = today's date

## Scenario 4 — Cold Lead Status Update
Purpose: When CSO adds an outcome comment in Respond.io, the webhook updates CSO sheet and Respond.io lifecycle.

Comment keywords:
- `Give Up` → W/Y = Give Up, X/Z = today, lifecycle = Cold Lead, close conversation
- `Pass promo` → W/Y = Client Reject, X/Z = today, lifecycle = Cold Lead, close conversation
- `Not interested` → W/Y = Client Reject, X/Z = today, lifecycle = Cold Lead, close conversation

Phone matching rule:
- Strip `+`, spaces, and dashes before matching.

## Scenario 5 — Sheet31 → Respond.io Contact + Lifecycle Sync
Purpose: Central sync engine from Google Sheets to Respond.io.

Sheet31 columns:
- A First Name
- B Last Name
- C Phone Number
- D Email
- F Lifecycle
- H Business Unit (`bu`)
- I premium_signature
- J text_template
- K Respond.io Contact ID write-back
- L CSO Contact ID reference
- M API Response Log

Processing:
1. Watch Sheet31 rows.
2. Create/update Respond.io contact using phone as identifier.
3. Sync name, phone, email, bu, premium_signature, text_template.
4. Set lifecycle from Sheet31 Column F.
5. Write Contact ID to Sheet31 Columns K/L.
6. Log API response to Column M.
7. Open Respond.io conversation.
8. Mark CSO Column AM = `R.io`.

## Scenario 6 & 7 — KIV Follow-Up + Respond.io Automation
Architecture:
- Make.com handles Respond.io lifecycle sync and contact creation/update.
- Google Apps Script handles KIV lead detection, due-date calculation, follow-up actions, and escalation.

KIV data points:
- CSO W/Y = KIV status
- CSO X/Z = KIV status date
- Sheet31 F = lifecycle sent to Respond.io
- Sheet31 K = Respond.io Contact ID used for API follow-up

## Automated CSO Columns
| Column | Field | Automated By |
|---|---|---|
| A | Timestamp Code | Scenario 1 |
| B–L | Lead data | Formula-driven |
| W | PRHB Status | Scenarios 2, 4, 7 |
| X | PRHB Status Date | Scenarios 2, 4, 7 |
| Y | SC Status | Scenarios 2, 4, 7 |
| Z | SC Status Date | Scenarios 2, 4, 7 |
| AK | Appointment Status | Scenario 3 |
| AL | Attendance Date | Scenario 3 |
| AM | Respond.io Sync Flag | Scenario 5 |

## Preservation Rule
Keep all six Make workflows active. Do not delete older successful workflows because they serve as production range logic or rollback references. Use `Sheet31 -> Respond.io Contact + Lifecycle Sync - Final` as the main production reference and keep the latest copy as backup or extension version.
