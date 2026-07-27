# 🏡Promotion 8 2026 (B) Day 2 — AI Workflow SOP

## Metadata
- Knowledge ID: KB-WF-P8B-D2
- Source: Respond.io JSON export
- Respond.io workflow ID: `1782887100445674`
- Status in JSON: `stopped`
- Created at raw timestamp: `1782887100445`
- Updated at raw timestamp: `1782989935280`
- Version: v4 / 2026-07 working import

## Purpose
Promotion 8 2026 (B) Day 2 follow-up workflow for customers who have not completed redemption or who need routing to CSO / appointment handling.

## Main Customer-Facing Message
```text
⏰ Your *FREE treatment offer* is ending soon!

Dear {{1}}! 🌸, this is a friendly reminder that your *FREE 1 Session Postpartum Treatment & Body Assessment* offer is almost ending.

💖 Here's a real result from one of our customers after just 1 treatment session.

The *good news* is 🌟:
✔️ You can reserve your entitlement today
✔️ Visit us on a later date that suits your schedule

Simply reply *"OK"* to reserve now, and we'll help arrange everything for you. Limited priority slots are available. ⏰
```

## WhatsApp Template / Media Steps
- Attachment step: **Send SC Client Result Photo** — `SC Client Result.png` (image/png)
- Template step: **Promo8 Day 2 Template**
  - Template name: `promo8_2026_day2`
  - Status: `approved`
  - Category: `MARKETING`
  - Language: `en`
  - Variables: `{{$contact.name}}`

## Question Steps
- **Day 2 Question** — type `text`, timeout `10 minutes`
  - Preview: ⏰ Your *FREE treatment offer* is ending soon!  Dear {{$contact.name}}!🌸, this is a friendly reminder that your *FREE 1 Session Postpartum Treatment & Body Assessment* offer is almost ending.  💖 Here's a real result from 
  - Options: free text
- **Book SC Appt Qs B** — type `text`, timeout `10 minutes`
  - Preview: We’re open from 10am to 8pm daily. May I know when you'd like to schedule your trial?  Preferred Date: Preferred Time: EDD / DOB of Your Youngest Child (DD MMM YYYY):  What was your mode of child delivery? - Natural Birt
  - Options: free text

## Routing Summary
- Customer replies containing `OK` are routed to appointment / CSO / PRHB booklet flow depending on day.
- Invalid replies trigger the Invalid Message workflow.
- Template sending failure adds an internal comment and routes to CSO checking.

## Connected Workflows
- Trigger Client Answered Text Message → workflow `1741234659260229`, step `29e05e`
- Trigger AI Can't Handle → workflow `1726115624765109`, step `2d7269`
- Trigger Invalid Message → workflow `1726115624765109`, step `318e0c`
- Trigger Straight to CSO → workflow `1728649862995626`, step `67a0ff`
- Trigger Talk to Agent Message → workflow `1741237063901462`, step `1c696e`
- Trigger Day 3 → workflow `1782897624494550`, step `None`

## Contact Tags Added
- Tag Promo8 Day 2 #1 → [4351616]
- Tag Promo8 Day 2 #2 → [2806106]

## QA Flags / Needs Review
- Wait step 'Wait 4 Hours' label suggests 4 hours but JSON is 10 minutes
- Wait step 'Wait 2 Hours' label suggests 2 hours but JSON is 10 minutes
- Wait step 'Wait 12 Hours' label suggests 12 hours but JSON is 10 minutes
- Wait step 'Wait 5 Hours' label suggests 5 hours but JSON is 10 minutes
- Wait step 'Wait 1 Hour' label suggests 1 hours but JSON is 10 minutes

## Related Documents
- Promotion 8 Master Workflow Registry
- Template Registry
- SC FAQ
- PRHB FAQ
