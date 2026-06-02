# Email Infrastructure Setup

## Purpose

This file defines the required infrastructure process before any Accord Tech Solutions cold email campaign can launch.

Use this file to check domains, DNS records, mailboxes, custom tracking domains, warmup, sender settings, and campaign sending limits.

No campaign should launch from an unverified or unhealthy sending setup.

---

## 01. Infrastructure Goal

The goal of email infrastructure setup is to protect sender reputation and give each campaign a stable sending foundation.

Every campaign must use:

- Approved sending domains
- Proper DNS authentication
- Healthy inboxes
- Custom tracking domains when required
- Controlled sending limits
- Warmup enabled before sending
- Clear ownership in the infrastructure tracker

The campaign should not use Accord Tech Solutions' primary business domain for cold outbound unless leadership explicitly approves it.

---

## 02. Domain Buying Rule

Approved buying platforms include:

- Namecheap
- Hostinger
- Google Domains
- Other CEO/ED-approved providers

Before buying a domain:

1. Prepare the proposed domain list.
2. Check that the domains look professional and close to the ATS brand or campaign use case.
3. Send the list to the CEO and ED by email.
4. Buy only after approval.

Avoid domains that look random, spammy, misleading, or unrelated to the sender identity.

---

## 03. Domain Usage Rule

Each sending domain must have a clear purpose.

Track:

- Domain name
- Provider
- Purchase date
- Renewal date
- Assigned campaign
- Assigned inboxes
- DNS status
- Custom tracking status
- Warmup status
- Health status
- Owner or responsible team member

If a domain has deliverability problems, do not reuse it until the issue is investigated.

---

## 04. Required DNS Records

Every direct domain setup must include:

- SPF
- DKIM
- DMARC
- CNAME when required
- Custom tracking CNAME when required

Use these tools for checking:

- DKIM Checker: <https://mxtoolbox.com/dkim.aspx>
- DMARC Checker: <https://mxtoolbox.com/>
- SPF Checker: <https://mxtoolbox.com/spf.aspx>

If inboxes are purchased from a reseller, DNS may already be handled by the reseller. In that case, verify what is already configured and update the tracker.

---

## 05. SPF Settings

For Hostinger and Instantly:

```text
"v=spf1 include:_spf.mail.hostinger.com include:spf.instantly.ai ~all"
```

For Google Workspace:

```text
v=spf1 include:_spf.google.com ~all
```

SPF must pass before the inbox is used for campaign sending.

---

## 06. DKIM Check

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

If the DKIM TXT value is found and verifies correctly, DKIM is set.

If DKIM is missing, pause the setup and complete DKIM before sending.

---

## 07. DMARC Settings

Previously used DMARC:

```text
Name: _dmarc
Type: TXT
Value: v=DMARC1; p=none; rua=mailto:dmarc@yourdomain.com
```

The team found this may create higher bounce risk in some setups.

Current safer DMARC option:

```text
Name: _dmarc
Type: TXT
Value: "v=DMARC1; p=none; rua=mailto:name@accordtechbd.com; ruf=mailto:wasiqur.rahman@accordtechbd.com; fo=1"
```

Alternative stricter DMARC option:

```text
v=DMARC1; p=reject; pct=100; rua=mailto:reports@inboxsetup.com; ruf=mailto:reports@inboxsetup.com; ri=604800; aspf=s; adkim=s
```

Use the DMARC option approved by the email marketing lead, CEO, or ED for the specific setup.

---

## 08. Domain Redirect

Each sending domain should redirect to:

```text
https://accordtechsolutions.com
```

Check the redirect in a browser after setup.

If the redirect fails, fix it before launch.

---

## 09. Custom Tracking Domain

Use this format:

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
3. Open each inbox.
4. Go to Settings.
5. Open Custom Tracking Domain.
6. Paste the custom tracking domain.
7. Click Verify or Auto Check.
8. Confirm the domain shows as verified.

Do not launch until the tracking domain status is confirmed for each inbox where tracking will be used.

---

## 10. Mailbox Creation Rule

If buying inboxes from resellers:

```text
Maximum 3-4 mailboxes per domain
```

If creating Hostinger inboxes directly:

```text
2-5 inboxes per domain
```

Each mailbox should have:

- Sender name
- Sender persona
- Profile image if required
- Signature
- Assigned domain
- Assigned campaign status
- Warmup enabled
- Sending limit configured

---

## 11. Adding Inboxes to Instantly

Process:

1. Create all inboxes.
2. Organize inbox details sequentially in a file.
3. Export the file in CSV format.
4. Open Instantly.
5. Go to Email Accounts.
6. Click Add New.
7. Select Connect Existing Account.
8. Select Any Provider.
9. Upload the CSV.
10. Confirm all inboxes connect successfully.

Any inbox that fails connection must be fixed before campaign assignment.

---

## 12. Warmup and Sending Settings

For each inbox in Instantly:

1. Enable warmup.
2. Go to Settings.
3. Open Sender Information and Signature.
4. Set campaign limit:

```text
10
```

5. Set minimum wait time:

```text
30 minutes
```

6. Set custom tracking domain.
7. Set warmup per day:

```text
25
```

8. Save settings.

Do not use a new inbox at full volume immediately.

---

## 13. Infrastructure Tracker

Update the Email Infrastructure Tracker after setup:

<https://docs.google.com/spreadsheets/d/1SX_4BR47A7bT7KxrOKRQ7AkKHWPVNuiJZUGoxTUuyO4/edit?gid=922694498#gid=922694498>

Required tracker fields:

- Domain
- Provider
- Inbox email
- Sender name
- SPF status
- DKIM status
- DMARC status
- Redirect status
- Custom tracking status
- Warmup status
- Instantly connection status
- Campaign limit
- Minimum wait time
- Current campaign
- Health status
- Notes

---

## 14. Health Check Before Campaign Assignment

Before assigning inboxes to a campaign, check:

- Inbox is connected
- Warmup is active
- DNS is verified
- Custom tracking is verified if used
- Sender name and signature are correct
- No recent bounce spike
- No unhealthy status in Instantly
- Inbox is not overloaded by another campaign
- Campaign limit is safe

If any item fails, mark the inbox as:

```text
Not Ready
```

---

## 15. Infrastructure Approval Gate

Before launch, confirm:

- Domains approved
- DNS records verified
- Inboxes connected
- Warmup active
- Sending limits configured
- Custom tracking checked
- Redirect checked
- Tracker updated
- CEO and ED approval received when required

Campaign status should remain:

```text
Infrastructure Pending
```

until all checks pass.

---

## 16. Final Infrastructure Rule

Never treat email infrastructure as a one-time setup.

Check it before launch, during the first 3 days, before scaling, and after campaign closing.

Use only healthy, verified, warmed, and properly tracked sending accounts.
