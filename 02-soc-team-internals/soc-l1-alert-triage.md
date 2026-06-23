## How Alerts Are Even Created

Before you can triage anything you need to understand where alerts come from. First an event happens — a login, a file download, a process running on a machine. The system logs it and sends it to a SIEM or EDR. The SIEM then checks if that event matches any detection rules it has, and if it does it creates an alert. This is what saves analysts from having to read through millions of raw logs every single day, the rules do the filtering and you just deal with what actually looks suspicious.

## What an Alert Actually Contains

Every alert has a set of fields and you need to read all of them before doing anything:

- Name — what happened
- Time — when it happened
- Severity — Low, Medium, High, or Critical
- Status — New, In Progress, or Closed
- Verdict — True Positive or False Positive
- Assignee — who is currently investigating it
- Description — why this event got flagged
- Fields — affected user, hostname, command used, whatever is relevant

## Which Alert to Pick First

When you open the dashboard and see a queue full of alerts you need to know where to start:

- Only pick alerts that are New and unassigned
- Start with Critical, then High, then Medium, then Low
- If two alerts have the same severity, take the older one first

In the lab I opened the SOC dashboard and did exactly this — went through the queue, sorted by severity, and worked oldest to newest within the same level. Sounds simple but it matters a lot when you have ten alerts sitting there at once.

## How to Actually Triage

First thing you do is assign the alert to yourself and move it to In Progress. This tells everyone else on the team that someone is already on it so nobody doubles up.

Then you investigate. You want to figure out who is affected — the user, hostname, device. What action actually triggered the alert. Look at the events right before and after to get context, because one event alone rarely tells the full story. Check threat intelligence tools like AbuseIPDB if there is an IP or domain involved.

Once you have enough to make a call you close it. Decide if it is a True Positive or False Positive, write a comment explaining what you found and why you made that call, then move it to Closed. In the lab I closed each alert with a comment and a verdict after going through this exact process — the comment step feels small but it is what makes your work useful to anyone who looks at it later.

## As an L1 Analyst

Missing a True Positive means a real attack goes undetected and nobody even knows. Every step in this process exists for a reason — assign so there is no confusion, investigate properly so you do not miss anything, comment everything so L2 has context if it needs to go up. Triage sounds like a basic skill but done badly it is how attacks slip through completely unnoticed.