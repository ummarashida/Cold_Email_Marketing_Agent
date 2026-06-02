# Telegram Notification Setup

## Purpose

This file defines how Accord Tech Solutions should structure Telegram notifications for important cold email campaign events, especially positive replies.

Use this file for Telegram alert fields, routing, testing, and notification quality.

---

## 01. Main Goal

The goal of Telegram notifications is to make sure important campaign replies are noticed quickly and routed to the correct team member.

Priority alerts:

- Positive replies
- Meeting requests
- Pricing questions
- Referral replies
- High-risk complaints
- Campaign health issues

---

## 02. Required Setup Information

Before enabling Telegram alerts, confirm:

```text
Telegram Bot Token
Telegram Chat ID
Campaign Name
Notification Owner
Alert Trigger
Test Status
```

Do not expose the bot token publicly.

Store credentials only in approved secure locations.

---

## 03. Alert Triggers

Send Telegram alerts for:

- Interested reply
- Send more info reply
- Pricing question
- Meeting request
- Referral
- Negative complaint
- Bounce spike
- Campaign paused
- Inbox unhealthy

Do not send noisy alerts for every open, auto reply, or routine metric update unless specifically requested.

---

## 04. Positive Reply Alert Format

Use this format:

```text
Positive Reply Alert

Campaign: [Campaign Name]
Segment: [Segment]
Company: [Company Name]
Contact: [First Name Last Name]
Title: [Job Title]
Email: [Email]
Reply Type: [Interested / Send More Info / Pricing / Meeting Request]
Sequence Step: [Step Number]
Subject: [Subject Line]
Reply Summary: [Short summary]
Recommended Action: [Next step]
Owner: [Team member]
Received: [Date and time]
```

Keep the alert short enough to read quickly.

---

## 05. Campaign Health Alert Format

Use this format:

```text
Campaign Health Alert

Campaign: [Campaign Name]
Issue: [Bounce Spike / Inbox Unhealthy / Complaint / Mapping Error]
Metric: [Relevant number]
Affected Segment: [Segment]
Affected Inbox: [Inbox if applicable]
Recommended Action: [Pause / Review / Remove Inbox / Check Mapping]
Owner: [Team member]
Detected: [Date and time]
```

Only send health alerts for issues that require action.

---

## 06. Notification Routing

Route alerts based on type:

```text
Positive Reply -> Sales follow-up owner
Pricing Question -> Sales/leadership owner
Meeting Request -> Sales owner
Referral -> Campaign owner
Complaint -> Campaign manager and leadership
Bounce Spike -> Email marketing lead
Inbox Unhealthy -> Infrastructure owner
```

If ownership is unclear, send the alert to the campaign manager.

---

## 07. Test Process

Before using Telegram alerts in a live campaign:

1. Send a test positive reply alert.
2. Confirm the correct chat receives it.
3. Confirm formatting is readable.
4. Confirm no sensitive token appears in the message.
5. Confirm owner routing is correct.
6. Confirm alert time is correct.
7. Confirm duplicate alerts are not sent.

Mark test status as:

```text
Passed
```

only after the test is confirmed.

---

## 08. Alert Quality Rules

Every alert should be:

- Short
- Actionable
- Accurate
- Routed correctly
- Free from invented details
- Linked to a campaign and owner

If data is missing, use:

```text
Unknown
Not Found
Not Confirmed
```

Do not guess company facts, reply intent, or next action.

---

## 09. Positive Reply Report Connection

Telegram alerts should connect with the positive-response lead report process.

For interested replies, the alert should mention:

- Sequence step that generated the reply
- Subject line
- Reply category
- Recommended response
- Whether a lead report is ready

Use positive-response-lead-report-agent.md for detailed reporting.

---

## 10. Final Rule

Telegram notifications should help the team act faster.

Do not create noisy alerts that make important replies harder to notice.
