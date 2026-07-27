# 🏡Promotion 8 2026 (B) Day 1 — AI Workflow SOP

## Metadata
- Knowledge ID: KB-WF-P8B-D1
- Source: Respond.io JSON export
- Respond.io workflow ID: `1782878374000027`
- Status in JSON: `stopped`
- Created at raw timestamp: `1782878374000`
- Updated at raw timestamp: `1782989916726`
- Version: v4 / 2026-07 working import

## Purpose
Promotion 8 2026 (B) Day 1 follow-up workflow for customers who have not completed redemption or who need routing to CSO / appointment handling.

## Main Customer-Facing Message
```text
Dear {{1}}! 🌸

As our valued {{2}} customer, you have an *exclusive FREE 1 Session Postpartum Treatment & Body Assessment* waiting for you at Mumsrelle Orchardgateway. 😉

*What you'll enjoy*:🌟
🎁 FREE Body Assessment
🎁 FREE 1 Session of Postpartum Treatment
🎁 Personalised body recovery consultation with our therapist

*Many mums visit us to improve*:
✅ Diastasis recti
✅ Body shape and tummy concerns
✅ Cellulite and stubborn fat
✅ Pelvic floor strength 

Simply reply *"OK"* if you'd like to know more or redeem now.

We look forward to welcoming you! 💕
```

## WhatsApp Template / Media Steps
- Template step: **Promo8 Day 1 Template**
  - Template name: `promo8_2026_day1`
  - Status: `approved`
  - Category: `MARKETING`
  - Language: `en`
  - Variables: `{{$contact.name}}, {{$contact.bu}}`
- Attachment step: **Send SC Booklet** — `PRHB Booklet (with Indiba)_20260212.pdf` (application/pdf)
- Attachment step: **Send SC Video** — `Tummy and Womb Revitalisation.mp4` (video/mp4)
- Attachment step: **Send $279 Trt Photo** — `mumsrelle_promotion_8_cso_05.png` (image/png)

## Question Steps
- **Book SC Appt Qs A** — type `multiple`, timeout `10 minutes`
  - Preview: Would you like to book for an appointment?  Your appointment includes a complimentary full-body assessment with our therapist to understand your body’s specific needs. Based on the assessment results, she will recommend 
  - Options: ['Book Appointment']
- **Book SC Appt Qs B** — type `text`, timeout `10 minutes`
  - Preview: We’re open from 10am to 8pm daily. May I know when you'd like to schedule your trial?  Preferred Date: Preferred Time: EDD / DOB of Your Youngest Child (DD MMM YYYY):  What was your mode of child delivery? - Natural Birt
  - Options: free text
- **Day 1 Question** — type `text`, timeout `10 minutes`
  - Preview: Dear {{$contact.name}}! 🌸  As our valued {{$contact.bu}} customer, you have an exclusive *FREE 1 Session Postpartum Treatment & Body Assessment* waiting for you at Mumsrelle Orchardgateway. 😉  *What you'll enjoy*:🌟 🎁 FRE
  - Options: free text

## Routing Summary
- Customer replies containing `OK` are routed to appointment / CSO / PRHB booklet flow depending on day.
- Invalid replies trigger the Invalid Message workflow.
- Template sending failure adds an internal comment and routes to CSO checking.

## Connected Workflows
- Trigger Client Answered Text Message → workflow `1741234659260229`, step `29e05e`
- Trigger Invalid Message → workflow `1726115624765109`, step `318e0c`
- Trigger Straight to CSO → workflow `1728649862995626`, step `67a0ff`
- Trigger Day 2 → workflow `1782887100445674`, step `None`

## Contact Tags Added
- Tag Promo8_2026 → [4351607]
- Tag Promo8_2026 #2 → [4351607]

## QA Flags / Needs Review
- Wait step 'Wait 4 Hours' label suggests 4 hours but JSON is 10 minutes
- Wait step 'Wait 2 Hours' label suggests 2 hours but JSON is 10 minutes
- Wait step 'Wait 12 Hours' label suggests 12 hours but JSON is 10 minutes
- Wait step 'Wait 5 Hours' label suggests 5 hours but JSON is 10 minutes
- Wait step 'Wait 1 Hour' label suggests 1 hours but JSON is 10 minutes
- Check attachment naming: step labelled `Send SC Booklet` sends `PRHB Booklet (with Indiba)_20260212.pdf`. Confirm whether intentional.

## Related Documents
- Promotion 8 Master Workflow Registry
- Template Registry
- SC FAQ
- PRHB FAQ
