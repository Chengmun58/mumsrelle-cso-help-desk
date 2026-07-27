# Promotion 8 2026 (B) — Respond.io Workflow Master Reference

This document summarizes the uploaded latest Respond.io JSON workflows for Promotion 8 2026 (B), Day 1 to Day 5.

## Workflow Metadata

| Day | Workflow name | Workflow ID | Status | Created | Published | Updated | Step count |
|---|---|---:|---|---|---|---|---:|
| Day 1 | 🏡Promotion 8 2026 (B) Day 1 | `1782878374000027` | stopped | 2026-07-01T11:59:34+08:00 | 2026-07-02T14:31:23.010000+08:00 | 2026-07-02T18:58:36.726000+08:00 | 70 |
| Day 2 | 🏡Promotion 8 2026 (B) Day 2 | `1782887100445674` | stopped | 2026-07-01T14:25:00.445000+08:00 | 2026-07-02T14:31:35.351000+08:00 | 2026-07-02T18:58:55.280000+08:00 | 65 |
| Day 3 | 🏡Promotion 8 2026 (B) Day 3 | `1782897624494550` | stopped | 2026-07-01T17:20:24.494000+08:00 | 2026-07-02T14:31:37.145000+08:00 | 2026-07-02T18:59:03.480000+08:00 | 78 |
| Day 4 | 🏡Promotion 8 2026 (B) Day 4 | `1782898347155769` | stopped | 2026-07-01T17:32:27.155000+08:00 | 2026-07-02T14:31:38.652000+08:00 | 2026-07-02T18:59:16.935000+08:00 | 67 |
| Day 5 | 🏡Promotion 8 2026 (B) Day 5 | `1782898357643978` | stopped | 2026-07-01T17:32:37.643000+08:00 | 2026-07-02T14:31:32.425000+08:00 | 2026-07-02T18:59:23.589000+08:00 | 60 |

## Current Day-by-Day Logic

| Day | Main message angle | Desired customer reply | Main next action |
|---|---|---|---|
| Day 1 | Free 1 Session Postpartum Treatment + Body Assessment for valued BU customer | `OK` | Send/ask SC appointment questions; invalid replies go to invalid handling; timeout triggers Day 2 |
| Day 2 | Reminder + real result proof + reserve entitlement today, visit later | `OK` | Ask SC appointment details; timeout triggers Day 3 |
| Day 3 | Alternative offer: Home-Based Pelvic Restoration Trial at $89 | `OK` / `Book Appointment` | Send PRHB booklet, invite to centre, then ask PRHB appointment questions; not interested route exists |
| Day 4 | Reminder that customer can choose either/both SC freebie and PRHB $89 trial | `OK` | Trigger talk-to-agent / straight-to-CSO handling; timeout triggers Day 5 |
| Day 5 | Last chance to redeem exclusive Mumsrelle privileges | `OK` | Trigger CSO/agent handling; timeout closes conversation |

## Operational Warnings

- All five uploaded workflows have status `stopped` in the JSON. Confirm in Respond.io before relying on them as active production workflows.
- Several wait step names say 2 hours, 4 hours, 12 hours, etc., but JSON values show `10 minutes`. This may be testing configuration or export inconsistency. Verify before publishing.
- The OK matching condition often checks for `OK ` with a trailing space or `contains OK`. To avoid missed routing, Respond.io condition should ideally accept `OK`, `Ok`, `ok`, and `OK `.
- Day 1 has a step named `Send SC Booklet` but the attachment filename is `PRHB Booklet (with Indiba)_20260212.pdf`; verify whether this is intentional.
- Day 4 has one `Reply Beyond Selection` condition that includes `WHAT`; verify if this is intended.

## Files Included

- `Day_1_Workflow.md`
- `Day_2_Workflow.md`
- `Day_3_Workflow.md`
- `Day_4_Workflow.md`
- `Day_5_Workflow.md`
- Raw uploaded JSON files are stored under `14_Source_Registry/raw_respondio_workflows_promo8_2026_b/`.
