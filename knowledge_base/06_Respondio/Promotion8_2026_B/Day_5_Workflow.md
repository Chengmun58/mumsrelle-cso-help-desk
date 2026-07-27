# 🏡Promotion 8 2026 (B) Day 5

## Metadata

- Respond.io Workflow ID: `1782898357643978`
- Status in uploaded JSON: `stopped`
- Created: 2026-07-01T17:32:37.643000+08:00
- Published: 2026-07-02T14:31:32.425000+08:00
- Updated: 2026-07-02T18:59:23.589000+08:00
- Manual ejection: `True`
- Exit conditions: `{'incomingMessage': False, 'outgoingMessage': False, 'manualAssignment': False}`

## Customer-facing WhatsApp Template(s)

### Send Promotion 8 2026 (B) Day 5
- Template name: `promo8_2026_day5`
- Template status: `approved`
- Header format: `none`

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

## Ask Question Steps

### Day 5 Question
- Question type: `text`
- Options: `[]`
- Timeout: `{'value': 10, 'unit': 'minutes'}`

```text
⏰ *Last Chance to Redeem Your Exclusive Mumsrelle Privileges*!

Hi {{$contact.name}}! 💕

Don't miss your last opportunity to enjoy these exclusive privileges as our valued {{$contact.bu}} customer.

Choose one or both:

🎁 *FREE Body Assessment + 1 Postpartum Treatment Session*

🏠 *Home-Based Pelvic Restoration Trial – $89*

Simply reply *"OK"*, and our team will assist you with your preferred appointment ASAP!

We look forward to welcoming you soon! 🌸
```

## Tags Applied

| Step | Action | Tag IDs |
|---|---:|---|
| Tag Promotion 8 2026 (B) Day 5 | addTag | `[4351975]` |
| Tag Promo8_2026_Trial5 | addTag | `[4351975]` |

## Connected / Triggered Workflows

| Step | Target workflow ID | Target step ID |
|---|---:|---|
| Trigger Invalid Message | `1726115624765109` | `318e0c` |
| Trigger Straight to CSO | `1728649862995626` | `67a0ff` |
| Trigger Close Conversation | `1741334214625544` | `81713f` |
| Trigger Another Workflow #4 | `1728649862995626` | `2800af` |
| Trigger Another Workflow #6 | `1728649862995626` | `2800af` |
| Trigger Another Workflow #8 | `1728649862995626` | `2800af` |
| Trigger Another Workflow #10 | `1728649862995626` | `2800af` |
| Trigger Another Workflow #12 | `1728649862995626` | `2800af` |
| Trigger Another Workflow #14 | `1741451154125944` | `f793db` |
| Trigger Another Workflow #15 | `1728649862995626` | `2800af` |

## Failure / CSO Escalation Comments

### Add Comment #4
```text
Failed to send Promotion 8 2026 (B) Day 5 Template, CSO please check the red "!" for reason. If it's to maintain healthy ecosystem engagement, then need to record & wait for few days later only select the Text Template to resume workflow.
```

## Wait Steps Found in JSON

> Note: Some wait step names say 2 hours / 4 hours / 12 hours, but uploaded JSON values currently show `10 minutes`. Treat this as a configuration item to verify in Respond.io before publishing live.

| Step name | JSON value | Unit |
|---|---:|---|
| Wait 4 Hours | 10 | minutes |
| Wait 2  Hours | 10 | minutes |
| Wait 12 Hours | 10 | minutes |
| Wait 5 Hours | 10 | minutes |
| Wait 1 Hour | 10 | minutes |

## Operational Interpretation

Last-chance message for both privileges. OK routes to CSO/agent workflows; timeout closes conversation.