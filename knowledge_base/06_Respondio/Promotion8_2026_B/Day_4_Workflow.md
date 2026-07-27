# 🏡Promotion 8 2026 (B) Day 4

## Metadata

- Respond.io Workflow ID: `1782898347155769`
- Status in uploaded JSON: `stopped`
- Created: 2026-07-01T17:32:27.155000+08:00
- Published: 2026-07-02T14:31:38.652000+08:00
- Updated: 2026-07-02T18:59:16.935000+08:00
- Manual ejection: `True`
- Exit conditions: `{'incomingMessage': False, 'outgoingMessage': False, 'manualAssignment': False}`

## Customer-facing WhatsApp Template(s)

### Promotion 8 2026 (B) Day 4
- Template name: `promo8_2026_day4`
- Template status: `approved`
- Header format: `none`

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

## Ask Question Steps

### Day 4 Question
- Question type: `text`
- Options: `[]`
- Timeout: `{'value': 10, 'unit': 'minutes'}`

```text
Hi {{$contact.name}}! 👋

*Don’t forget* — your exclusive *Mumsrelle perks* are waiting. 💫

Take a moment to pamper yourself while supporting your recovery — you deserve it. 💕

You may choose either or both:
🎁 *FREE Body Assessment + 1 Session Postpartum Treatment*

*AND/OR*

🏠 *Home-Based Pelvic Restoration Trial – Only $89*

Simply reply *"OK"* to reserve now. We'll be happy to help you arrange your appointment.
```

## Tags Applied

| Step | Action | Tag IDs |
|---|---:|---|
| Tag Promo8_2026_Trial4 | addTag | `[4351950]` |
| Promo8_2026_Trial4 | addTag | `[4351950]` |

## Connected / Triggered Workflows

| Step | Target workflow ID | Target step ID |
|---|---:|---|
| Trigger Invalid Message | `1726115624765109` | `318e0c` |
| Trigger Talk to Agent Message | `1741237063901462` | `1c696e` |
| Trigger Straight to CSO | `1728649862995626` | `2800af` |
| Trigger Day 5 | `1782898357643978` | `None` |
| Trigger Another Workflow #6 | `1728649862995626` | `2800af` |

## Failure / CSO Escalation Comments

### Add Comment #3
```text
Failed to send Promotion 8 2026 (B) Day 4, CSO please check the red "!" for reason. If it's to maintain healthy ecosystem engagement, then need to record & wait for few days later only select the Text Template to resume workflow.
```

## Wait Steps Found in JSON

> Note: Some wait step names say 2 hours / 4 hours / 12 hours, but uploaded JSON values currently show `10 minutes`. Treat this as a configuration item to verify in Respond.io before publishing live.

| Step name | JSON value | Unit |
|---|---:|---|
| Wait 6 Hours | 10 | minutes |
| Wait 2 Hours | 10 | minutes |
| Wait 23 Hours #1 | 10 | minutes |
| Wait 23 Hours #2 | 10 | minutes |
| Wait 17 Hours | 10 | minutes |
| Wait 1 Hour | 10 | minutes |

## Operational Interpretation

Reminder that customer may choose either/both free SC treatment and $89 PRHB trial. OK routes to agent/CSO handling; timeout proceeds to Day 5.