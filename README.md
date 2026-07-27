# Mumsrelle CSO AI Help Desk

Single internal workspace for the Mumsrelle CSO team to prepare safe customer replies, review live cases, use approved templates, consult SOP references, and monitor daily KPI responsibilities.

## Current Status

This is a local prototype. It does not connect to live Respond.io, Google Sheets, Aoikumo, or Sequoia APIs yet.

The merged app uses the existing GitHub Pages site as the main entry point. The GitHub version uses anonymised sample customer data only.

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | Main standalone app. Open this file in a browser or publish it through GitHub Pages. |
| `support.js` | Runtime support script required by the app. |

Internal SOPs, AI instructions, source-priority rules, and detailed knowledge-base files are intentionally excluded from this public repository.

## Main Sections

- Approved Answer Search that returns only reviewed Q&A entries
- Live Cases for customer enquiries
- Approved Templates with customer-facing campaign names removed
- SOP & Knowledge Base directory
- Daily KPI view for CSO responsibilities
- Risk and escalation classification
- Human approval before any external sending
- Admin-only Google Sheets and Respond.io integration setup

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
- Keep internal SOPs, source registries, medical-safety guidance, and workflow JSON in a private repository or internal document store.
