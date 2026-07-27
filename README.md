# Mumsrelle CSO AI Help Desk

Single internal workspace for the Mumsrelle CSO team to prepare safe customer replies, review live cases, use approved templates, consult SOP references, and monitor daily KPI responsibilities.

## Current Status

Approved Answers now load from a protected Supabase backend. The public build has read-only access to rows where `Status = Approved` and `Active = true`; it cannot add, edit, or delete backend data.

Live Cases remain anonymised workflow examples. The public build does not connect to live Respond.io, Aoikumo, or Sequoia APIs.

The merged app uses the existing GitHub Pages site as the main entry point. The GitHub version uses anonymised sample customer data only.

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | Main standalone app. Open this file in a browser or publish it through GitHub Pages. |
| `support.js` | Runtime support script required by the app. |

Internal SOPs, AI instructions, source-priority rules, and detailed knowledge-base files are intentionally excluded from this public repository.

## Main Sections

- Approved Answer Search backed by an editable Supabase table, with a verified 15-answer static fallback
- Anonymised Live Cases workflow examples
- Approved Templates that copy the full customer reply
- Clickable SOP & Knowledge Base operating guides
- Daily KPI view for CSO responsibilities
- Risk and escalation classification
- Human approval before any external sending
- Admin-only Google Sheets and Respond.io integration setup
- Device History persisted in the current browser for sample case actions
- Shared backend Change History for every Approved Answer insert, update, and delete

## Editable Backend

Use the Supabase Table Editor for:

- `cso_helpdesk_approved_answers`: add, edit, approve, activate, or deactivate customer answers.
- `cso_helpdesk_change_history`: review the old value, new value, operation, timestamp, and actor for every change.

Publishing rule: only rows with `status = Approved` and `active = true` are returned to the website. After editing, use **Refresh Answers** in the Help Desk or reload the page.

Security rule: the publishable browser key has `SELECT` access only to active Approved answers. Anonymous users have no insert, update, delete, or Change History access.

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

- Replace Live Cases sample data with an authenticated Google Sheets or backend integration only after approval rules and staff access are finalised.
- Keep Respond.io sending manual unless management approves a controlled automation flow.
- Keep internal SOPs, source registries, medical-safety guidance, and workflow JSON in a private repository or internal document store.
