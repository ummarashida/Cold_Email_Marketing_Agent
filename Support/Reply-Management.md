# Reply Management

## Purpose

This file defines how Accord Tech Solutions classifies, responds to, escalates, and records all cold email replies.

Use this file for interested replies, pricing questions, send-more-info replies, not interested replies, unsubscribe requests, wrong person replies, referrals, out-of-office replies, auto replies, negative replies, and unclear replies.

---

## 01. Main Goal

The goal of reply management is to respond quickly, protect compliance, route real opportunities, and keep campaign data accurate.

Every reply should be classified before action.

---

## 02. Core Reply Categories

Classify replies as:

```text
Interested
Send More Info
Pricing Question
Meeting Request
Not Interested
Unsubscribe / Remove Me
Wrong Person
Referral
Out of Office
Auto Reply
Negative Reply
Unclear / Needs Review
```

If the classification is uncertain, mark it as:

```text
Needs Manual Review
```

---

## 03. Universal Reply Rules

For every reply:

1. Stop the sequence for that lead.
2. Classify the reply.
3. Update campaign tags or CRM.
4. Respond using the approved brand voice.
5. Add suppression when required.
6. Record the campaign, step, subject, and body that generated the reply.
7. Escalate interested replies to the sales follow-up owner.

Stop-on-reply must be enabled in Instantly, but the team should still verify important replies manually.

---

## 04. Interested Reply

Examples:

```text
Interested.
Tell me more.
Can you send details?
This sounds useful.
How does this work?
```

Action:

- Mark as Interested
- Create positive response lead report
- Send or prepare a helpful response
- Notify the assigned team member
- Move to sales follow-up

Use positive-response-lead-report-agent.md for the full report.

---

## 05. Send More Info

Recommended response:

```text
Hi {{firstName}},

Sure - happy to share.

ATS helps B2B teams with prospect research, data enrichment, CRM cleanup, and cold email campaign support. The main goal is to improve the quality of targeting, campaign setup, and sales conversations before your team spends time on bad-fit leads.

I can also share a simple example based on your market.

Best,
{{senderName}}
```

If the original campaign promised a PDF, checklist, audit, or report, send that asset or prepare it for human approval.

---

## 06. Pricing Question

Recommended response:

```text
Hi {{firstName}},

Pricing depends on the scope, list size, research depth, and campaign support needed.

If you share the rough volume and goal, I can suggest the most practical structure.

Best,
{{senderName}}
```

Action:

- Mark as Pricing Question
- Escalate to sales owner
- Ask for scope before quoting
- Do not invent pricing

---

## 07. Meeting Request

Examples:

```text
Can we talk?
Do you have time this week?
Send your calendar.
```

Action:

- Mark as Meeting Request
- Notify the sales owner immediately
- Provide calendar link only if approved
- Prepare company and contact context

Response should be short and helpful.

---

## 08. Not Interested

Recommended response:

```text
Understood, thanks for letting me know.

I will not follow up further.

Best,
{{senderName}}
```

Action:

- Mark as Not Interested
- Stop sequence
- Add to suppression list if the reply indicates no future contact

---

## 09. Unsubscribe / Remove Me

Examples:

```text
Unsubscribe.
Remove me.
Stop emailing me.
Do not contact me again.
```

Action:

1. Add to suppression list immediately.
2. Stop all future sending to that email.
3. Suppress company domain if the request clearly applies to the company.
4. Do not send a sales response.

Optional confirmation:

```text
Confirmed - you have been removed.
```

Keep this response short.

---

## 10. Wrong Person

Examples:

```text
I am not the right person.
This is not my area.
```

Action:

- Mark as Wrong Person
- Ask only if a referral is natural
- Do not pressure the prospect

Recommended response:

```text
Thanks for letting me know.

Is there someone better on your team for this, or should I close the loop here?
```

---

## 11. Referral

Examples:

```text
Please contact Sarah.
John handles this.
```

Action:

- Mark as Referral
- Add referred contact if appropriate
- Verify the referred email before sending
- Keep the original contact noted as referral source

Do not email the referred person if they are already suppressed.

---

## 12. Out of Office

Action:

- Mark as Out of Office
- Check return date
- Schedule follow-up after return if relevant
- Do not suppress unless the auto reply asks for removal

If a replacement contact is listed, verify before use.

---

## 13. Auto Reply

Examples:

```text
Ticket created.
We received your message.
This mailbox is not monitored.
```

Action:

- Mark as Auto Reply
- Do not count as positive reply
- Review for useful routing information
- Suppress if mailbox is not monitored and no useful contact exists

---

## 14. Negative Reply

Negative replies may include frustration, complaint, or hostile tone.

Action:

- Stop sequence
- Add to suppression if needed
- Do not argue
- Do not defend the campaign
- Escalate if complaint risk exists

Recommended response when appropriate:

```text
Understood. I apologize for the interruption and will make sure you are not contacted again.
```

---

## 15. Unclear Reply

If the reply cannot be confidently classified:

- Mark as Unclear / Needs Review
- Do not send an automated response
- Escalate to human review

Do not guess prospect intent.

---

## 16. Reply Data to Record

For every meaningful reply, record:

```text
Campaign Name
Segment
Lead Source
Company Name
Contact Name
Email
Reply Category
Reply Summary
Sequence Step
Subject Line
Email Version
Next Action
Owner
Suppression Status
Date Received
Notes
```

---

## 17. Final Rule

Reply handling should be calm, fast, and accurate.

Interested replies should move forward quickly. Removal requests should be honored immediately. Unclear replies should be reviewed before response.
