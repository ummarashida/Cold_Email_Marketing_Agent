# Cold Email Marketing Agent - Master Overview

This master file combines the main workflow from the core instruction files:

- [Cold Email Marketing SOP](SOP.md)
- [Data Enrichment](data-enrichment.md)
- [ICP Analysis](ICP.md)
- [Campaign Launch Flowchart](campaign-flowchart.md)
- [Brand Voice & Cold Email Messaging System](Brand-voice.md)
- [B2B Cold Email Service Routing](b2b-cold-email-service-routing.md)
- [Positive Response Lead Report Agent](positive-response-lead-report-agent.md)
- [Support File Index](Support.md)
- [Email Infrastructure Setup](Support/Email-Infrastructure.md)
- [Verification and Suppression Handling](Support/Verification-and-Suppression.md)
- [Email Sequence QA](Support/Email-Sequence-QA.md)
- [Instantly Campaign Setup](Support/Instantly-Setup.md)
- [Monitoring and Reporting](Support/Monitoring-and-Reporting.md)
- [Reply Management](Support/Reply-Management.md)
- [Telegram Notification Setup](Support/Telegram-Notification-Setup.md)
- [Campaign Performance Database](Support/Campaign-Performance-Database.md)
- [Lead Collection](Support/Lead-Collection.md)
- [Segmentation and File QA](Support/Segmentation-and-File-QA.md)

The purpose of this document is to give a clear top-level view of how domain setup, raw prospect data, enrichment, analysis, brand voice, B2B service routing, approval, launch, positive reply handling, monitoring, and reporting work together for Accord Tech Solutions cold email campaigns.

---

## 01. Full Campaign Workflow

Every cold email campaign should follow this order:

```text
Domain and Inbox Setup
Raw Data Collection
Data Enrichment
ICP Analysis
Service Fit Analysis
Pain Point Analysis
Brand Voice Alignment
Email Infrastructure Selection
Email Sequence Writing
Internal Approval
Instantly Campaign Setup
Pilot Campaign Launch
Campaign Monitoring
Positive Reply Handling
Reporting and Optimization
Campaign Closing
```

The campaign should not be launched directly from raw data. The data must be cleaned, enriched, analyzed, matched with the right Accord Tech Solutions service, written in the approved ATS brand voice, checked against the SOP, and approved before launch.

---

## 02. Raw Data Collection Overview

Raw prospect data should be collected based on campaign criteria.

The raw list should match:

- Target industry
- Company size
- Target geography
- Business type
- Decision-maker role
- Service relevance
- ICP criteria

For Accord Tech Solutions, the target geography is:

```text
USA
UK
Canada
```

The goal is to collect prospects that are relevant before enrichment begins.

---

## 03. Data Enrichment Overview

Data enrichment prepares a clean and accurate prospect list for cold email campaigns.

The final enriched file should have:

- No duplicate contacts
- No duplicate companies
- No messy company names
- No generic company emails
- No missing important fields
- Clean prospect information from top to bottom

Important checks include:

- First name and last name check
- Non-English name check
- Invalid name check
- Blank first name check
- Empty email check
- Generic email check
- Duplicate contact check
- Duplicate company check
- Company name cleanup
- Company suffix removal
- Company link removal
- Important field check

Common issue remarks:

```text
First Name Missing
Invalid Name
Non-English Name
Email Missing
Generic Email
Duplicate Contact
Duplicate Company
Company Name Cleaned
Company Suffix Removed
Company Link Removed
Invalid Data
Needs Manual Review
```

If a row has multiple issues, separate remarks with commas.

Example:

```text
Invalid Name, Generic Email, Company Suffix Removed
```

---

## 04. Row-Wise Prospect Analysis Overview

After basic cleaning, each row should be analyzed using the available company and prospect data.

The analysis should identify:

- Business type
- Industry segment
- B2B / B2C status
- Tech / non-tech status
- Sales team status
- Marketing team status
- Possible pain points
- Best Accord Tech Solutions service fit
- Cold email angle
- ICP match
- Data confidence

If something cannot be confirmed, use:

```text
Unknown
Not Found
Not Confirmed
Needs Manual Review
```

Do not guess randomly.

---

## 05. ICP Analysis Overview

ICP means Ideal Customer Profile.

For Accord Tech Solutions, ICP analysis identifies which companies are the best potential customers based on:

- Industry
- Company size
- Geography
- Business type
- Tech / non-tech status
- Team structure
- CRM or data needs
- Sales and marketing needs
- Possible pain points
- Service fit

Preferred company size:

```text
50-200 employees
```

Priority business types:

```text
B2B
Both
```

Target geography:

```text
USA
UK
Canada
```

---

## 06. Strong ICP Industries

Strong ICP industries include:

```text
Software Development
IT Services and IT Consulting
Technology, Information and Internet
Financial Services
Information Services
Health Technology
Business Consulting and Services
Education Administration Programs
Venture Capital / Sustainable Investment
Environmental Services
Interior Design
Architecture / Design Firms
CRM-based Service Businesses
```

These industries are relevant because they often need:

- Lead generation
- Cold email outreach
- Data enrichment
- CRM data management
- Email marketing
- Appointment setting
- Prospect research
- Campaign management
- Portfolio promotion
- Sales pipeline support

---

## 07. Good ICP Signals

A company is a good ICP if it has one or more of these signals:

- 50-200 employees
- Located in or targeting the USA, UK, or Canada
- B2B or both B2B/B2C business model
- Has a sales team
- Has a marketing team
- Has a CRM system
- Uses email marketing
- Uses outbound sales
- Has a portfolio or service-based business
- Works with business clients
- Needs consistent lead generation
- Has a website and active LinkedIn presence
- Has decision-makers available on LinkedIn
- Shows growth or hiring activity
- Uses tools like Studio Designer, Houzz Pro, Ivy, CRM, Klaviyo, or similar platforms

---

## 08. Bad ICP Signals

A company should be low priority or not a match if:

- Outside the target geography with no clear USA, UK, or Canada market fit
- No website found
- No clear business model
- No decision-maker found
- Very small company with no clear budget
- Student project or temporary business
- Irrelevant industry
- No sales or marketing need
- No online presence
- Company information is not clear
- Business appears inactive

---

## 09. ICP Match Score

Each company should receive one ICP match score:

```text
High Match
Medium Match
Low Match
Not a Match
```

Use this logic:

- **High Match:** Relevant industry, 50-200 employees, target geography, B2B or both, clear need for ATS services, and visible decision-makers.
- **Medium Match:** Relevant or semi-relevant company with possible need, but not fully confirmed.
- **Low Match:** Weak fit, unclear budget, or limited service need.
- **Not a Match:** Irrelevant, no clear need, missing important data, or not suitable for ATS services.

---

## 10. Accord Tech Solutions Service Fit

Each prospect should be matched with the most relevant Accord Tech Solutions service.

Possible services:

```text
Cold Email Outreach
B2B Lead Generation
Lead List Building
Data Enrichment
Email Verification
CRM Data Management
Item Listing Support
Appointment Setting Support
Email Marketing Campaign Management
Klaviyo / B2C Email Marketing
LinkedIn Prospect Research
Digital Marketing Support
Website Conversion Support
```

Best format:

```text
Primary ATS Service Fit: Cold Email Outreach
Secondary ATS Service Fit: Lead List Building
```

Do not select too many services for one company.

---

## 11. Pain Point Analysis Overview

Pain points should be realistic, specific, and useful for cold email personalization.

Good pain points include:

```text
Weak outbound lead generation system
No clear cold email outreach process
Low website-to-lead conversion
Weak follow-up system for interested leads
Poor email marketing automation
No visible retention or nurture campaign
Limited social proof or case studies
Unclear sales pipeline process
No clear lead capture system on website
Weak B2B appointment-setting process
Poor customer reactivation process
Weak segmentation for email campaigns
Manual prospecting process
Low visibility in target market
No clear decision-maker targeting strategy
```

Avoid vague pain points like:

```text
Needs marketing
```

Use clear pain points such as:

```text
The company appears to serve B2B clients but does not show a clear outbound lead generation or appointment-setting process.
```

---

## 12. Cold Email Angle Overview

For each prospect, create a short cold email angle based on:

- Industry
- Pain point
- ICP match
- Decision-maker role
- ATS service fit
- Campaign goal

Example:

```text
Helping B2B companies build a cleaner outbound system to reach more decision-makers.
```

Another example:

```text
Helping e-commerce brands improve repeat purchases through better email automation.
```

The angle should be simple, human, and relevant.

---

## 13. Brand Voice and Messaging Overview

Before writing any cold email sequence, the message must follow the ATS brand voice.

ATS should sound:

- Simple
- Human
- Professional
- Helpful
- Direct
- Relevant
- Reply-focused

ATS should not sound like:

- A spammy lead generation vendor
- A hype-heavy digital marketing agency
- A robotic automation tool
- A pushy sales rep
- A company promising overnight results
- A generic agency selling every service to everyone

Every ATS message should:

- Start with the prospect, not ATS
- Focus on one clear pain point
- Use one service angle per email
- Keep the message short and easy to read
- Use a soft CTA
- Avoid hype, spam words, and overpromising
- Create replies before asking for meetings

Core brand rule:

```text
Sound human. Stay relevant. Focus on the prospect. Create replies.
```

The full writing rules, service positioning, CTAs, subject line guidance, examples, and reply handling voice are defined in:

```text
Brand-voice.md
```

---

## 14. B2B Cold Email Service Routing Overview

The B2B cold email service routing file defines how ATS should position cold email as a service and how the agent should route requests around service scope.

The agent should use this file when deciding:

- Whether the request is about B2B cold outreach
- Which service tier fits the situation
- Whether the campaign should focus on meetings, replies, pipeline, or deliverability
- Whether the request is out of scope
- Which tools and service approach should be recommended

Core B2B cold email rules:

- Lead with outcomes, not email volume
- Focus on booked meetings, replies, and pipeline opportunities
- Use secondary sending domains, not the primary domain
- Avoid spray-and-pray outreach
- Use signal-based personalization
- Keep cold emails short, plain text, and reply-focused
- Avoid buying unverified lists
- Protect sender reputation and deliverability

The full routing and service context is defined in:

```text
b2b-cold-email-service-routing.md
```

---

## 15. SOP and Email Infrastructure Overview

Before campaign setup, the SOP must be followed for domain, inbox, DNS, tracking, warmup, sending limit, upload, QA, launch, monitoring, and reporting requirements.

The full operational process is defined in:

```text
SOP.md
```

Email infrastructure must be checked before launch.

Review:

- Available domains
- Available mailboxes
- Mailboxes already being used
- Mailboxes that should not be used
- Healthy mailboxes
- Mailboxes with deliverability issues
- Mailboxes suitable for the new campaign
- SPF, DKIM, DMARC, and CNAME status
- Custom tracking domain status
- Warmup status
- Campaign sending limits

Only approved and healthy sending accounts should be used.

---

## 16. Email Sequence Overview

The email sequence should be written after the service angle and pain points are confirmed.

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
- Subject lines
- A/B variations if needed

Before finalizing, confirm:

- The email is under 110 words where possible
- The first line is relevant
- The CTA is soft and easy to answer
- The message avoids spammy phrases
- The email does not ask for a meeting too early
- The prospect's pain comes before the ATS service introduction

---

## 17. Internal Approval Overview

Before launch, the final campaign plan must be approved by the CEO and ED.

Approval should cover:

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

The campaign should not launch until the sequence, target service, prospect list, brand voice alignment, infrastructure, and SOP launch readiness are approved.

---

## 18. Instantly Campaign Setup Overview

After approval, the campaign should be set up in Instantly or the approved campaign platform.

Setup should include:

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
- Reviewing at least 20 custom openers
- Testing all links and UTMs
- Launching a 10-15% pilot batch first

---

## 19. Positive Reply Handling Overview

When a campaign gets a positive reply, the positive-response lead report agent should be used.

The agent should:

- Stop the sequence immediately for that lead
- Classify the reply as positive, neutral, negative, out-of-office, wrong person, or unsubscribe
- Build a one-page company and person portfolio
- Report which campaign, sequence step, subject, and body earned the reply
- Analyze the prospect's intent
- Draft 2-3 response variants
- Send or prepare a Telegram notification
- Mark unverifiable fields as `unknown`
- Escalate low-confidence classification for human review

Positive reply handling must use verified list data and enrichment only. The agent must never invent company or person facts.

The full process is defined in:

```text
positive-response-lead-report-agent.md
```

---

## 20. Final Output Columns

The final enriched and analyzed campaign file should include:

```text
Company Name
Personal LinkedIn URL
Email
First Name
Last Name
Job Title
Company Website
Company Domain
Location
Industry
Company Size
Geography
Industry Segment
B2B / B2C
Business Type
Tech / Non-Tech
Sales Team Status
Marketing Team Status
Decision Maker Availability
Main Pain Point
Secondary Pain Point
Primary ATS Service Fit
Secondary ATS Service Fit
Service Fit Reason
Cold Email Angle
Personalization Note
Brand Voice Check
ICP Match
ICP Match Reason
Data Confidence
Remarks
```

---

## 21. Final Campaign Launch Checklist

Before launching, confirm:

- Raw data collected properly
- Data enrichment completed
- Duplicate contacts removed or marked
- Duplicate companies removed or marked
- Generic emails removed or marked
- ICP analysis completed
- Target geography checked
- Pain points identified
- ATS service fit confirmed
- Brand voice alignment checked
- Email infrastructure selected
- Sequence written
- Personalization fallback tested
- 20+ random opener rows reviewed
- Links and UTMs tested
- CEO and ED approval received
- Instantly campaign setup completed
- Pilot batch plan confirmed
- Test email checked
- Campaign settings reviewed
- Suppression list process ready
- Monitoring and reporting process ready

---

## 22. Monitoring and Post-Launch Overview

After launch, the campaign must be monitored according to the SOP.

Track:

- Open rate
- Reply rate
- Positive reply rate
- Bounce rate
- Spam complaints
- Unsubscribes
- Meetings booked
- Performance by segment
- Performance by inbox
- Performance by campaign step
- Positive reply source sequence
- Booked meeting opportunity

Key thresholds:

```text
Open rate goal: 60%+
Reply rate goal: 3%+
Bounce rate limit: below 2%
Complaint rate limit before scaling: below 0.1%
```

Pause the campaign if bounce rate rises, spam complaints increase, open rate drops suddenly, wrong leads are uploaded, personalization errors appear, or one inbox starts performing badly.

Only scale after the pilot batch performs well and inbox health remains stable.

---

## 23. Final Rule

Every campaign should move through the full process:

```text
Setup Infrastructure -> Collect -> Clean -> Enrich -> Analyze -> Match -> Route Service -> Align Voice -> Write -> QA -> Approve -> Setup -> Pilot Launch -> Monitor -> Handle Positive Replies -> Scale -> Report -> Close
```

The final output should clearly show:

```text
Who the company is
What type of business they are
Whether they match the ICP
What pain point they may have
Which ATS service fits them best
What cold email angle should be used
Whether the message follows the ATS brand voice
Which B2B cold email service route applies
Which sequence step created any positive reply
Whether they are ready for campaign launch
```

If data is missing or unclear, use:

```text
Unknown
Not Found
Not Confirmed
Needs Manual Review
```

Do not guess randomly. Use available data, company website, LinkedIn, industry, business model, geography, and public information to make the best possible analysis.
