# Cold Email Marketing Agent Support Files

## Purpose

This file is the support document index for the Accord Tech Solutions cold email marketing agent.

Use this file to understand which support `.md` file should be used for each part of the campaign process.

The main SOP is:

```text
SOP.md
```

The master workflow file is:

```text
Master.md
```

These support files give the agent more detailed rules for infrastructure, verification, sequence QA, Instantly setup, monitoring, reply handling, notifications, performance tracking, lead collection, and segmentation.

The 10 detailed support files are organized inside:

```text
Support/
```

This keeps the root folder clean while `Support.md` works like a master support index.

---

## 01. Support File Usage Order

Use the support files in this order when building, auditing, or operating the email marketing agent:

1. [Email Infrastructure](Support/Email-Infrastructure.md)
2. [Verification and Suppression](Support/Verification-and-Suppression.md)
3. [Email Sequence QA](Support/Email-Sequence-QA.md)
4. [Instantly Setup](Support/Instantly-Setup.md)
5. [Monitoring and Reporting](Support/Monitoring-and-Reporting.md)
6. [Reply Management](Support/Reply-Management.md)
7. [Telegram Notification Setup](Support/Telegram-Notification-Setup.md)
8. [Campaign Performance Database](Support/Campaign-Performance-Database.md)
9. [Lead Collection](Support/Lead-Collection.md)
10. [Segmentation and File QA](Support/Segmentation-and-File-QA.md)

This order follows the SOP priority order and keeps the agent focused on campaign safety before launch speed.

---

## 02. Support File Map

| File | Main Use | Agent Should Use It When |
|---|---|---|
| [Email Infrastructure](Support/Email-Infrastructure.md) | Domains, DNS, mailboxes, tracking, warmup, sending limits | Checking whether sending infrastructure is ready |
| [Verification and Suppression](Support/Verification-and-Suppression.md) | Email verification, risky emails, duplicate handling, suppression list | Preparing or approving a clean sending list |
| [Email Sequence QA](Support/Email-Sequence-QA.md) | Subject lines, body length, Instantly format, fallback tokens, opener QA | Writing or checking campaign sequences |
| [Instantly Setup](Support/Instantly-Setup.md) | CSV upload, field mapping, campaign settings, test emails, pilot launch | Setting up a campaign inside Instantly |
| [Monitoring and Reporting](Support/Monitoring-and-Reporting.md) | Daily monitoring, pause rules, scale rules, final report | Managing live campaigns and reporting results |
| [Reply Management](Support/Reply-Management.md) | Interested, pricing, unsubscribe, wrong person, referral, OOO, negative replies | Classifying and responding to campaign replies |
| [Telegram Notification Setup](Support/Telegram-Notification-Setup.md) | Telegram alerts, routing, positive reply notification format | Sending campaign alerts to the team |
| [Campaign Performance Database](Support/Campaign-Performance-Database.md) | Winning sequences, reply reasons, meetings, lead source quality | Storing campaign learning after launch |
| [Lead Collection](Support/Lead-Collection.md) | Apollo filters, bot fields, source tracking, handoff process | Collecting raw lead data before enrichment |
| [Segmentation and File QA](Support/Segmentation-and-File-QA.md) | Segment rules, ICP gate, CSV checks, company cleanup, approval | Preparing final segmented CSV files |

---

## 03. How the Agent Should Use These Files

The agent should not use these files randomly.

It should choose the file based on the campaign stage:

```text
Infrastructure question -> Support/Email-Infrastructure.md
Lead source or Apollo question -> Support/Lead-Collection.md
Email quality or suppression question -> Support/Verification-and-Suppression.md
Segment or CSV question -> Support/Segmentation-and-File-QA.md
Copywriting or sequence question -> Support/Email-Sequence-QA.md and Brand-voice.md
Instantly setup question -> Support/Instantly-Setup.md
Live campaign issue -> Support/Monitoring-and-Reporting.md
Reply handling question -> Support/Reply-Management.md
Positive reply report -> positive-response-lead-report-agent.md
Telegram alert question -> Support/Telegram-Notification-Setup.md
Campaign learning/history question -> Support/Campaign-Performance-Database.md
```

If the agent is not sure which file to use, it should start with:

```text
Master.md
```

and then move to the most relevant support file.

---

## 04. Required Agent Behavior

The agent must:

- Follow `SOP.md` as the main operating process.
- Use `Master.md` to understand the full campaign workflow.
- Use `Brand-voice.md` before writing any email copy.
- Use `ICP.md` before approving campaign fit.
- Use `data-enrichment.md` before finalizing any lead list.
- Use the support files for detailed operational checks.
- Avoid guessing when data is missing.
- Use `Unknown`, `Not Found`, `Not Confirmed`, or `Needs Manual Review` when information cannot be verified.
- Never launch a campaign before infrastructure, list quality, sequence QA, unsubscribe setup, and approval checks pass.

---

## 05. Final Campaign Flow With Support Files

Use this complete flow:

1. [Lead Collection](Support/Lead-Collection.md)
2. [Data Enrichment](data-enrichment.md)
3. [ICP Analysis](ICP.md)
4. [Segmentation and File QA](Support/Segmentation-and-File-QA.md)
5. [Verification and Suppression](Support/Verification-and-Suppression.md)
6. [Email Infrastructure](Support/Email-Infrastructure.md)
7. [Brand Voice](Brand-voice.md)
8. [Email Sequence QA](Support/Email-Sequence-QA.md)
9. [Instantly Setup](Support/Instantly-Setup.md)
10. [Monitoring and Reporting](Support/Monitoring-and-Reporting.md)
11. [Reply Management](Support/Reply-Management.md)
12. [Positive Response Lead Report Agent](positive-response-lead-report-agent.md)
13. [Telegram Notification Setup](Support/Telegram-Notification-Setup.md)
14. [Campaign Performance Database](Support/Campaign-Performance-Database.md)

This flow helps the agent move from raw data to campaign launch, monitoring, reply handling, and learning history.

---

## 06. Final Rule

`Support.md` is the index file.

It does not replace the SOP or the detailed support files.

It tells the email marketing agent where to look, which file to use, and how the support documents connect.
