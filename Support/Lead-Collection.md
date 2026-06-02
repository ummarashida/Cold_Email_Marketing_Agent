# Lead Collection

## Purpose

This file defines how Accord Tech Solutions collects raw lead data before cleaning, enrichment, verification, segmentation, ICP analysis, and campaign setup.

Use this file for Apollo source links, bot output requirements, market research handoff, coding team handoff, and raw data quality standards.

---

## 01. Main Goal

The goal of lead collection is to gather relevant raw prospects that match the campaign ICP before enrichment begins.

Lead collection should support:

- Target industry
- Target geography
- Target role
- Company size
- Service fit
- Campaign angle
- Verification readiness
- Segmentation readiness

Raw data should never be treated as campaign-ready.

---

## 02. Approved Data Sources

Common sources:

- Apollo
- Company websites
- LinkedIn
- Google search
- Google Business Profile
- SEO bot output
- Market research team sources
- Other approved source links

The market research team usually provides Apollo source links.

---

## 03. Standard Apollo Filters

Typical Apollo filters:

```text
Email status: Verified
Location: USA, UK, Canada, or campaign-specific geography
Job title: Owner, Founder, C-Suite, senior decision-maker
Employee size: 50-200
Targeted keywords: campaign-specific
```

Use titles based on the campaign goal.

Examples:

```text
Founder
CEO
Owner
President
CMO
VP Marketing
Head of Sales
Growth Lead
Operations Lead
Business Development
```

---

## 04. Team Handoff Process

Standard process:

1. Market research team provides Apollo source links to the coding team.
2. Coding team runs the Apollo bot, SEO bot, and Google bot.
3. Coding team collects as much relevant data as possible from the source list.
4. Coding team submits the raw list back to the market research team.
5. Market research team finds and verifies emails.
6. The list moves to cleaning, enrichment, verification, suppression, and ICP review.

Do not skip the verification and suppression stage.

---

## 05. Bot Run Tools

Approved tools:

- Python
- VS Code
- ChromeDriver
- VPN

Bot output should be stored in a clean file and labeled by source, date, and segment.

---

## 06. Required Apollo Bot Fields

Apollo bot output may include:

```text
Company Name
Domain
Address
Country
Number of Employees
Industry
Founded Year
Phone Number
First Name
Last Name
Job Title
LinkedIn
LinkedIn About Us
Person LinkedIn
Source Link
```

Missing values should be marked as:

```text
Not Found
```

---

## 07. Required SEO Bot Fields

SEO bot output may include:

```text
Final_URL
Status_Code
Fetch_ms
Page_Title
Title_Length
Meta_Description
Meta_Description_Length
Robots_Meta
X_Robots_Tag
Canonical_URL
Canonical_Status
H1_Texts
H1_Count
Images_Count
Images_Missing_Alt
Images_Alt_Coverage
Links_Internal
Links_External
HTML_Lang
Word_Count
Content_Size_Bytes
Schema_Status
Schema_Count
Schema_Types
Schema_Points
SEO Offer
Explanation
```

Use SEO output for website issue campaigns, SEO campaigns, local service campaigns, and website conversion campaigns.

---

## 08. Required Google Bot Fields

Google bot output may include:

```text
Search_Query
GMB_Name
Rating
Reviews_Number
Reputation Notes
Specialty
GMB_Link
Website_Link
Website_Status
```

Use Google bot output for local service campaigns, reputation campaigns, and segments where public review data matters.

---

## 09. Market Research Email Fields

Market research may add:

```text
Corporate Emails
Personal Emails
Other Source
Source Link
```

Personal emails are preferred for cold email campaigns.

Generic or corporate emails should be separated before launch.

---

## 10. Raw Data Quality Rules

Before handoff, check:

- Company name exists
- Domain or website exists when available
- Contact name exists when available
- Job title exists when available
- Geography is relevant
- Company size is close to campaign ICP
- Source link is included
- Duplicate source rows are reduced
- No obviously irrelevant companies dominate the list

If the source quality is weak, return it for review before enrichment.

---

## 11. Source Tracking

Every row should include source information.

Recommended source fields:

```text
Lead Source
Source URL
Bot Source
Collection Date
Collected By
Segment
Campaign Goal
```

Source tracking is important for later bounce, reply, and performance analysis.

---

## 12. Campaign Segment Tagging

Add a segment tag during collection when possible.

Example tags:

```text
HVAC
Portfolio
SaaS
E-commerce
Healthcare
Retail
Restaurants
Real Estate
Interior Design
Architecture
Local Service
```

The segment tag should match the future campaign sequence.

---

## 13. Lead Collection Approval Gate

Before moving to enrichment, confirm:

- Source links are approved
- Geography fits the campaign
- Employee size fits the campaign
- Titles are relevant
- Raw fields are sufficient
- Source tracking exists
- Segment tag is clear
- Market research and coding team handoff is complete

If the list is too broad, mark it:

```text
Needs Source Review
```

---

## 14. Final Rule

Lead collection should prioritize relevance before volume.

A smaller list of better-fit prospects is more useful than a large list that creates verification issues, weak personalization, or bad reply quality.
