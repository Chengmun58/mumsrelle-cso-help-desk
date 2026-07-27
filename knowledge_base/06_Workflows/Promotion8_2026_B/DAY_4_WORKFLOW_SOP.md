# 🏡Promotion 8 2026 (B) Day 4 — AI Workflow SOP

## Metadata
- Knowledge ID: KB-WF-P8B-D4
- Source: Respond.io JSON export
- Respond.io workflow ID: `1782898347155769`
- Status in JSON: `stopped`
- Created at raw timestamp: `1782898347155`
- Updated at raw timestamp: `1782989956935`
- Version: v4 / 2026-07 working import

## Purpose
Promotion 8 2026 (B) Day 4 follow-up workflow for customers who have not completed redemption or who need routing to CSO / appointment handling.

## Main Customer-Facing Message
```text
Hi {{1}} ! 👋

*Don’t forget* — your exclusive *Mumsrelle perks* are waiting. 💫

Take a moment to pamper yourself while supporting your recovery — you deserve it. 💕

You may choose either or both:
🎁 *FREE Body Assessment + 1 Session Postpartum Treatment*

_AND/OR_

🏠 *Home-Based Pelvic Restoration Trial – Only $89*

Simply reply *"OK"* to reserve now. We'll be happy to help you arrange your appointment.
```

## WhatsApp Template / Media Steps
- Template step: **Promotion 8 2026 (B) Day 4**
  - Template name: `promo8_2026_day4`
  - Status: `approved`
  - Category: `MARKETING`
  - Language: `en`
  - Variables: `{{$contact.name}}`

## Question Steps
- **Day 4 Question** — type `text`, timeout `10 minutes`
  - Preview: Hi {{$contact.name}}! 👋  *Don’t forget* — your exclusive *Mumsrelle perks* are waiting. 💫  Take a moment to pamper yourself while supporting your recovery — you deserve it. 💕  You may choose either or both: 🎁 *FREE Body 
  - Options: free text

## Routing Summary
- Customer replies containing `OK` are routed to appointment / CSO / PRHB booklet flow depending on day.
- Invalid replies trigger the Invalid Message workflow.
- Template sending failure adds an internal comment and routes to CSO checking.

## Connected Workflows
- Trigger Invalid Message → workflow `1726115624765109`, step `318e0c`
- Trigger Talk to Agent Message → workflow `1741237063901462`, step `1c696e`
- Trigger Straight to CSO → workflow `1728649862995626`, step `2800af`
- Trigger Day 5 → workflow `1782898357643978`, step `None`
- Trigger Another Workflow #6 → workflow `1728649862995626`, step `2800af`

## Contact Tags Added
- Tag Promo8_2026_Trial4 → [4351950]
- Promo8_2026_Trial4 → [4351950]

## QA Flags / Needs Review
- Wait step 'Wait 6 Hours' label suggests 6 hours but JSON is 10 minutes
- Wait step 'Wait 2 Hours' label suggests 2 hours but JSON is 10 minutes
- Wait step 'Wait 23 Hours #1' label suggests 23 hours but JSON is 10 minutes
- Wait step 'Wait 23 Hours #2' label suggests 23 hours but JSON is 10 minutes
- Wait step 'Wait 17 Hours' label suggests 17 hours but JSON is 10 minutes
- Wait step 'Wait 1 Hour' label suggests 1 hours but JSON is 10 minutes

## Related Documents
- Promotion 8 Master Workflow Registry
- Template Registry
- SC FAQ
- PRHB FAQ
