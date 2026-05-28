# SOC L1 Alert Triage — Writeup

## What This Room Was About
This room taught me how alerts are created, how to read them,
and how to properly investigate and close them as a SOC L1 analyst.

## How Alerts Are Created
First an event happens — a login, a file download, a process running.
The system logs it and sends it to a SIEM or EDR.
The SIEM checks if it matches any detection rules.
If it does — it creates an alert.
This saves analysts from reading millions of raw logs every day.

## Alert Properties
Every alert has these key fields:
- Name — what happened
- Time — when it happened
- Severity — Low, Medium, High, Critical
- Status — New, In Progress, Closed
- Verdict — True Positive or False Positive
- Assignee — who is investigating it
- Description — why this was flagged
- Fields — affected user, hostname, command used

## How to Pick Which Alert First
1. Only pick New unassigned alerts
2. Start with Critical severity then High then Medium then Low
3. For same severity — take the oldest one first

## How to Triage an Alert

Step 1 — Assign it to yourself and move to In Progress.

Step 2 — Investigate:
- Who is affected — user, hostname, device
- What action triggered it
- Look at events before and after the alert
- Check threat intelligence tools like AbuseIPDB

Step 3 — Close it:
- Decide True Positive or False Positive
- Write a comment explaining what you found and why
- Move to Closed

## What I Did in the Lab
Opened the SOC dashboard.
Reviewed the alerts in the queue.
Prioritised by severity and time.
Investigated each alert step by step.
Closed them with correct verdicts and comments.

## My Key Takeaway
Missing a True Positive means a real attack goes undetected.
Every step in triage exists for a reason.
Always assign first, investigate properly, comment everything, then close.