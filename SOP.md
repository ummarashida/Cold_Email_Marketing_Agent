# Cold Email Marketing SOP

## Standard Operating Procedure

This SOP defines the operational process for Accord Tech Solutions cold email campaigns, from domain setup and lead collection to campaign launch, monitoring, reporting, and closing.

---

## 1. Domain Setup

### 1.1 Domain Buying

Approved domain buying platforms include:

- Namecheap
- Hostinger
- Google Domains
- Other approved domain providers

Before purchasing any domain, take approval from the CEO and ED by email.

### 1.2 Technical DNS Setup

Add and verify the following DNS records:

- SPF
- DKIM
- DMARC
- CNAME

Use these tools to check setup:

- DKIM Checker: <https://mxtoolbox.com/dkim.aspx>
- DMARC Checker: <https://mxtoolbox.com/>
- SPF Checker: <https://mxtoolbox.com/spf.aspx>

Current process:

If inboxes are bought from resellers, the team mainly focuses on adding each persona's image to their assigned mailbox. In that case, step 1.2 may be skipped based on reseller setup.

### 1.3 Domain Redirect

Set the domain redirect to:

```text
https://accordtechsolutions.com
```

Use this redirect for each sending domain.

### 1.4 Mailbox Creation Per Domain

Create a maximum of 3-4 mailboxes per domain when buying inboxes from resellers.

For Hostinger-based email setup, create 2-5 inboxes per domain.

### 1.5 Custom Tracking Domain Setup

Custom tracking domain format:

```text
inst.companydomain
```

Example:

```text
inst.accordtechsolutions.space
```

Hostinger setup:

1. Log in to Hostinger.
2. Go to Domains.
3. Select the domain.
4. Go to DNS Zone.
5. Add a new CNAME record.
6. Use these values:

```text
Type: CNAME
Name / Host: inst
Value / Points to: prox.itrackly.com
TTL: 300 or default
```

Instantly setup:

1. Go to Instantly.
2. Click Email Accounts.
3. Click each inbox.
4. Go to Settings.
5. Open Custom Tracking Domain.
6. Paste the custom tracking domain.
7. Click Verify or Auto Check.
8. Confirm the domain shows as verified.

### 1.6 Add Inboxes to Instantly

After completing the setup:

1. Create all inboxes in Hostinger.
2. Organize them in a file sequentially.
3. Download the file in CSV format.
4. Go to Instantly.
5. Open Email Accounts.
6. Click Add New.
7. Select Connect Existing Account.
8. Select Any Provider.
9. Upload the CSV.

### 1.7 Inbox Warmup and Sending Settings

For each inbox in Instantly:

1. Enable warmup.
2. Go to Settings.
3. Open Sender Information and Signature.
4. Set campaign limit to:

```text
10
```

5. Set minimum wait time to:

```text
30 minutes
```

6. Set custom tracking domain.
7. Set warmup per day to:

```text
25
```

8. Save settings.

Update the Email Infrastructure Tracker after setup.

Tracker:

<https://docs.google.com/spreadsheets/d/1SX_4BR47A7bT7KxrOKRQ7AkKHWPVNuiJZUGoxTUuyO4/edit?gid=922694498#gid=922694498>

### 1.8 Hostinger Email Setup Note

If emails are created directly from Hostinger, always follow the technical setup process in step 1.2.

Current update:

The team currently creates mailboxes from resellers in many cases.

### 1.9 DKIM Check

In Hostinger:

1. Go to Dashboard.
2. Select the domain.
3. Click Manage.
4. Go to DNS Zone.
5. Search for:

```text
DKIM
```

Expected name:

```text
default._domainkey
```

If the DKIM TXT value is found, DKIM is already set.

### 1.10 Previous DMARC Setting

Previous DMARC record:

```text
Name: _dmarc
Type: TXT
Value: v=DMARC1; p=none; rua=mailto:dmarc@yourdomain.com
```

This was found to have a higher chance of hard bounces.

### 1.11 Updated DMARC Setting

Safer DMARC setting identified by the email marketing team:

```text
Name: _dmarc
Type: TXT
Value: "v=DMARC1; p=none; rua=mailto:name@accordtechbd.com; ruf=mailto:wasiqur.rahman@accordtechbd.com; fo=1"
```

### 1.12 DMARC Update 2.0

Alternative DMARC setting:

```text
v=DMARC1; p=reject; pct=100; rua=mailto:reports@inboxsetup.com; ruf=mailto:reports@inboxsetup.com; ri=604800; aspf=s; adkim=s
```

### 1.13 SPF Settings

Hostinger and Instantly SPF:

```text
"v=spf1 include:_spf.mail.hostinger.com include:spf.instantly.ai ~all"
```

Google SPF:

```text
v=spf1 include:_spf.google.com ~all
```

After SPF, DKIM, and DMARC setup, follow:

```text
1.3 -> 1.5 -> 1.6 -> 1.7
```

---

## 2. Lead Data Collection and Verification

### 2.1 Data Sources

The market research team provides Apollo source links.

Typical Apollo filters:

- Email status: Verified
- Location
- Job title: Owner, Founder, C-Suite
- Employee size: 50-200
- Targeted keywords

Process:

1. Market research team provides Apollo source links to the coding team.
2. Coding team runs the Apollo bot, SEO bot, and Google bot.
3. Coding team collects as much data as possible from the source list.
4. Coding team submits the list back to the market research team.
5. Market research team finds and verifies emails.

Bot run tools:

- Python
- VS Code
- ChromeDriver
- VPN

### 2.2 Bot Output Fields

| SEO Bot | Google Bot | Apollo Bot | Market Research Team |
|---|---|---|---|
| Final_URL | Search_Query | Company Name | Corporate Emails |
| Status_Code | GMB_Name | Domain | Personal Emails |
| Fetch_ms | Rating | Address | Other Source |
| Page_Title | Reviews_Number | Country | Source Link |
| Title_Length | Reputation Notes | Number of Employees |  |
| Meta_Description | Specialty | Industry |  |
| Meta_Description_Length | GMB_Link | Founded Year |  |
| Robots_Meta | Website_Link | Phone Number |  |
| X_Robots_Tag | Website_Status | First Name |  |
| Canonical_URL |  | Last Name |  |
| Canonical_Status |  | Job Title |  |
| H1_Texts |  | LinkedIn |  |
| H1_Count |  | LinkedIn About Us |  |
| Images_Count |  | Person LinkedIn |  |
| Images_Missing_Alt |  |  |  |
| Images_Alt_Coverage |  |  |  |
| Links_Internal |  |  |  |
| Links_External |  |  |  |
| HTML_Lang |  |  |  |
| Word_Count |  |  |  |
| Content_Size_Bytes |  |  |  |
| Schema_Status |  |  |  |
| Schema_Count |  |  |  |
| Schema_Types |  |  |  |
| Schema_Points |  |  |  |
| SEO Offer |  |  |  |
| Explanation |  |  |  |

### 2.3 Email Verification

Use one or more of these tools:

- Debounce
- NeverBounce
- ZeroBounce
- Platform-built-in verifier

Remove or separate:

- Invalid emails
- Duplicate emails
- Generic emails
- Risky verification results
- Unknown verification results

Generic email examples:

- info@
- admin@
- sales@
- support@
- it@

Risky and unknown emails should be moved to a quarantine tab.

Goal:

```text
Bounce rate below 2%
```

### 2.4 Suppression List

Create and maintain a centralized suppression list so contacts who unsubscribe or request removal are permanently excluded from future campaigns.

Purpose:

- Maintain compliance
- Protect sender reputation
- Avoid contacting removed prospects again

Suppression list:

<https://docs.google.com/spreadsheets/d/1Fplns4qU3NH3HD23g9mqsFaTO_RCEV2so4d7KoVnTSg/edit?gid=0#gid=0>

---

## 3. Lead Segmentation and File Preparation

Segment leads by:

- Industry
- Role or title
- Company size
- Geography
- Custom tags
- Founded year
- Annual revenue
- SEO issue
- Reputation management need
- Website issue
- No website status

Example segments:

- HVAC
- Portfolio
- SaaS
- E-commerce
- Healthcare
- Retail
- Restaurants
- Real estate

### 3.1 ICP Match Verification

Before finalizing any segmented list, every record must pass an ICP match check.

Check:

- First name
- Email quality
- No generic or role-based emails
- LinkedIn employee profile
- HQ location
- City, state, and country
- Pain point identification

After the ICP check, take approval from the CEO and ED before finalizing the file.

### 3.2 Primary Segmentation

Assign each lead to one primary segment.

### 3.3 Drive Upload

After segmentation, upload the separated files to the approved Drive folder.

---

## 4. Download Segmented List in CSV Format

### 4.1 Blank Column Check

Before CSV export, confirm:

- No blank emails are included.
- Names are capitalized properly.
- All required fields contain correct information.
- No blank required columns remain.

### 4.2 Company Name Normalization

Company names should not contain unnecessary suffixes such as:

- Inc
- LLC
- Ltd
- Co.
- Company

Export removed duplicates to a separate log file for audit purposes.

---

## 5. Email Writing and Sequences

### 5.1 Prompt Creation Before Script Writing

Before writing the sequence, create a prompt to guide the sequence.

After the prompt is ready, discuss it with the full team.

### 5.2 Subject Line Rules

Subject lines should be:

- Personalized according to segment fields
- Short
- Natural and relevant
- Low-pressure
- Not clickbait
- Different for each step
- Not repeated in the body

Example:

```text
Found friction on {{companyName}} website
```

### 5.3 Email Body Rules

Subject length:

```text
3-5 words
```

Body length:

```text
3-5 lines
55-70 words
Under 20 seconds reading time
Plain text
Clear soft CTA
```

Sequence structure:

- First email
- 2 follow-ups
- 1 breakup email

Follow-up duration:

```text
3-5 days
```

Do not use:

- Quick Question as a subject line
- FREE!!!
- 100% guaranteed
- Spammy language
- Clickbait subject lines
- Hard meeting CTAs in the first email

Always include a polite opt-out line when required.

Meeting CTAs should only be used after the prospect shows interest. The first email should aim to create a reply, not force a booked call.

Once the sequence is ready, create a PDF for prospects who respond.

### 5.4 Personalization Token Fallback Rules

All personalization tokens must have predefined fallback values.

Rules:

- If `{{FirstName}}` is blank, use `there`.
- If `{{CompanyName}}` is blank, use `your company`.
- If any required token is missing, use a neutral alternative.

All campaigns must be tested before launch to confirm fallback values render correctly.

### 5.5 Custom Opener QA Check

Before launch, manually review at least 20 random rows to verify:

- Opener accuracy
- Correct personalization mapping
- Contextual relevance

### 5.6 Link and UTM QA

Test every URL and UTM before launch.

The campaign should proceed only after QA confirmation.

### 5.7 Segment-Specific Script Requirement

Create a separate email script for each target segment.

Do not use one generic template across multiple segments.

---

## 6. Uploading Leads to Email Platform

Approved tools include:

- Instantly
- Mailchimp
- Brevo
- Other approved email platforms

### 6.1 Upload CSV and Map Columns

In the email platform:

1. Go to Campaigns.
2. Add leads.
3. Upload the CSV.
4. Map columns correctly.

Example mapping:

```text
{{firstName}} -> First Name
{{companyName}} -> Company Name
{{industry}} -> Industry
```

### 6.2 Sending Limit for Multiple Contacts Per Company

When sending to multiple contacts from the same company, set the campaign to send only:

```text
2-3 emails per day per company
```

### 6.3 Add Sequence and Configure Campaign

Instantly setup checklist:

- Add 3-4 sequence steps.
- Set how often emails are sent.
- Avoid Monday AM and Friday PM schedules.
- Select accounts to use.
- Enable stop sending emails on reply.
- Enable open tracking.
- Add daily sending limit.
- Insert unsubscribe link/header.
- Test unsubscribe setup.
- Launch only after checks pass.

For multiple contacts:

- Add 4 sequence steps.
- Set daily sending limit to 2-3 per company.
- Confirm stop-on-reply is enabled.
- Confirm unsubscribe setup works.

### 6.4 Pilot Batch Launch

Start with:

```text
10-15% of the list
```

Review performance before scaling.

---

## 7. Campaign Execution and Monitoring

### 7.1 Monitor After Launch

Monitor:

- Open rate
- Reply rate
- Bounce rate
- Spam complaints

Targets:

```text
Open rate: 60%+
Reply rate: 3%+
Bounce rate: below 2%
Spam complaints: below 1
```

Respond to replies quickly and update CRM or platform tags.

Pause and troubleshoot if opens or deliverability drop significantly.

### 7.2 Scale-Up Criteria

Increase sending volume only if:

- Bounce rate stays below 2%.
- Complaint rate stays below 0.1%.

Do not scale unless both conditions are consistently maintained.

---

## 8. Reporting and Optimization

Track:

- Open rates
- Reply rates
- Bounce rates
- Unsubscribes
- Positive replies
- Booked calls or meetings

Optimization process:

- Run A/B tests on subject lines and CTAs.
- Review best and worst performing segments.
- Review best and worst performing days.
- Review best and worst performing templates.
- Log campaign results.
- Adjust messaging.
- Clean the list after each campaign.
- Keep inboxes warm between campaigns.

Resources:

- Inbox setup and Instantly settings: <https://drive.google.com/drive/u/0/folders/1Ha3QN9Owd7A2I-lgSqloWy46nsTtYIyt>
- Campaign setup Instantly SOP: <https://drive.google.com/drive/u/0/folders/1SOklLQcpElIIVSB8K8O06FzFskuzZ2vX>

---

## 9. Campaign Management, Monitoring, and Post-Launch Process

### 9.1 After Launch Check

After launch, check:

- All selected inboxes are active.
- Sequence mapping works correctly.
- Sending schedule is running.
- Stop-on-reply is turned on and works correctly.
- Unsubscribe option works.
- Emails are going out correctly.

If any major issue is found, pause the campaign and fix it first.

### 9.2 First 3 Days Monitoring

For the first 3 days, check the campaign carefully every day.

Review:

- Sent emails
- Bounce rate
- Open rate
- Reply rate
- Unsubscribe or spam complaints
- Inbox performance
- Personalization errors

This catches problems early before they affect the full campaign.

### 9.3 Reply Management

Check replies daily and sort them properly.

Main reply types:

- Interested
- Not interested
- Unsubscribe / remove me
- Wrong person
- Out of office
- Auto reply

Actions:

| Reply Type | Action |
|---|---|
| Interested | Move to sales follow-up |
| Not interested | Add to suppression list if needed |
| Unsubscribe / remove me | Add to suppression list immediately |
| Wrong person / referral | Update contact if useful |
| Out of office | Follow up later if needed |
| Auto reply | Review and tag correctly |

### 9.4 Daily Performance Review

Review campaign performance every day.

Track:

- Total sent
- Delivered
- Bounced
- Opened
- Replied
- Positive replies
- Negative replies
- Unsubscribes
- Meetings booked

Also check performance by:

- Segment
- Lead source
- Inbox
- Campaign step

### 9.5 When to Pause

Pause the campaign or affected inboxes if:

- Bounce rate goes above the limit.
- Spam complaints increase.
- Open rate drops suddenly.
- Wrong leads were uploaded.
- Personalization errors are found.
- One inbox starts performing badly.

Do not continue sending until the issue is checked and fixed.

### 9.6 When to Scale

Only scale the campaign when:

- Pilot batch performs well.
- Bounce rate stays below 2%.
- Complaint rate stays very low.
- Replies are relevant.
- Inboxes are stable.

Increase sending slowly.

### 9.7 Weekly Review

Each week, review:

- Best subject lines
- Best-performing segments
- Weak segments
- Bounce reasons
- Negative reply reasons
- Unsubscribe reasons
- Follow-up performance

Use this review to improve future campaigns.

### 9.8 Campaign Closing

When the campaign ends:

- Export the final full report.
- Record key results.
- Update the suppression list.
- Remove bad leads from future use.
- Note the best and worst-performing scripts.
- Note the best and worst-performing segments.
- Keep inboxes warm after campaign end.

Operational note:

This process helps ATS manage campaigns after launch, respond quickly to issues, protect inbox health, improve results over time, and run each campaign in an organized way.

---

## Final SOP Rule

Every campaign must move through:

```text
Domain Setup -> Lead Collection -> Verification -> Segmentation -> ICP Check -> File Preparation -> Email Writing -> QA -> Upload -> Pilot Launch -> Monitor -> Scale -> Report -> Close
```

Do not launch a campaign until the list, infrastructure, copy, tracking, unsubscribe setup, and approval steps are complete.

---

## SOP Coverage Audit

This section shows which SOP requirements are already covered by the current `.md` files and which supporting files may be useful to create later.

Current approved files:

- `SOP.md`
- `Master.md`
- `Brand-voice.md`
- `b2b-cold-email-service-routing.md`
- `data-enrichment.md`
- `ICP.md`
- `campaign-flowchart.md`
- `positive-response-lead-report-agent.md`

### Already Covered in Current Files

| SOP Area | Current Coverage | File |
|---|---|---|
| Full cold email operating process | Covered | `SOP.md` |
| Overall campaign workflow | Covered | `Master.md`, `campaign-flowchart.md` |
| B2B cold email service positioning and routing | Covered | `b2b-cold-email-service-routing.md`, `Master.md` |
| Data cleaning and enrichment | Covered | `data-enrichment.md`, `SOP.md` |
| ICP analysis and scoring | Covered | `ICP.md`, `Master.md`, `SOP.md` |
| Employee size rule | Covered as 50-200 employees | `SOP.md`, `ICP.md`, `Master.md` |
| Brand voice and cold email style | Covered | `Brand-voice.md`, `SOP.md` |
| Subject line and CTA rules | Covered | `Brand-voice.md`, `SOP.md` |
| Email verification and generic email removal | Covered at SOP level | `SOP.md`, `data-enrichment.md` |
| Suppression list process | Covered at SOP level | `SOP.md` |
| Segmentation and file preparation | Covered at SOP level | `SOP.md`, `Master.md` |
| Instantly campaign setup | Covered at SOP level | `SOP.md`, `campaign-flowchart.md` |
| Pilot launch rule | Covered | `SOP.md`, `Master.md`, `campaign-flowchart.md` |
| Monitoring, pause, and scale rules | Covered | `SOP.md`, `Master.md`, `campaign-flowchart.md` |
| Reply management categories | Covered at SOP level | `SOP.md`, `Brand-voice.md` |
| Positive reply lead report and response variants | Covered | `positive-response-lead-report-agent.md`, `Master.md` |
| Reporting and campaign closing | Covered at SOP level | `SOP.md` |

### Areas That Are Covered but Could Be Stronger

The current files are enough for a working agent. The SOP, Master, ICP, data enrichment, brand voice, B2B service routing, campaign flowchart, and positive-response agent now cover the main campaign process.

Some SOP areas are still broad inside `SOP.md`. For a stronger agent, these areas may need separate detailed files later:

- Email infrastructure setup
- Lead collection process
- Email verification and suppression handling
- Segmentation and file QA
- Email sequence QA
- Instantly campaign setup
- Monitoring and reporting
- Full reply management for all reply types, not only positive replies

### Current Coverage Summary

| Current File | What It Covers for the SOP | Status |
|---|---|---|
| `SOP.md` | Main operational process from domain setup to campaign closing | Core file ready |
| `Master.md` | Top-level workflow and how all instruction files connect | Core file ready |
| `Brand-voice.md` | Email tone, CTAs, subject lines, service positioning, reply style | Core file ready |
| `b2b-cold-email-service-routing.md` | B2B cold email service scope, service tiers, deliverability-safe positioning, tool stack | Core file ready |
| `data-enrichment.md` | Data cleaning, duplicate checks, generic emails, company cleanup, row-wise analysis | Core file ready |
| `ICP.md` | ICP logic, geography, company size, business type, service fit, match scoring | Core file ready |
| `campaign-flowchart.md` | Campaign step-by-step flow from setup to launch and monitoring | Core file ready |
| `positive-response-lead-report-agent.md` | Positive reply detection, portfolio building, sequence attribution, response variants, Telegram reporting | Core file ready |

### Suggested Future `.md` Files

Do not create these files unless approved by the user.

Recommended files:

1. `Email-Infrastructure.md`
   - For domain buying, DNS setup, SPF, DKIM, DMARC, CNAME, custom tracking domain, inbox warmup, and sending limits.

2. `Lead-Collection.md`
   - For Apollo filters, bot sources, coding team process, market research handoff, and raw data field requirements.

3. `Verification-and-Suppression.md`
   - For email verifier rules, invalid/risky/unknown handling, generic email removal, duplicate logs, bounce target, and suppression list updates.

4. `Segmentation-and-File-QA.md`
   - For segment rules, ICP gate, CSV export checks, blank field checks, company name cleanup, and approval before upload.

5. `Email-Sequence-QA.md`
   - For subject line checks, body length, fallback tokens, opener QA, link/UTM QA, segment-specific copy, and final copy approval.

6. `Instantly-Setup.md`
   - For uploading CSVs, mapping fields, adding sequences, schedules, stop-on-reply, unsubscribe settings, test emails, and pilot launch setup.

7. `Monitoring-and-Reporting.md`
   - For first 3 days monitoring, daily metrics, pause rules, scale rules, weekly reviews, final reporting, and campaign closing.

8. `Reply-Management.md`
   - For all reply types, including interested, pricing, unsubscribe, wrong person, referral, out-of-office, auto-reply, negative replies, and suppression actions.

9. `Telegram-Notification-Setup.md`
   - For Telegram bot token, chat ID, alert format, notification routing, and positive reply alert testing.

10. `Campaign-Performance-Database.md`
   - For storing winning sequences, winning steps, reply reasons, positive reply source, meetings booked, and campaign learning history.

### Priority Order for Future File Creation

If only a few files are created first, use this order:

1. `Email-Infrastructure.md`
2. `Verification-and-Suppression.md`
3. `Email-Sequence-QA.md`
4. `Instantly-Setup.md`
5. `Monitoring-and-Reporting.md`
6. `Reply-Management.md`
7. `Telegram-Notification-Setup.md`
8. `Campaign-Performance-Database.md`
9. `Lead-Collection.md`
10. `Segmentation-and-File-QA.md`

### Final Audit Rule

The current SOP is usable now. The suggested files are optional support files that would make the agent more detailed, safer, and easier to control.

No new `.md` file should be created unless the user gives clear permission.
