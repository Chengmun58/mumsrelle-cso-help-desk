# Mumsrelle CSO AI Help Desk

Interactive prototype for the Mumsrelle CSO team to review customer-service cases, draft safe replies, flag escalation cases, and prepare Respond.io / Google Sheets integration requirements.

## Current Status

This is a local prototype. It does not connect to live Respond.io, Google Sheets, Aoikumo, or Sequoia APIs yet.

The app is intended for workflow review, team alignment, and future implementation planning.

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | Main standalone app. Open this file in a browser or publish it through GitHub Pages. |
| `support.js` | Runtime support script required by the app. |
| `mumsrelle-cso-help-desk.dc.html` | Source-style DC export kept for reference. |
| `knowledge_base/` | Mumsrelle AI knowledge base, SOPs, promotion references, templates, workflow notes, and source registry. |

## Main Workflow Covered

- Case Inbox for customer enquiries
- Risk and escalation classification
- Draft customer replies
- Human approval before any external sending
- Google Sheets field mapping design
- Respond.io event mapping design
- Knowledge-source hierarchy and source registry

## Safety Rules

- Medical, refund, complaint, safety, unclear eligibility, or missing-information cases should be escalated.
- The prototype must not send messages automatically.
- Approved drafts should still be reviewed by an authorised CSO, Centre Manager, or Management depending on risk level.

## Suggested GitHub Pages Setup

1. Push this folder to a GitHub repository.
2. In GitHub, go to `Settings > Pages`.
3. Select the default branch and root folder.
4. Open the generated GitHub Pages URL.

## Notes For Future Development

- Replace local mock data with Google Sheets or backend API reads only after approval rules are finalised.
- Keep Respond.io sending manual unless management approves a controlled automation flow.
- Maintain `knowledge_base/14_Source_Registry/` as the source-of-truth audit trail for imported SOPs and workflow JSON.
