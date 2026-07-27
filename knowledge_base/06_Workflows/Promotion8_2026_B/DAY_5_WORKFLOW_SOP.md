# 🏡Promotion 8 2026 (B) Day 5 — AI Workflow SOP

## Metadata
- Knowledge ID: KB-WF-P8B-D5
- Source: Respond.io JSON export
- Respond.io workflow ID: `1782898357643978`
- Status in JSON: `stopped`
- Created at raw timestamp: `1782898357643`
- Updated at raw timestamp: `1782989963589`
- Version: v4 / 2026-07 working import

## Purpose
Promotion 8 2026 (B) Day 5 follow-up workflow for customers who have not completed redemption or who need routing to CSO / appointment handling.

## Main Customer-Facing Message
```text
⏰ *Last Chance to Redeem Your Exclusive Mumsrelle Privileges!*

Hi {{1}} ! 💕

Don't miss your last opportunity to enjoy these *exclusive privileges* as our valued {{2}} customer.

Choose one or both:

🎁 *FREE Body Assessment + 1 Postpartum Treatment Session*

🏠 *Home-Based Pelvic Restoration Trial – $89*

Simply reply *"OK"*, and our team will assist you with your preferred appointment ASAP!

We look forward to welcoming you soon! 🌸
```

## WhatsApp Template / Media Steps
- Template step: **Send Promotion 8 2026 (B) Day 5**
  - Template name: `promo8_2026_day5`
  - Status: `approved`
  - Category: `MARKETING`
  - Language: `en`
  - Variables: `{{$contact.name}}, {{$contact.bu}}`

## Question Steps
- **Day 5 Question** — type `text`, timeout `10 minutes`
  - Preview: ⏰ *Last Chance to Redeem Your Exclusive Mumsrelle Privileges*!  Hi {{$contact.name}}! 💕  Don't miss your last opportunity to enjoy these exclusive privileges as our valued {{$contact.bu}} customer.  Choose one or both:  
  - Options: free text

## Routing Summary
- Customer replies containing `OK` are routed to appointment / CSO / PRHB booklet flow depending on day.
- Invalid replies trigger the Invalid Message workflow.
- Template sending failure adds an internal comment and routes to CSO checking.

## Connected Workflows
- Trigger Invalid Message → workflow `1726115624765109`, step `318e0c`
- Trigger Straight to CSO → workflow `1728649862995626`, step `67a0ff`
- Trigger Close Conversation → workflow `1741334214625544`, step `81713f`
- Trigger Another Workflow #4 → workflow `1728649862995626`, step `2800af`
- Trigger Another Workflow #6 → workflow `1728649862995626`, step `2800af`
- Trigger Another Workflow #8 → workflow `1728649862995626`, step `2800af`
- Trigger Another Workflow #10 → workflow `1728649862995626`, step `2800af`
- Trigger Another Workflow #12 → workflow `1728649862995626`, step `2800af`
- Trigger Another Workflow #14 → workflow `1741451154125944`, step `f793db`
- Trigger Another Workflow #15 → workflow `1728649862995626`, step `2800af`

## Contact Tags Added
- Tag Promotion 8 2026 (B) Day 5 → [4351975]
- Tag Promo8_2026_Trial5 → [4351975]

## QA Flags / Needs Review
- Wait step 'Wait 4 Hours' label suggests 4 hours but JSON is 10 minutes
- Wait step 'Wait 2  Hours' label suggests 2 hours but JSON is 10 minutes
- Wait step 'Wait 12 Hours' label suggests 12 hours but JSON is 10 minutes
- Wait step 'Wait 5 Hours' label suggests 5 hours but JSON is 10 minutes
- Wait step 'Wait 1 Hour' label suggests 1 hours but JSON is 10 minutes

## Related Documents
- Promotion 8 Master Workflow Registry
- Template Registry
- SC FAQ
- PRHB FAQ
