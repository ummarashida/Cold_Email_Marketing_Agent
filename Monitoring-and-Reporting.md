# Monitoring and Reporting

## Purpose

This file defines how Accord Tech Solutions monitors cold email campaigns after launch, decides when to pause or scale, reports performance, and closes campaigns properly.

Use this file during pilot launch, the first 3 days, daily review, weekly review, scaling, optimization, and final reporting.

---

## 01. Main Goal

The goal of monitoring is to protect deliverability, catch errors early, improve campaign performance, and turn campaign learning into better future campaigns.

Campaigns should be managed actively after launch.

---

## 02. Core Metrics

Track:

- Total sent
- Delivered
- Opened
- Replied
- Positive replies
- Negative replies
- Unsubscribes
- Bounces
- Spam complaints
- Meetings booked
- Performance by segment
- Performance by inbox
- Performance by sequence step
- Performance by subject line

---

## 03. Performance Targets

Standard campaign targets:

```text
Open rate: 60%+
Reply rate: 3%+
Bounce rate: below 2%
Spam complaints: below 1
Complaint rate before scaling: below 0.1%
```

These are guidance thresholds. If campaign context is unusual, document the reason.

---

## 04. After Launch Check

Immediately after launch, check:

- Selected inboxes are active
- Campaign status is live
- Sending schedule is running
- Sequence mapping works
- Stop-on-reply is enabled
- Unsubscribe option works
- Emails are going out correctly
- No unexpected high bounce appears

If a major issue is found, pause the campaign and fix it first.

---

## 05. First 3 Days Monitoring

For the first 3 days, review the campaign daily.

Check:

- Sent volume
- Bounce rate
- Open rate
- Reply rate
- Unsubscribe or spam complaints
- Inbox performance
- Personalization errors
- Sequence step behavior
- Reply classification

The first 3 days are the highest-risk period for mapping and deliverability issues.

---

## 06. Daily Review

Every campaign day, record:

- Total sent
- Delivered
- Opened
- Replied
- Positive replies
- Negative replies
- Unsubscribes
- Meetings booked
- Bounced
- Paused inboxes
- Notes

Also review:

- Segment performance
- Lead source performance
- Inbox performance
- Campaign step performance
- Subject line performance

---

## 07. Pause Rules

Pause the campaign or affected inboxes if:

- Bounce rate goes above 2%
- Spam complaints increase
- Open rate drops suddenly
- Wrong leads were uploaded
- Personalization errors are found
- One inbox performs badly
- Unsubscribe rate looks abnormal
- Stop-on-reply is not working
- Tracking or links are broken

Do not continue sending until the issue is checked and fixed.

---

## 08. Troubleshooting Process

When a campaign is paused:

1. Identify the affected campaign, segment, inbox, or sequence step.
2. Export the affected records if needed.
3. Check verification status.
4. Check suppression status.
5. Check field mapping.
6. Check DNS and inbox health.
7. Check sending volume and schedule.
8. Check whether a specific lead source caused the issue.
9. Fix the issue.
10. Relaunch only after approval.

Document the cause and fix in the campaign notes.

---

## 09. Scale-Up Criteria

Only scale when:

- Pilot batch performs well
- Bounce rate stays below 2%
- Complaint rate stays below 0.1%
- Replies are relevant
- Inboxes remain healthy
- No major personalization errors appear
- Suppression process is working

Increase volume slowly.

Do not scale a weak or unstable campaign.

---

## 10. Weekly Review

Each week, review:

- Best subject lines
- Worst subject lines
- Best-performing segments
- Weak segments
- Bounce reasons
- Negative reply reasons
- Unsubscribe reasons
- Follow-up performance
- Positive reply source step
- Meetings booked
- Learnings for next campaign

Use this review to improve future lists, copy, targeting, and setup.

---

## 11. A/B Test Review

When a test is active, compare:

- Open rate
- Reply rate
- Positive reply rate
- Negative reply rate
- Unsubscribe rate
- Bounce rate

Do not choose a winner based only on opens.

The preferred winner is the version that creates the best positive replies with acceptable deliverability.

---

## 12. Reply Reporting

For positive replies, record:

- Company name
- Contact name
- Email
- Campaign name
- Segment
- Sequence step
- Subject line
- Email body version
- Reply text summary
- Intent level
- Recommended next action
- Meeting status

Use positive-response-lead-report-agent.md for detailed positive reply handling.

---

## 13. Final Campaign Report

At campaign close, prepare a final report with:

- Campaign name
- Segment
- Date range
- List size
- Sent count
- Delivered count
- Open rate
- Reply rate
- Positive reply rate
- Bounce rate
- Unsubscribe rate
- Spam complaints
- Meetings booked
- Best subject line
- Best sequence step
- Best-performing segment
- Worst-performing segment
- Main issues
- Recommended improvements
- Final decision: continue, improve, pause, or archive

---

## 14. Campaign Closing Process

When the campaign ends:

1. Export the final full report.
2. Record key results.
3. Update the suppression list.
4. Remove bad leads from future use.
5. Note best and worst scripts.
6. Note best and worst segments.
7. Add learnings to the performance database.
8. Keep inboxes warm after campaign end.
9. Archive or label the campaign clearly.

---

## 15. Final Rule

Every campaign should leave the team smarter than it started.

Track results clearly, document issues honestly, and use campaign learning to improve the next list, sequence, setup, and reply handling process.
