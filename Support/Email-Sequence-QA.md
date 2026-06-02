# Email Sequence QA

## Purpose

This file defines how Accord Tech Solutions creates, checks, and approves cold email sequences before upload into Instantly or any other platform.

Use this file for subject lines, email body quality, Instantly.ai format, personalization tokens, fallback values, custom openers, links, UTMs, and final approval.

---

## 01. Main Goal

The goal of email sequence QA is to make sure every sequence is:

- Short
- Human
- Professional
- Segment-specific
- Reply-focused
- Deliverability-safe
- Correctly personalized
- Aligned with ATS brand voice
- Ready for Instantly setup

The first email should create a reply, not force a meeting.

---

## 02. Required Writing Sequence

Before writing the final sequence:

1. Review ICP and segment.
2. Review service fit.
3. Review available personalization fields.
4. Create the sequence-writing prompt.
5. Discuss the prompt with the team.
6. Write the sequence.
7. QA the sequence.
8. Send for CEO and ED approval when required.
9. Only then upload to Instantly.

Do not write one generic template for multiple segments.

---

## 03. Instantly House Format

Use this standard structure:

```text
Subject: [short subject line]

{{RANDOM | Hi | Hey | Greetings}} {{firstName}},

[Hook - observation, stat, or named trigger about the prospect's company]

[Value frame - what was noticed, what may be possible, or what ATS helps with]

[Soft CTA as a question]

{{RANDOM | Best regards, | Cheers, | Thanks, | Warm regards, }}
{{accountSignature}}
```

This format keeps the sequence consistent with the existing ATS Instantly.ai campaign style.

---

## 04. Sequence Length Rule

Default sequence:

```text
4 steps
```

Recommended structure:

- Email 1: first outreach
- Email 2: follow-up with one new point
- Email 3: follow-up with proof, checklist, or useful angle
- Email 4: closing-loop or breakup email

Acceptable minimum:

```text
3 steps
```

Do not create a one-step cold campaign unless it is an infrastructure or deliverability test.

---

## 05. Cadence Rule

Default cadence:

```text
Day 0 -> Day 3 -> Day 6/7 -> Day 10/11 -> Final close
```

Common delay pattern:

```text
3 -> 3 -> 4 -> 1
```

Also acceptable:

```text
3 -> 4 -> 4 -> 1
3 -> 4 -> 5 -> 1
```

Avoid sending follow-ups too aggressively.

---

## 06. Subject Line Rules

Subject lines should be:

- 3-5 words when possible
- Natural
- Relevant to the segment
- Low-pressure
- Different for each step
- Not repeated directly in the body
- Free from hype and clickbait

Avoid:

```text
Quick Question
FREE!!!
100% guaranteed
Final attempt
Urgent
Limited-time offer
```

Good subject styles:

```text
{{companyName}} outreach
lead list quality
campaign prep
CRM data question
Found friction on {{companyName}}
Closing the loop
```

---

## 07. Body Length Rule

Recommended body length:

```text
55-70 words
```

Acceptable range:

```text
25-110 words
```

Reading time target:

```text
Under 20 seconds
```

Use:

- Plain language
- Short lines
- 2-4 short paragraphs
- One idea per paragraph
- One CTA

Avoid:

- Long intros
- Multiple services in one email
- Heavy formatting
- Hard meeting asks in Email 1
- Overexplaining ATS

---

## 08. CTA Rule

Use permission-based CTAs.

Good CTAs:

```text
Should I send a simple example?
Would it be useful if I shared the process?
Should I share a short checklist?
Would a quick list-quality review be useful?
Should I leave this for now?
Would you like me to send it over?
```

Avoid early meeting CTAs:

```text
Can we book a call?
Are you free tomorrow?
What time works?
Click here to schedule.
```

Meeting CTAs should only be used after the prospect shows interest.

---

## 09. Token Standardization

Use consistent token casing.

Preferred tokens:

```text
{{firstName}}
{{companyName}}
{{industry}}
{{state}}
{{accountSignature}}
```

Avoid mixing:

```text
{{companyName}}
{{CompanyName}}
```

Avoid inconsistent review tokens:

```text
{{Rating}}
{{Ratings}}
{{Number_of_Reviews}}
{{Reviews}}
```

Before upload, match every token to the CSV column name and Instantly mapping.

---

## 10. Fallback Rules

All personalization tokens must have fallback values.

Rules:

```text
{{firstName}} blank -> there
{{companyName}} blank -> your company
{{industry}} blank -> your market
{{state}} blank -> your area
```

If a required token is missing and no neutral fallback works, rewrite the sentence without that token.

Do not let blank tokens render inside the campaign.

---

## 11. Custom Opener QA

Before launch, manually review at least:

```text
20 random rows
```

Check:

- Opener accuracy
- Correct personalization mapping
- Segment relevance
- No awkward fallback
- No fake compliment
- No unsupported claim
- Company and industry match the sentence

If more than 2 reviewed rows have personalization errors, pause sequence upload and fix the data or copy.

---

## 12. Link and UTM QA

Test every link before launch.

Check:

- Link opens correctly
- UTM values are correct
- Tracking domain is verified
- No broken redirect
- No wrong company or segment link
- Unsubscribe link works when required

If links are not needed, prefer no links in early cold emails to protect deliverability.

---

## 13. A/B Testing Rule

Every active campaign should include a simple test when possible.

Recommended tests:

- Subject A vs Subject B
- Observation hook vs stat hook
- Checklist CTA vs example CTA
- Short proof line vs no proof line

Do not test too many things at once.

Track the winner by:

- Open rate
- Reply rate
- Positive reply rate
- Bounce rate
- Unsubscribe rate

---

## 14. Approved Output Format

When the agent creates a sequence, use this format:

```text
Campaign Segment:
Primary ATS Service Fit:
Main Pain Point:
Personalization Fields Used:
Fallback Values:
Cadence:

Email 1
Subject:
Body:

Email 2
Delay:
Subject:
Body:

Email 3
Delay:
Subject:
Body:

Email 4
Delay:
Subject:
Body:

QA Notes:
Approval Status:
```

---

## 15. Final QA Checklist

Before approval, confirm:

- Segment-specific script created
- Subject lines are short and natural
- Body length is acceptable
- Sequence uses one main angle
- CTA is soft
- No hard meeting ask in Email 1
- No spammy words
- Tokens match CSV fields
- Fallbacks are defined
- 20 random openers reviewed
- Links and UTMs tested
- Opt-out line or unsubscribe setting is ready when required
- Sequence follows Brand-voice.md
- CEO and ED approval received when required

---

## 16. Final Rule

A sequence is not ready because it sounds good.

It is ready only when it is relevant to the segment, mapped correctly in Instantly, tested with real fields, approved internally, and safe to send.
