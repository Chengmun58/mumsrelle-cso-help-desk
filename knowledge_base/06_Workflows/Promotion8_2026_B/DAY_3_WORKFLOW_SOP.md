# 🏡Promotion 8 2026 (B) Day 3 — AI Workflow SOP

## Metadata
- Knowledge ID: KB-WF-P8B-D3
- Source: Respond.io JSON export
- Respond.io workflow ID: `1782897624494550`
- Status in JSON: `stopped`
- Created at raw timestamp: `1782897624494`
- Updated at raw timestamp: `1782989943480`
- Version: v4 / 2026-07 working import

## Purpose
Promotion 8 2026 (B) Day 3 follow-up workflow for customers who have not completed redemption or who need routing to CSO / appointment handling.

## Main Customer-Facing Message
```text
Dear {{1}} , 🌸

We noticed you haven't redeemed your *complimentary Postpartum Treatment & Body Assessment* yet. 

If visiting the centre isn't convenient, we have another exclusive privilege for our valued {{2}} customers.

🏠 *Home-Based Pelvic Restoration Trial — Only $89*

✨ Enjoy professional postpartum treatment in the comfort of *your own home*.

✅ Supports postpartum body recovery
✅ Strengthens and restores the pelvic floor
✅ No travelling required – we'll come to you!

Reply *"OK"* if you'd like to find out more or reserve your session.
```

## WhatsApp Template / Media Steps
- Attachment step: **Send PRHB Booklet** — `Mumsrelle Booklet - Home-based Pelvic.pdf` (application/pdf)
- Template step: **Promo8 Day 3 Template**
  - Template name: `promo8_2026_day3`
  - Status: `approved`
  - Category: `MARKETING`
  - Language: `en`
  - Variables: `{{$contact.name}}, {{$contact.bu}}`
- Attachment step: **Send PRHB Introduction Photo** — `Mumsrelle Sleekflow Image-03.png` (image/png)

## Question Steps
- **Day 3 Question** — type `text`, timeout `10 minutes`
  - Preview: Dear {{$contact.name}}, 🌸  We noticed you haven't redeemed your *complimentary Postpartum Treatment & Body Assessment* yet.   If visiting the centre isn't convenient, we have another exclusive privilege for our valued {{
  - Options: free text
- **Invite to Centre** — type `multiple`, timeout `12 hours`
  - Preview: The trial will take place at our centre in Orchardgateway and includes a free full-body assessment so our therapist can better understand your body’s needs. The trial is only $89, with no additional charges. 😊  After you
  - Options: ['Book Appointment', "I'm not Interested"]
- **Book PRHB Appt Qs** — type `text`, timeout `12 hours`
  - Preview: We’re open from 10am to 8pm daily. May I know when you'd like to schedule your trial?  Preferred Date: Preferred Time: Name: Email: EDD / DOB of Your Youngest Child (DD MMM YYYY):  What was your mode of child delivery? -
  - Options: free text

## Routing Summary
- Customer replies containing `OK` are routed to appointment / CSO / PRHB booklet flow depending on day.
- Invalid replies trigger the Invalid Message workflow.
- Template sending failure adds an internal comment and routes to CSO checking.

## Connected Workflows
- Trigger AI Can't Handle → workflow `1726115624765109`, step `2d7269`
- Trigger Invalid Message → workflow `1726115624765109`, step `318e0c`
- Trigger Straight to CSO → workflow `1728649862995626`, step `2800af`
- Trigger Client Answered Text → workflow `1741234659260229`, step `29e05e`
- Trigger Talk to Agent Message → workflow `1741237063901462`, step `1c696e`
- Trigger Not Interested Message → workflow `1741331502817611`, step `1f896c`
- Trigger Day 4 → workflow `1782898347155769`, step `None`
- Trigger Another Workflow #8 → workflow `1782898347155769`, step `None`
- Trigger Another Workflow #9 → workflow `1741331502817611`, step `1f896c`

## Contact Tags Added
- Tag Promo8_2026_Day3 → [4351928]
- Promo8_2026_Day3 → [4351928]

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
