# Instantly Campaign Setup

## Purpose

This file defines how Accord Tech Solutions sets up cold email campaigns inside Instantly after the list, sequence, infrastructure, and approvals are complete.

Use this file for CSV upload, field mapping, sequence setup, account selection, schedule, unsubscribe settings, stop-on-reply, test emails, and pilot launch.

---

## 01. Pre-Setup Requirements

Before opening a campaign in Instantly, confirm:

- Final CSV is approved
- ICP check is complete
- Verification and suppression checks are complete
- Sequence QA is complete
- Personalization fallbacks are ready
- Infrastructure is approved
- Sending inboxes are healthy
- CEO and ED approval received when required

If any item is incomplete, keep the campaign in:

```text
Setup Pending
```

---

## 02. Campaign Naming Rule

Use a clear campaign name.

Recommended format:

```text
[Segment] - [Service Angle] - [Batch/Date]
```

Examples:

```text
HVAC - SEO Visibility - Batch 01
SaaS - Cold Email Outreach - June 2026
Portfolio - Growth Support - Batch 02
```

The campaign name should make reporting easy later.

---

## 03. Upload CSV

Process:

1. Open Instantly.
2. Go to Campaigns.
3. Create or open the approved campaign.
4. Click Add Leads.
5. Upload the final CSV.
6. Confirm row count.
7. Check for upload errors.
8. Do not proceed if required fields fail.

Only upload the final campaign-ready list.

---

## 04. Required Field Mapping

Map all required columns carefully.

Standard mapping:

```text
{{firstName}} -> First Name
{{companyName}} -> Company Name
{{industry}} -> Industry
{{state}} -> State
{{accountSignature}} -> Account Signature
```

Also map any campaign-specific fields, such as:

```text
{{Rating}}
{{Number_of_Reviews}}
{{Reputation_Score}}
{{Years_In_Business}}
{{Found_Keywords}}
{{Funding_Type}}
{{Rank}}
{{Personalization_Note}}
```

Every token used in the sequence must map to a CSV column or have a safe fallback.

---

## 05. Token Casing Rule

Use one casing style throughout the campaign.

Preferred:

```text
{{firstName}}
{{companyName}}
```

Avoid mixing:

```text
{{companyName}}
{{CompanyName}}
```

If the CSV uses different casing, either rename the CSV column or update the sequence before launch.

---

## 06. Add Sequence Steps

Default Instantly setup:

```text
3-4 sequence steps
```

Recommended:

- Email 1: cold open
- Email 2: follow-up after 3-4 days
- Email 3: follow-up after 3-5 days
- Email 4: closing-loop or breakup email

Add subject lines and body copy exactly as approved in Email-Sequence-QA.md.

---

## 07. Sequence Formatting

Use the approved ATS Instantly format:

```text
{{RANDOM | Hi | Hey | Greetings}} {{firstName}},

[Body]

{{RANDOM | Best regards, | Cheers, | Thanks, | Warm regards, }}
{{accountSignature}}
```

Check that spintax renders correctly.

Do not add unnecessary images, heavy HTML, or extra links.

---

## 08. Sending Schedule

Avoid:

- Monday early morning
- Friday late afternoon
- Weekends unless the campaign has a specific reason

Recommended sending window:

```text
Tuesday to Thursday
Business hours in target timezone
```

Set timezone based on the campaign geography.

For USA campaigns, use the relevant US timezone or a safe national sending window.

---

## 09. Sending Limits

For each inbox, follow the infrastructure settings:

```text
Campaign limit: 10
Minimum wait time: 30 minutes
Warmup per day: 25
```

For multiple contacts from the same company:

```text
2-3 emails per day per company
```

Do not scale sending before pilot results are reviewed.

---

## 10. Account Selection

Select only approved inboxes.

Check:

- Inbox is connected
- Warmup is active
- Custom tracking is verified if used
- No unhealthy status
- Inbox is not assigned beyond safe capacity
- Sender name and signature are correct

If one inbox is unhealthy, remove it from the campaign before launch.

---

## 11. Safety Settings

Enable:

- Stop sending emails on reply
- Unsubscribe option or unsubscribe header when required
- Open tracking if approved
- Custom tracking domain when tracking is used

Confirm:

- Reply detection works
- Unsubscribe setup works
- Tracking domain is verified
- No duplicate campaign sends

Stop-on-reply must be enabled for every cold email campaign.

---

## 12. Tracking Settings

Default measurement:

- Open tracking enabled when approved
- Link tracking disabled unless the campaign needs click data
- Custom tracking domain verified before tracking is used

If link tracking is enabled, test every link and UTM before launch.

Do not enable tracking through an unverified tracking domain.

---

## 13. Test Email Process

Before launch:

1. Send test emails to internal addresses.
2. Check subject lines.
3. Check greeting.
4. Check every personalization token.
5. Check fallback rendering.
6. Check signature.
7. Check unsubscribe link or header.
8. Check links and UTMs if used.
9. Check mobile readability.
10. Confirm no broken spintax.

If any test fails, fix it and send another test.

---

## 14. Pilot Batch Launch

Start with:

```text
10-15% of the list
```

Pilot launch goals:

- Catch mapping issues
- Check deliverability
- Watch bounce rate
- Review personalization quality
- Confirm replies stop the sequence
- Confirm reporting works

Do not launch the full list until pilot performance is reviewed.

---

## 15. Launch Approval Checklist

Before switching the campaign live, confirm:

- CSV uploaded correctly
- Fields mapped correctly
- Tokens render correctly
- Fallbacks tested
- Sequence steps added
- Schedule configured
- Healthy accounts selected
- Sending limits set
- Stop-on-reply enabled
- Unsubscribe setup tested
- Tracking settings checked
- Test emails reviewed
- Pilot batch selected
- Monitoring owner assigned

---

## 16. Final Rule

Instantly setup is not only uploading leads and pasting copy.

The campaign is ready only when the list, tokens, sequence, schedule, inboxes, safety settings, test emails, and pilot plan all pass review.
