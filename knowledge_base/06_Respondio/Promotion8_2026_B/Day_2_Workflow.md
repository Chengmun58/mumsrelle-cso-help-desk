# 🏡Promotion 8 2026 (B) Day 2

## Metadata

- Respond.io Workflow ID: `1782887100445674`
- Status in uploaded JSON: `stopped`
- Created: 2026-07-01T14:25:00.445000+08:00
- Published: 2026-07-02T14:31:35.351000+08:00
- Updated: 2026-07-02T18:58:55.280000+08:00
- Manual ejection: `True`
- Exit conditions: `{'incomingMessage': False, 'outgoingMessage': False, 'manualAssignment': False}`

## Customer-facing WhatsApp Template(s)

### Promo8 Day 2 Template
- Template name: `promo8_2026_day2`
- Template status: `approved`
- Header format: `image`

```text
⏰ Your *FREE treatment offer* is ending soon!

Dear {{1}}! 🌸, this is a friendly reminder that your *FREE 1 Session Postpartum Treatment & Body Assessment* offer is almost ending.

💖 Here's a real result from one of our customers after just 1 treatment session.

The *good news* is 🌟:
✔️ You can reserve your entitlement today
✔️ Visit us on a later date that suits your schedule

Simply reply *"OK"* to reserve now, and we'll help arrange everything for you. Limited priority slots are available. ⏰
```

## Ask Question Steps

### Day 2 Question
- Question type: `text`
- Options: `[]`
- Timeout: `{'value': 10, 'unit': 'minutes'}`

```text
⏰ Your *FREE treatment offer* is ending soon!

Dear {{$contact.name}}!🌸, this is a friendly reminder that your *FREE 1 Session Postpartum Treatment & Body Assessment* offer is almost ending.

💖 Here's a real result from one of our customers after just 1 treatment session.

The *good news* is 🌟:
✔️ You can reserve your entitlement today
✔️ Visit us on a later date that suits your schedule

Simply reply *"OK"* to reserve now, and we'll help arrange everything for you. Limited priority slots are available. ⏰
```
### Book SC Appt Qs B
- Question type: `text`
- Options: `[]`
- Timeout: `{'value': 10, 'unit': 'minutes'}`

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

## Tags Applied

| Step | Action | Tag IDs |
|---|---:|---|
| Tag Promo8 Day 2 #1 | addTag | `[4351616]` |
| Tag Promo8 Day 2 #2 | addTag | `[2806106]` |

## Connected / Triggered Workflows

| Step | Target workflow ID | Target step ID |
|---|---:|---|
| Trigger Client Answered Text Message | `1741234659260229` | `29e05e` |
| Trigger AI Can't Handle | `1726115624765109` | `2d7269` |
| Trigger Invalid Message | `1726115624765109` | `318e0c` |
| Trigger Straight to CSO | `1728649862995626` | `67a0ff` |
| Trigger Talk to Agent Message | `1741237063901462` | `1c696e` |
| Trigger Day 3 | `1782897624494550` | `None` |

## Failure / CSO Escalation Comments

### Add Comment #3
```text
Failed to send Pomo8 Day 2 Template, CSO please check the red "!" for reason. If it's to maintain healthy ecosystem engagement, then need to record & wait for few days later only select the Text Template to resume workflow
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

Urgency/reminder using SC client result proof. If customer replies OK, ask for SC appointment details. If no response, proceeds to Day 3.