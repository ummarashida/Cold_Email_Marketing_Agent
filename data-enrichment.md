## 01. Main Goal of Data Enrichment

The main goal of Data Enrichment is to prepare a clean and accurate prospect list for cold email campaigns.

The final file must be campaign-ready, meaning:

- No duplicate contacts
- No duplicate companies
- No incorrect or messy company names
- No generic company emails
- No empty important fields
- A clean, professional, and properly organized prospect list from top to bottom

The purpose is to make sure the lead list is neat, clean, accurate, and ready to use for cold email outreach.

---

## 02. Common Columns in the Lead List

The lead list usually contains common columns such as:

- Company Name
- Personal LinkedIn URL
- Email
- First Name
- Last Name
- Job Title
- Company Website
- Company Domain
- Location
- Industry
- Remarks / Comments

---

## 03. Data Checking and Cleaning Process

### First Name and Last Name Check

Check the First Name and Last Name columns carefully.

Make sure the names are written in English.

If any name is written in another language or contains non-English characters, identify and mark it.

Example:

- Arabic characters
- Chinese characters
- Japanese characters
- Korean characters
- Russian characters
- Any other non-English language characters

If found, mark the row in the remarks/comments column.

Use this remark:

`Non-English Name`

---

### Company Name Check

Check the Company Name column carefully.

Make sure each company name is clean, professional, and written consistently.

Fix messy company names when the correct name is clear.

Examples of messy company names:

- Extra spaces
- Random capital letters
- Website URLs instead of company names
- Legal suffix issues such as repeated LLC, Ltd, Inc, or GmbH
- Incorrect spelling
- Company names mixed with descriptions

If the company name is unclear or cannot be confidently corrected, mark the row as:

`Needs Manual Review`

---

### Empty Email Check

Check the Email column and find out if any email field is empty.

If an email is missing, mark it clearly as:

`Email Missing`

---

### Generic Email Check

Check the Email column and identify any generic company email addresses.

Generic emails are not personal prospect emails and should not be used for cold email campaigns.

Examples of generic emails:

- info@domain.com
- contact@domain.com
- hello@domain.com
- support@domain.com
- sales@domain.com
- marketing@domain.com
- admin@domain.com
- office@domain.com
- team@domain.com
- social@domain.com
- inquiry@domain.com
- enquiries@domain.com
- service@domain.com
- customer@domain.com
- careers@domain.com
- jobs@domain.com
- press@domain.com
- media@domain.com
- billing@domain.com
- accounts@domain.com

If a generic email is found, mark it as:

`Generic Email`

---

### Duplicate Contact Check

Check the full lead list and identify duplicate contacts.

If the same contact appears more than once, keep only one unique contact as valid.

Mark the other duplicate rows as:

`Duplicate Contact`

A contact should be considered duplicate if the same email appears more than once.

Also check possible duplicates based on:

- Same first name
- Same last name
- Same company
- Same LinkedIn profile
- Same email domain

But the email address should be the main identifier for duplicate checking.

---

### Duplicate Company Check

Check the full lead list and identify duplicate companies.

If the same company appears multiple times, keep the best contact only unless the campaign specifically allows multiple contacts from the same company.

Use the Company Name, Company Website, and Company Domain columns to identify duplicate companies.

Mark extra rows from the same company as:

`Duplicate Company`

---

### Important Field Check

Check whether important fields are empty.

Important fields usually include:

- Company Name
- Email
- First Name
- Last Name
- Job Title
- Company Website or Company Domain
- Location

If an important field is missing and the row cannot be completed confidently, mark it as:

`Invalid Data`

If the row may still be useful but needs human checking, mark it as:

`Needs Manual Review`

---

### Final Cleaning Rule

After checking all rows, the final prospect list should be clean, organized, and ready for cold email campaign use.

Each problematic row should be marked with a clear remark, such as:

- Email Missing
- Generic Email
- Duplicate Contact
- Duplicate Company
- Non-English Name
- Invalid Data
- Needs Manual Review

Rows without problems should be kept clean and should not contain unnecessary notes.

The final file should be organized from top to bottom with valid prospects first and problematic rows clearly marked for review or removal.

---

## 04. First Name and Last Name Quality Check

### Invalid First Name / Last Name Check

Check the First Name and Last Name columns carefully.

A name should not be only a single letter or random capital letters.

Identify and mark names that do not look like real person names.

Examples of invalid names:

- A
- B
- M
- Aa
- AB
- MD
- Mr
- Ms
- N/A
- Unknown
- Test

If the First Name or Last Name looks incomplete, fake, or not like a real person's name, mark the row as:

`Invalid Name`

---

### Blank First Name Check

Check if the First Name column is blank.

If the First Name is missing, mark the row as:

`First Name Missing`

This is important because First Name is commonly used for cold email personalization.

Example:

```text
Hi {{firstName}},
```

If the first name is missing, the email personalization may break or look unprofessional.

---

## 05. Company Name Cleaning Rule

Check the Company Name column and clean it properly.

The company name should not contain legal suffixes or unnecessary company endings.

Remove suffixes such as:

- LLC
- LLP
- Inc
- INC
- Ltd
- Limited
- Org
- Organization
- Corp
- Corporation
- Co.
- Company
- PLC
- Pvt Ltd
- GmbH
- Group
- Holdings

Example:

```text
Bright Home Design LLC -> Bright Home Design
ABC Marketing Inc -> ABC Marketing
Creative Studio LLP -> Creative Studio
```

---

### Company Name Link Removal

If the company name contains any link, URL, or website format, remove the link and keep only the clean company name.

Examples:

```text
https://abcmarketing.com -> ABC Marketing
www.brighthome.com -> Bright Home
ABC Marketing - https://abcmarketing.com -> ABC Marketing
```

If the correct company name is not clear from the link, mark it as:

`Needs Manual Review`

---

## 06. Remarks/Status Column Rule

For every issue found, add a clear remark in the Remarks column.

Possible remarks:

```text
First Name Missing
Invalid Name
Non-English Name
Email Missing
Generic Email
Duplicate Contact
Company Name Cleaned
Company Suffix Removed
Company Link Removed
Needs Manual Review
```

If one row has multiple problems, separate the remarks with commas.

Example:

```text
Invalid Name, Generic Email, Company Suffix Removed
```

---

## 07. Row-Wise Prospect Analysis

After the basic data cleaning is complete, analyze each row based on the final available data.

The goal is to understand each prospect properly and identify:

- Their business type
- Their industry
- Whether they are B2B, B2C, or both
- Whether they are tech, non-tech, or mixed
- Their possible business pain points
- Their possible sales/marketing structure
- Which Accord Tech Solutions service is the best fit for them

---

## 08. B2B / B2C Classification

For each company, classify the business model as:

```text
B2B
B2C
Both
Unknown
```

Use this logic:

- **B2B:** The company sells products or services to other businesses.
- **B2C:** The company sells directly to consumers.
- **Both:** The company serves both businesses and consumers.
- **Unknown:** Not enough information is available.

Add a short reason if needed.

Example:

```text
B2B - The company provides software/services to other businesses.
```

---

## 09. Tech / Non-Tech Classification

For each company, classify the company type as:

```text
Tech
Non-Tech
Mixed
Unknown
```

Use this logic:

- **Tech:** SaaS, software, IT, AI, automation, apps, platforms, cybersecurity, data, cloud, digital products.
- **Non-Tech:** Interior design, real estate, construction, healthcare, legal, education, manufacturing, local services, retail, hospitality.
- **Mixed:** E-commerce brands, digital agencies, service companies using both online and offline business models.
- **Unknown:** Not enough information is available.

---

## 10. Industry Segmentation

Segment each company by industry.

Examples:

```text
SaaS
IT Services
Digital Marketing
E-commerce
Real Estate
Interior Design
Architecture
Construction
Healthcare
Education
Finance
Legal Services
Manufacturing
Retail
Hospitality
Professional Services
Consulting
Local Service Business
Other
```

If the industry is unclear, mark it as:

```text
Unknown
```

---

## 11. Sales and Marketing Team Check

Try to identify whether the company appears to have:

```text
Sales Team
Marketing Team
Both Sales and Marketing Team
No Clear Team Found
Unknown
```

Use available data such as:

- Job titles
- LinkedIn company page
- Website team page
- Careers page
- Employee roles
- Company size
- Public company information

Examples of sales-related titles:

```text
Sales Manager
Business Development Manager
Account Executive
SDR
BDR
Head of Sales
VP Sales
```

Examples of marketing-related titles:

```text
Marketing Manager
Growth Manager
Demand Generation Manager
Email Marketing Manager
Head of Marketing
CMO
Content Marketing Manager
```

If there is not enough information, do not guess. Mark it as:

```text
Unknown
```

---

## 12. Pain Point Identification

For each company, identify realistic possible pain points based on their industry, business model, company size, website, social presence, and available data.

Pain points should be specific and useful for cold email personalization.

Examples of possible pain points:

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

Bad pain point example:

```text
Needs marketing
```

Good pain point example:

```text
The company appears to serve B2B clients but does not show a clear outbound lead generation or appointment-setting process.
```

Keep pain points short, realistic, and spreadsheet-friendly.

---

## 13. Accord Tech Solutions Service Fit

Based on the final enriched data, identify which Accord Tech Solutions service is the best fit for each prospect.

Possible service categories:

```text
B2B Lead Generation
Cold Email Outreach
Cold Email Campaign Management
Appointment Setting Support
Email Marketing Strategy
B2C Email Marketing
Klaviyo Email Marketing
Email Automation Setup
Lead List Building
Data Enrichment
Email Verification
CRM Data Management
LinkedIn Prospect Research
Website Conversion Support
Digital Marketing Support
```

Choose the most relevant service for each prospect.

Do not select too many services for one company.

Best format:

```text
Primary Service Fit: Cold Email Outreach
Secondary Service Fit: Lead Generation
```

---

## 14. Service Fit Logic

Use this logic when selecting the best service:

### If the company is B2B

Best possible services:

```text
Cold Email Outreach
B2B Lead Generation
Appointment Setting Support
Lead List Building
Email Verification
CRM Data Management
```

### If the company is B2C

Best possible services:

```text
B2C Email Marketing
Klaviyo Email Marketing
Email Automation Setup
Customer Retention Campaigns
Customer Reactivation Campaigns
```

### If the company is Both B2B and B2C

Best possible services:

```text
Cold Email Outreach
B2C Email Marketing
Email Automation Setup
Lead Generation
```

### If the company has a sales team

Best possible services:

```text
Cold Email Outreach
Appointment Setting Support
CRM Data Management
Lead Generation
```

### If the company has a marketing team

Best possible services:

```text
Email Marketing Strategy
Email Automation Setup
Klaviyo Email Marketing
B2C Email Marketing
Digital Marketing Support
```

### If the company has weak public data

Best possible services:

```text
Data Enrichment
Lead List Building
LinkedIn Prospect Research
CRM Data Management
```

---

## 15. Required Analysis Columns

Add these columns in the final file:

```text
Industry Segment
B2B / B2C
Tech / Non-Tech
Sales Team Status
Marketing Team Status
Main Pain Point
Secondary Pain Point
Primary ATS Service Fit
Secondary ATS Service Fit
Service Fit Reason
Cold Email Angle
Personalization Note
ICP Match
Data Confidence
Remarks
```

---

## 16. Cold Email Angle

For each row, create a short cold email angle based on the company's pain point and service fit.

Example:

```text
Helping B2B companies build a cleaner outbound system to reach more decision-makers.
```

Another example:

```text
Helping e-commerce brands improve repeat purchases through better email automation.
```

Keep the angle simple, human, and relevant.

---

## 17. ICP Match Score

Based on the enriched data, classify the lead as:

```text
High Match
Medium Match
Low Match
Not a Match
```

Use this logic:

- **High Match:** Clear need for ATS service and strong fit.
- **Medium Match:** Possible need, but not fully confirmed.
- **Low Match:** Weak fit but still usable for testing.
- **Not a Match:** Not suitable for our services.

---

## 18. Final Rule

Do not guess randomly.

Use the available data, company website, LinkedIn, industry, business model, and public information to make the best possible analysis.

If something cannot be confirmed, use:

```text
Unknown
Not Found
Not Confirmed
Needs Manual Review
```

The final enriched file must help us understand:

```text
Who the company is
What type of business they are
What pain point they may have
Which ATS service fits them best
What cold email angle we should use
Whether they are a good ICP match or not
```
