# Positive-Reply Agent - Full Process Specification

## Purpose

When a cold-email campaign gets a positive reply, this agent automatically:

1. Sends a Telegram notification.
2. Builds a one-page company and person portfolio.
3. Reports which sequence and step the reply came from.
4. Analyzes the reply and proposes the best response approach with multiple variants to choose from.

---

## 1. Trigger

| Item | Value |
|---|---|
| Event | A reply is detected on an active cold-email campaign |
| Source | Sending platform webhook, such as Instantly, Smartlead, or Apollo |
| Condition | Reply is classified as positive |
| Action on trigger | Fire the full pipeline below, then push to Telegram |

Important:

The sequence must stop immediately for this lead the moment any reply lands, including positive, neutral, or out-of-office. No follow-up should fire on top of a live conversation.

---

## 2. Inputs the Agent Receives

The agent receives data from the webhook payload and the campaign list used to build the campaign.

```json
{
  "lead_email": "person@company.com",
  "campaign_id": "...",
  "sequence_step": 2,
  "reply_text": "full text of their reply",
  "replied_at": "ISO timestamp",
  "lead_data": {
    "first_name": "...",
    "last_name": "...",
    "title": "...",
    "company": "...",
    "company_domain": "...",
    "linkedin": "...",
    "phone": "...",
    "signal_used": "the trigger signal this lead was targeted with",
    "...": "any other enriched fields from the original list"
  },
  "sequence_meta": {
    "email_1_subject": "...",
    "email_1_body": "...",
    "step_that_got_reply": 2,
    "body_that_got_reply": "..."
  }
}
```

The agent works only from the list data already attached to the lead plus the reply.

If a field is missing, the agent may enrich it through the connected enrichment source. It must never invent facts.

---

## 3. Step 1 - Classify the Reply

Classify the reply as:

```text
Positive
Neutral
Negative
Out of Office
Wrong Person
Unsubscribe
```

### Positive Reply Signals

A reply is positive if the prospect:

- Asks for a call
- Asks for a demo
- Asks for pricing
- Asks for more information
- Says interested
- Says tell me more
- Asks to send the deck, teardown, sample, or overview
- Asks a qualifying question about timing, fit, or how it works
- Refers the sender to the right person

### Not Positive

Do not fire the full positive-reply pipeline for:

- Hard no
- Not interested
- Unsubscribe
- Remove me
- Out-of-office
- Wrong person with no referral

Route these separately:

| Reply Type | Action |
|---|---|
| Hard no / not interested | Mark closed |
| Unsubscribe / remove me | Add to suppression list immediately |
| Out-of-office | Re-queue for return date if available |
| Wrong person with no referral | Mark for re-routing |

### Classification Output

```text
classification: POSITIVE
confidence: 0.0-1.0
reason: short one-line reason
```

If positive classification confidence is low, flag for human review instead of auto-drafting.

---

## 4. Step 2 - Build the One-Page Portfolio

Build a single-page profile that combines company details, person details, and engagement details.

Pull from list data first. Enrich only the gaps.

### 4.1 Company Block

Include:

- Company name
- Domain
- Website
- Industry or vertical
- Company size
- Revenue band if known
- HQ location
- Funding or stage if available
- Recent signals from the last 90 days
- Tech stack if enriched
- One-line description of what the company does

Recent signals may include:

- Funding
- Hiring
- Product launches
- News
- Partnerships
- Expansion

### 4.2 Person Block

Include:

- Full name
- Title
- Seniority or role
- LinkedIn URL
- Email
- Phone if available
- Reports-to or team if known
- Trigger signal used for targeting
- Prior touch history

### 4.3 Engagement Block

Include:

- Campaign name or ID
- Sequence step that received the reply
- Exact email body that earned the reply
- Days from send to reply
- Reply text verbatim

### Enrichment Rule

If a field is missing, enrich through the connected enrichment source.

If the field still cannot be verified, mark it as:

```text
unknown
```

Never guess.

---

## 5. Step 3 - Sequence Attribution Report

The agent reports which approach produced the positive reply.

| Field | Example |
|---|---|
| Campaign | Q2 SaaS founders |
| Total steps in sequence | 4 |
| Step that got the reply | Email 2, Day 3 bump |
| Subject line of that step | follow-up process |
| Body of that step | Verbatim body |
| Approach type of that step | Signal-hook + soft interest check |
| Time to reply | 3 days |

This builds a running record of which sequences, steps, and approaches produce positive replies.

The goal is to identify winning angles and double down on them.

---

## 6. Step 4 - Reply Analysis and Suggested Response Variants

The agent decides what type of reply should be sent back, then drafts multiple variants for review.

### 6.1 Decide the Response Intent

Choose the response intent based on what the prospect actually asked.

| Prospect Reply | Response Intent |
|---|---|
| Asked for a call | Push toward booking with 2 time windows |
| Asked for info, deck, teardown, or sample | Send the asset and ask one light qualifying question |
| Asked a question | Answer concisely and advance to the next step |
| Gave a referral | Thank them and ask for a warm intro or permission to mention them |
| Lukewarm / maybe later | Soft nurture and set a future check-in |

Do not dump a calendar link too early. Keep the response conversational and low-pressure.

### 6.2 Produce Response Variants

Generate 2-3 response variants for the chosen intent.

Each variant should be labeled by strategy.

Examples:

- Direct booking angle
- Send value first angle
- Consultative angle
- Light qualification angle

Each variant must:

- Be plain text
- Be short
- Use one CTA
- Avoid spam-trigger phrases
- Avoid overexplaining
- Match the ATS brand voice

---

## 7. Step 5 - Telegram Notification

After classification, portfolio creation, sequence attribution, and reply analysis are complete, push one message to Telegram.

Suggested format:

```text
POSITIVE REPLY - {{first_name}} @ {{company}}

Person:
{{first_name}} {{last_name}} - {{title}}

Company:
{{company}} - {{industry}} - {{size}} - {{location}}

LinkedIn:
{{linkedin}}

Replied to:
{{campaign}} - Step {{step}} ({{step_type}})

Time to reply:
{{days_to_reply}} days

Their reply:
"{{reply_text}}"

Intent:
{{detected_intent}}

Suggested approach:
{{approach_label}}

Variants are ready below or in the dashboard.
```

The full one-page portfolio and response variants should be attached or linked so everything is available in one place.

---

## 8. End-to-End Flow Summary

```text
Positive reply detected
        |
        v
[1] Classify reply
        |
        |-- not positive -> route to closed / OOO re-queue / re-route / suppression
        |
        v
[2] Build one-page portfolio
        |
        v
[3] Create sequence-attribution report
        |
        v
[4] Analyze reply -> decide intent -> draft 2-3 response variants
        |
        v
[5] Send Telegram notification
        |
        v
User picks a variant -> send
```

---

## 9. Hard Rules for the Agent

1. Stop the sequence for any lead the instant a reply lands.
2. Use only list data plus verified enrichment.
3. Never invent company or person facts.
4. Use one CTA per response email.
5. Avoid multi-ask replies.
6. Avoid spam-trigger phrases such as "circle back", "touch base", "I hope this finds you well", and "game-changer".
7. Keep response emails plain text and short.
8. Do not use images in response emails.
9. Do not use tracking pixels in response emails.
10. Mark unverifiable fields as `unknown`.
11. Flag low-confidence positive classification for human review.
12. Add unsubscribe or remove-me replies to the suppression list immediately.

---

## 10. Required Integrations and Setup

### Sending Platform Webhook

Required for reply detection.

Supported sources:

- Instantly
- Smartlead
- Apollo

### Enrichment Source

Used to fill portfolio gaps.

Supported sources:

- Clay
- Apollo
- Other approved enrichment source

### Telegram Bot

Required for notification delivery.

Needs:

- Bot token
- Chat ID
- Approved message format

### Storage

Storage should keep a running record of:

- Positive replies
- Reply classification
- Campaign name
- Sequence step
- Winning subject lines
- Winning body copy
- Winning approach type
- Response variant selected
- Outcome after reply

---

## 11. Output Format

When the agent processes a positive reply, produce:

```text
Classification:

Confidence:

Reason:

Company Portfolio:

Person Portfolio:

Engagement Details:

Sequence Attribution:

Detected Intent:

Suggested Approach:

Response Variant A:

Response Variant B:

Response Variant C:

Telegram Notification:

Fields Marked Unknown:

Human Review Needed:
```

---

## Final Rule

The agent exists to help ATS respond to positive replies quickly, accurately, and professionally.

It must protect live conversations, avoid unsupported claims, show which campaign approach worked, and give the user clear response options.
