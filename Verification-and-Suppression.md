# Verification and Suppression Handling

## Purpose

This file defines how Accord Tech Solutions verifies email data, removes risky contacts, handles generic emails, logs duplicates, and maintains the suppression list.

Use this file before any campaign upload and after every campaign close.

---

## 01. Main Goal

The goal is to keep campaign lists clean, compliant, and deliverability-safe.

Every campaign list must protect:

- Bounce rate
- Sender reputation
- Prospect trust
- Compliance
- Future campaign quality

Campaign target:

```text
Bounce rate below 2%
```

---

## 02. Approved Verification Tools

Use one or more approved tools:

- Debounce
- NeverBounce
- ZeroBounce
- Platform-built-in verifier

If the tool results conflict, use the more conservative result unless the email marketing lead approves otherwise.

---

## 03. Verification Status Categories

Classify every email into one of these statuses:

```text
Valid
Invalid
Risky
Unknown
Catch-All
Disposable
Role-Based
Duplicate
Suppressed
Needs Manual Review
```

Only `Valid` emails should move directly to the final campaign-ready list.

---

## 04. Invalid Email Rule

Remove invalid emails from the campaign-ready list.

Mark them as:

```text
Invalid Email
```

Invalid emails should not be uploaded to Instantly or any other sending platform.

---

## 05. Risky and Unknown Email Rule

Move risky and unknown results to a quarantine tab.

Use these remarks:

```text
Risky Email - Quarantine
Unknown Email - Quarantine
```

Do not use risky or unknown emails in a campaign unless leadership explicitly approves a controlled test.

---

## 06. Generic Email Rule

Generic emails should be removed or separated before campaign upload.

Examples:

```text
info@
admin@
sales@
support@
contact@
hello@
office@
team@
marketing@
careers@
jobs@
press@
billing@
accounts@
```

Mark generic emails as:

```text
Generic Email
```

Use personal decision-maker emails whenever possible.

---

## 07. Role-Based Email Rule

Role-based addresses are not ideal for B2B cold campaigns.

Examples:

```text
ceo@
founder@
owner@
manager@
director@
marketing@
sales@
hr@
support@
```

If the address is clearly role-based, mark it as:

```text
Role-Based Email
```

Use only if the campaign has a specific approved reason.

---

## 08. Duplicate Contact Rule

The same email address should not appear more than once in the final sending list.

Primary duplicate identifier:

```text
Email
```

Secondary identifiers:

- LinkedIn profile
- First name
- Last name
- Company domain
- Company name

Keep the best and most complete record.

Mark removed duplicate rows as:

```text
Duplicate Contact
```

Export removed duplicates to a separate duplicate log.

---

## 09. Duplicate Company Rule

If the campaign allows only one contact per company, keep the strongest decision-maker only.

If the campaign allows multiple contacts per company, follow the SOP sending limit:

```text
2-3 emails per day per company
```

Mark extra company records as:

```text
Duplicate Company
```

or:

```text
Approved Multi-Contact Company
```

when multiple contacts are intentionally retained.

---

## 10. Suppression List Rule

Before upload, check the list against the centralized suppression list:

<https://docs.google.com/spreadsheets/d/1Fplns4qU3NH3HD23g9mqsFaTO_RCEV2so4d7KoVnTSg/edit?gid=0#gid=0>

Remove any contact or company that appears in the suppression list.

Mark the row as:

```text
Suppressed - Do Not Contact
```

Suppressed contacts must never be uploaded into a new campaign.

---

## 11. When to Add to Suppression

Add a contact to the suppression list when they:

- Unsubscribe
- Say remove me
- Say stop contacting me
- Complain about the outreach
- Ask not to be contacted again
- Are marked internally as do not contact
- Create legal or reputational risk

Add the company domain too when the request clearly applies to the full company.

---

## 12. Suppression List Fields

The suppression list should include:

- Email
- First Name
- Last Name
- Company Name
- Company Domain
- Reason
- Source Campaign
- Request Date
- Added By
- Notes

Use clear reasons:

```text
Unsubscribed
Remove Request
Complaint
Do Not Contact
Internal Suppression
Hard Bounce
Legal Risk
```

---

## 13. Hard Bounce Handling

If a campaign produces hard bounces:

1. Export bounced contacts.
2. Add hard-bounced emails to the suppression list.
3. Review the verification source.
4. Check whether the bounce came from a specific segment, source, or inbox.
5. Pause scaling until the cause is understood.

If bounce rate rises above:

```text
2%
```

pause the affected campaign or segment.

---

## 14. Final Campaign-Ready Status

A contact can be marked campaign-ready only if:

- Email is valid
- Email is not generic
- Email is not role-based unless approved
- Contact is not suppressed
- Contact is not duplicate
- Company is not duplicate unless approved
- First name is usable
- Company name is clean
- ICP check passes

Use this status:

```text
Campaign Ready
```

---

## 15. Verification Output Columns

Add or maintain these columns:

```text
Email Verification Status
Verification Tool
Verification Date
Generic Email Status
Duplicate Contact Status
Duplicate Company Status
Suppression Status
Final Sending Status
Remarks
```

---

## 16. Final Rule

Do not sacrifice list quality for volume.

If a contact creates bounce risk, compliance risk, or reputational risk, remove it from the campaign-ready list and document the reason.
