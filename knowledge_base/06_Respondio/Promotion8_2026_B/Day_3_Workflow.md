# 🏡Promotion 8 2026 (B) Day 3

## Metadata

- Respond.io Workflow ID: `1782897624494550`
- Status in uploaded JSON: `stopped`
- Created: 2026-07-01T17:20:24.494000+08:00
- Published: 2026-07-02T14:31:37.145000+08:00
- Updated: 2026-07-02T18:59:03.480000+08:00
- Manual ejection: `True`
- Exit conditions: `{'incomingMessage': False, 'outgoingMessage': False, 'manualAssignment': False}`

## Customer-facing WhatsApp Template(s)

### Promo8 Day 3 Template
- Template name: `promo8_2026_day3`
- Template status: `approved`
- Header format: `image`

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

## Ask Question Steps

### Day 3 Question
- Question type: `text`
- Options: `[]`
- Timeout: `{'value': 10, 'unit': 'minutes'}`

```text
Dear {{$contact.name}}, 🌸

We noticed you haven't redeemed your *complimentary Postpartum Treatment & Body Assessment* yet. 

If visiting the centre isn't convenient, we have another exclusive privilege for our valued {{$contact.bu}} customers.

🏠 *Home-Based Pelvic Restoration Trial — Only $89*

✨ Enjoy professional postpartum treatment in the comfort of *your own home*.

✅ Supports postpartum body recovery
✅ Strengthens and restores the pelvic floor
✅ No travelling required – we'll come to you!

Reply *"OK"* if you'd like to find out more or reserve your session.
```
### Invite to Centre
- Question type: `multiple`
- Options: `['Book Appointment', "I'm not Interested"]`
- Timeout: `{'value': 12, 'unit': 'hours'}`

```text
The trial will take place at our centre in Orchardgateway and includes a free full-body assessment so our therapist can better understand your body’s needs. The trial is only $89, with no additional charges. 😊

After your trial, you can choose to continue the service either at your home or at our centre—whichever is more convenient for you.
```
### Book PRHB Appt Qs
- Question type: `text`
- Options: `[]`
- Timeout: `{'unit': 'hours', 'value': 12}`

```text
We’re open from 10am to 8pm daily. May I know when you'd like to schedule your trial?

Preferred Date:
Preferred Time:
Name:
Email:
EDD / DOB of Your Youngest Child (DD MMM YYYY):

What was your mode of child delivery?
- Natural Birth
- C-section
- I'm currently pregnant
- I'm not a mother

⌛Duration: 1 Hour 30 Mins
📍Location: #03-06, Orchardgateway
```

## Tags Applied

| Step | Action | Tag IDs |
|---|---:|---|
| Tag Promo8_2026_Day3 | addTag | `[4351928]` |
| Promo8_2026_Day3 | addTag | `[4351928]` |

## Connected / Triggered Workflows

| Step | Target workflow ID | Target step ID |
|---|---:|---|
| Trigger AI Can't Handle | `1726115624765109` | `2d7269` |
| Trigger Invalid Message | `1726115624765109` | `318e0c` |
| Trigger Straight to CSO | `1728649862995626` | `2800af` |
| Trigger Client Answered Text | `1741234659260229` | `29e05e` |
| Trigger Talk to Agent Message | `1741237063901462` | `1c696e` |
| Trigger Not Interested Message | `1741331502817611` | `1f896c` |
| Trigger Day 4 | `1782898347155769` | `None` |
| Trigger Another Workflow #8 | `1782898347155769` | `None` |
| Trigger Another Workflow #9 | `1741331502817611` | `1f896c` |

## Failure / CSO Escalation Comments

### Add Comment #8
```text
Failed to send Promo8_2026_Day3 Template, CSO please check the red "!" for reason. If it's to maintain healthy ecosystem engagement, then need to record & wait for few days later only select the Text Template to resume workflow.
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

Switches angle to Home-Based Pelvic Restoration Trial at $89 for customers who have not redeemed the centre freebie. If customer replies OK, sends PRHB booklet and asks whether to book.