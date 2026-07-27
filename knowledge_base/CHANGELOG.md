# Changelog

## v4 — 2026-07-07
- Added Master Index.
- Added Workflow Registry.
- Added Template Registry.
- Added Decisions Register.
- Added Deprecated Register.
- Imported latest user-uploaded Respond.io JSON files for Promotion 8 2026 (B) Day 1–Day 5.
- Generated AI-readable SOP files for each Day 1–Day 5 workflow.
- Added QA flags for stopped workflow status, OK matching, wait-duration mismatch, and Day 1 booklet naming issue.

## v3 — 2026-07-07

### Added
- Added latest uploaded Respond.io JSON workflows:
  - Promotion 8 2026 (B) Day 1
  - Promotion 8 2026 (B) Day 2
  - Promotion 8 2026 (B) Day 3
  - Promotion 8 2026 (B) Day 4
  - Promotion 8 2026 (B) Day 5
- Added AI-readable Markdown SOP for each Day 1–Day 5 workflow.
- Added master reference under `06_Respondio/Promotion8_2026_B/README.md`.
- Stored raw JSON exports under `14_Source_Registry/raw_respondio_workflows_promo8_2026_b/`.

### Verification Notes
- Uploaded workflows show `status: stopped` in JSON.
- Wait step display names and JSON values appear inconsistent in several places. JSON shows 10-minute values while step names mention longer waits. Verify directly in Respond.io before setting live.
- OK routing conditions should be normalized to avoid missing replies because several conditions use `OK ` with a trailing space.

# CHANGELOG

## 2026-07-07
- Initial Mumsrelle AI Knowledge Base created.
- Source included: uploaded `Mumsrelle CSE SOP.pdf`.
- Source included: Notion `SC FAQ`, active, last reviewed 2026-07-06.
- Added base folders for SOP, FAQ, Promotions, Respond.io, Templates, Aoikumo, Sequoia, Internal Policies, Reports, Troubleshooting, and Meeting Notes.

## 2026-07-07 — v2 Google Drive + Respond.io workflow sync
- Added Google Drive automation blueprint source: `Mumsrelle Automation Blueprint Reference`, updated 2026-06-03.
- Added Make.com workflow preservation source: `Make_Automation_Workflow_Preservation_Summary_2026-06-03`.
- Added CSE Schedule working file reference for SC confirmation/reminder daily tasks.
- Added Respond.io latest five workflow reference for `🏡 Promotion 8 2026 (B) Day 1–Day 5`.
- Added source priority and conflict-resolution rule: latest working file / active workflow overrides older PDF or chat notes.

## Rules
- Add every future change here before updating SOP/FAQ files.
- If an older SOP conflicts with a newer changelog entry, follow the changelog.
