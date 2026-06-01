# Campaign Launch Flowchart

## 01. Domain and Inbox Setup

Before collecting or uploading campaign data, confirm the campaign has approved sending infrastructure.

Check:

- Domain approval received
- SPF, DKIM, DMARC, and CNAME configured
- Custom tracking domain verified
- Inboxes created and active
- Warmup enabled
- Sending limits configured
- Email Infrastructure Tracker updated

Use the full process in:

```text
SOP.md
```

---

## 02. Raw Data Collection

Before launching any cold email campaign, the first step is to collect raw prospect data based on our campaign criteria.

The raw data should match our target requirements, such as:

- Target industry
- Company size
- Location
- Business type
- Decision-maker role
- Service relevance
- ICP criteria
- Employee size of 50-200 where applicable

The goal is to collect a prospect list that is relevant to the campaign objective.

---

## 03. Data Enrichment

After collecting the raw data, the full file must be processed under the Data Enrichment workflow.

During this stage, the prospect list should be cleaned, checked, and enriched.

This includes:

- Removing duplicate contacts
- Removing duplicate companies
- Checking first name and last name quality
- Finding missing data
- Removing generic emails
- Cleaning company names
- Checking company domains
- Checking LinkedIn profiles
- Identifying B2B / B2C status
- Identifying tech / non-tech status
- Finding industry segment
- Finding company pain points
- Finding the best ATS service fit

The final enriched file should be clean, accurate, and ready for campaign analysis.

---

## 04. Verification, Suppression, and File QA

Before campaign writing or upload, verify the list and remove risky records.

Check:

- Invalid emails removed
- Risky and unknown emails moved to quarantine
- Generic emails removed or marked
- Duplicate contacts removed
- Duplicate companies handled
- Suppression list checked
- CSV file has no blank required fields

Use:

```text
SOP.md
data-enrichment.md
```

---

## 05. Email Infrastructure Selection

Before campaign setup, we need to check our email infrastructure.

We need to identify:

- Which domains are available
- Which mailboxes are available
- Which mailboxes are already being used
- Which mailboxes should not be used
- Which mailboxes are healthy
- Which mailboxes have deliverability issues
- Which mailboxes are suitable for the new campaign

After checking everything, we need to select the best available email accounts for the campaign.

---

## 06. Campaign Service Fit Analysis

After data enrichment, we need to analyze which Accord Tech Solutions service is the best fit for the prospect list.

We should review the companies in the list and identify:

- What type of companies they are
- What industry they belong to
- What pain points they may have
- Which service they are most likely to respond to
- Whether the campaign should focus on cold email outreach, lead generation, data enrichment, CRM support, email marketing, or another ATS service

The goal is to choose the most relevant service angle before writing the email sequence.

---

## 07. Pain Point Analysis

Based on the enriched data, we need to identify the main pain points of the target companies.

The pain points should be connected to the selected ATS service.

Example:

If the target companies are B2B service companies, possible pain points may be:

- Weak outbound lead generation
- No clear follow-up system
- Low appointment booking rate
- Manual prospecting process
- Poor CRM data quality
- No consistent email outreach process

If the target companies are B2C brands, possible pain points may be:

- Weak customer retention
- No proper email automation
- Low repeat purchase rate
- No customer reactivation flow
- Poor email segmentation

---

## 08. Brand Voice Alignment

Before writing or approving the email sequence, confirm the campaign follows the ATS brand voice.

The message should be:

- Simple
- Human
- Professional
- Relevant
- Reply-focused
- Focused on one pain point
- Focused on one service angle
- Built around a soft CTA

Avoid:

- Clickbait subject lines
- Spammy wording
- Overpromising
- Hard meeting CTAs in the first email
- Generic compliments

Use the full guide in:

```text
Brand-voice.md
SOP.md
```

---

## 09. Email Sequence Writing

After selecting the service angle and identifying the pain points, the email sequence should be written.

The sequence should be based on:

- Target industry
- Prospect pain points
- ATS service fit
- ICP match
- Decision-maker role
- Campaign goal

The email copy should be:

- Short
- Clear
- Human-sounding
- Relevant to the prospect
- Focused on one main pain point
- Focused on one clear service offer
- Written for replies, not just opens
- Aligned with the ATS brand voice

The sequence should include:

- Step 1 email
- Step 2 follow-up
- Step 3 follow-up
- Breakup email if needed
- Subject lines
- A/B variations if needed
- Token fallback checks
- Opener QA
- Link and UTM QA

---

## 10. Internal Approval

Before launching the campaign, the final campaign plan must be approved by the CEO and ED.

Approval should be taken for:

- Prospect list quality
- ICP match
- Target industry
- Selected ATS service
- Pain point angle
- Email sequence
- Brand voice alignment
- Subject lines
- Campaign strategy
- Sending infrastructure
- SOP launch readiness

The campaign should not be launched until the sequence, target service, prospect list, infrastructure, brand voice alignment, and SOP readiness are approved.

---

## 11. Instantly Campaign Setup

After approval, the campaign should be set up in Instantly.

The setup process should include:

- Creating a new campaign
- Uploading the final enriched prospect list
- Mapping all required fields correctly
- Adding the approved email sequence
- Adding subject lines and variations
- Selecting the approved sending accounts
- Setting daily sending limits
- Setting schedule and timezone
- Checking unsubscribe settings
- Checking tracking settings
- Checking campaign safety settings
- Testing the campaign before launch
- Testing personalization token fallbacks
- Testing links and UTMs
- Confirming unsubscribe setup

---

## 12. Pilot Launch

Start with:

```text
10-15% of the list
```

Review the pilot before scaling.

Scale only if:

- Bounce rate stays below 2%
- Complaint rate stays below 0.1%
- Replies are relevant
- Inboxes remain stable

---

## 13. Monitoring and Reporting

After launch, monitor:

- Open rate
- Reply rate
- Positive replies
- Bounce rate
- Spam complaints
- Unsubscribes
- Meetings booked
- Segment performance
- Inbox performance
- Campaign step performance

Use:

```text
SOP.md
Brand-voice.md
```

---

## 14. Final Campaign Launch Checklist

Before launching, check:

- Raw data collected properly
- Data enrichment completed
- Duplicate contacts removed or marked
- Generic emails removed or marked
- ICP analysis completed
- Pain points identified
- ATS service fit confirmed
- Brand voice alignment checked
- Email infrastructure selected
- Sequence written
- Personalization fallback tested
- 20+ custom openers reviewed
- Links and UTMs tested
- CEO and ED approval received
- Instantly campaign setup completed
- Pilot batch plan confirmed
- Test email checked
- Campaign settings reviewed
- Suppression list checked
- Monitoring process ready

---

## 15. Final Instruction

Every cold email campaign must follow this process step by step.

The campaign should not be launched only with raw data.

First, the infrastructure must be ready. Then the prospect list must be collected, enriched, verified, analyzed, matched with the correct ATS service, connected with the right pain points, written in the ATS brand voice, checked through QA, and approved internally.

Only after completing these steps should the campaign be set up, pilot-launched, monitored, scaled, reported, and closed.
