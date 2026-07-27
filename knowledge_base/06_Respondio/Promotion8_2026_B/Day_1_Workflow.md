# 🏡Promotion 8 2026 (B) Day 1

## Metadata

- Respond.io Workflow ID: `1782878374000027`
- Status in uploaded JSON: `stopped`
- Created: 2026-07-01T11:59:34+08:00
- Published: 2026-07-02T14:31:23.010000+08:00
- Updated: 2026-07-02T18:58:36.726000+08:00
- Manual ejection: `True`
- Exit conditions: `{'incomingMessage': False, 'outgoingMessage': False, 'manualAssignment': False}`

## Customer-facing WhatsApp Template(s)

### Promo8 Day 1 Template
- Template name: `promo8_2026_day1`
- Template status: `approved`
- Header format: `image`

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

## Ask Question Steps

### Book SC Appt Qs A
- Question type: `multiple`
- Options: `['Book Appointment']`
- Timeout: `{'value': 10, 'unit': 'minutes'}`

```text
Would you like to book for an appointment?

Your appointment includes a complimentary full-body assessment with our therapist to understand your body’s specific needs. Based on the assessment results, she will recommend a suitable treatment tailored for you.😊
```
### Book SC Appt Qs B
- Question type: `text`
- Options: `[]`
- Timeout: `{'unit': 'minutes', 'value': 10}`

```text
We’re open from 10am to 8pm daily. May I know when you'd like to schedule your trial?

Preferred Date:
Preferred Time:
EDD / DOB of Your Youngest Child (DD MMM YYYY):

What was your mode of child delivery?
- Natural Birth
- C-section
- I'm currently pregnant
- I'm not a mother

⌛Duration: 2 Hours 30 Mins
📍Location: #03-06, Orchardgateway
```
### Day 1 Question
- Question type: `text`
- Options: `[]`
- Timeout: `{'unit': 'minutes', 'value': 10}`

```text
Dear {{$contact.name}}! 🌸

As our valued {{$contact.bu}} customer, you have an exclusive *FREE 1 Session Postpartum Treatment & Body Assessment* waiting for you at Mumsrelle Orchardgateway. 😉

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

## Tags Applied

| Step | Action | Tag IDs |
|---|---:|---|
| Tag Promo8_2026 | addTag | `[4351607]` |
| Tag Promo8_2026 #2 | addTag | `[4351607]` |

## Connected / Triggered Workflows

| Step | Target workflow ID | Target step ID |
|---|---:|---|
| Trigger Client Answered Text Message | `1741234659260229` | `29e05e` |
| Trigger Invalid Message | `1726115624765109` | `318e0c` |
| Trigger Straight to CSO | `1728649862995626` | `67a0ff` |
| Trigger Day 2 | `1782887100445674` | `None` |

## Failure / CSO Escalation Comments

### Add Comment #2
```text
Failed to send Promo8 Day 1 Template. CSO please check the red "!" for reason. 

If it's required parameter is missing, then check if the required data in contact fields is completed

If it's either client doesn't have WhatsApp or the number is part of Meta experiment which we can't send WhatsApp template, then call/ email client.
```

## Wait Steps Found in JSON

> Note: Some wait step names say 2 hours / 4 hours / 12 hours, but uploaded JSON values currently show `10 minutes`. Treat this as a configuration item to verify in Respond.io before publishing live.

| Step name | JSON value | Unit |
|---|---:|---|
| Wait 4 Hours | 10 | minutes |
| Wait 2 Hours | 10 | minutes |
| Wait 12 Hours | 10 | minutes |
| Wait 5 Hours | 10 | minutes |
| Wait 1 Hour | 10 | minutes |

## Operational Interpretation

Initial free SC treatment + body assessment invitation. If customer replies OK, the flow sends/uses SC appointment questions. If no response, it proceeds to Day 2.