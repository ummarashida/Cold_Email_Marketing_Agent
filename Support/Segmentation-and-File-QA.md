# Segmentation and File QA

## Purpose

This file defines how Accord Tech Solutions segments leads, checks ICP match, prepares campaign CSV files, cleans company names, checks blank fields, logs duplicates, uploads files to Drive, and secures approval before platform upload.

Use this file after enrichment and verification, before sequence writing and Instantly setup.

---

## 01. Main Goal

The goal is to turn a cleaned lead list into campaign-ready segmented files.

Each final file should be:

- Relevant to one segment
- Clean
- Verified
- Suppression-checked
- ICP-checked
- Properly mapped for email tokens
- Approved before upload

---

## 02. Segmentation Criteria

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
- Service fit
- Campaign angle

Every lead should belong to one primary segment.

---

## 03. Example Segments

Common segment examples:

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
Local Service Business
Reputation Management
SEO Opportunity
Website Issue
Lead Generation
```

Do not mix unrelated segments in one campaign file.

---

## 04. Primary Segment Rule

Assign each lead to one primary segment.

Use this field:

```text
Primary Segment
```

If additional context is useful, add:

```text
Secondary Segment
```

Example:

```text
Primary Segment: HVAC
Secondary Segment: SEO Opportunity
```

The email sequence should be written for the primary segment.

---

## 05. ICP Gate

Before finalizing a segmented list, every row must pass an ICP match check.

Check:

- First name
- Email quality
- No generic or role-based emails unless approved
- LinkedIn employee profile
- HQ location
- City, state, and country
- Company size
- Business type
- Pain point identification
- ATS service fit
- Suppression status

Only approved ICP rows should move into the final CSV.

---

## 06. ICP Status Values

Use one status:

```text
High Match
Medium Match
Low Match
Not a Match
Needs Manual Review
```

Campaign-ready files should prioritize:

```text
High Match
Medium Match
```

Low Match records should be used only if approved for a test.

Not a Match records should not be uploaded.

---

## 07. Blank Column Check

Before CSV export, confirm no required blank fields remain.

Required fields:

```text
Email
First Name
Company Name
Company Domain or Website
Job Title
Industry or Segment
ICP Match
Primary ATS Service Fit
Primary Segment
```

If a required token field is blank, define fallback values before launch.

---

## 08. Name Formatting Check

Check:

- First names are capitalized properly
- Last names are capitalized properly
- No non-English names unless approved
- No initials only
- No placeholder values

Invalid examples:

```text
N/A
Unknown
Test
Admin
Mr
Ms
A
AB
```

Mark issues as:

```text
Invalid Name
First Name Missing
Needs Manual Review
```

---

## 09. Company Name Normalization

Company names should be clean and natural.

Remove unnecessary suffixes:

```text
Inc
LLC
Ltd
Co.
Company
Corporation
Corp
Group
Holdings
GmbH
Pvt Ltd
```

Examples:

```text
Bright Home Design LLC -> Bright Home Design
ABC Marketing Inc -> ABC Marketing
Creative Studio LLP -> Creative Studio
```

Do not over-clean if the suffix is part of the brand identity.

---

## 10. Duplicate Log

Export removed duplicates to a separate log.

Duplicate log should include:

```text
Email
Company Name
Company Domain
Duplicate Type
Kept Row ID
Removed Row ID
Reason
Date
```

Duplicate types:

```text
Duplicate Contact
Duplicate Company
Duplicate LinkedIn
Duplicate Domain
```

---

## 11. Final CSV File Naming

Use a clear file name:

```text
[Segment]_[ServiceAngle]_[Batch]_[Date]_Final.csv
```

Example:

```text
HVAC_SEO_Batch01_2026-06-02_Final.csv
```

Avoid vague names like:

```text
final.csv
new leads.csv
cleaned list.csv
```

---

## 12. Drive Upload

After segmentation, upload files to the approved Drive folder.

Upload:

- Final CSV
- Quarantine tab or file
- Duplicate log
- Suppression check notes
- Approval notes when available

Make sure the file owner and campaign manager can access the folder.

---

## 13. Approval Before Upload

Before uploading to Instantly, take approval from the CEO and ED when required.

Approval should cover:

- Segment
- ICP match
- File quality
- Verification status
- Suppression check
- Service angle
- Sequence readiness
- Infrastructure readiness

Do not upload unapproved files into a live campaign.

---

## 14. Final File QA Checklist

Confirm:

- No blank emails
- No invalid emails
- No generic emails unless approved
- No risky or unknown emails unless approved
- No suppressed contacts
- No unapproved duplicates
- Company names cleaned
- Names formatted properly
- Required columns present
- Segment tag present
- ICP status present
- Service fit present
- Personalization fields present
- Fallback values defined
- File uploaded to Drive
- Approval received

---

## 15. Final Rule

The final CSV is the campaign foundation.

If the file is messy, the sequence, Instantly setup, and reporting will also become messy. Clean the file before launch, not after problems appear.
