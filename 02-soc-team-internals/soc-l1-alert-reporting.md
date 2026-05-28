# SOC L1 Alert Reporting — Writeup

## What This Room Was About
This room was about what happens after alert triage.
How to write a proper report, when to escalate to L2,
and how to handle critical communication situations.

## What I Learned

### Alert Reporting
Before closing or escalating I need to document my investigation.
Most important for True Positives.

Why reports matter:
- Saves L2 time — they get full context immediately
- SIEM logs deleted after 3-12 months but alerts kept forever
- Writing reports actually improves my own analysis skills

### The 5 Ws Framework
- Who — user, account, or system involved
- What — exact action or event that happened
- When — when the activity started and ended
- Where — device, IP, or website involved
- Why — my reasoning for the final verdict

### When to Escalate to L2
- Major cyberattack needing deeper investigation
- Remediation needed — malware removal, host isolation, password reset
- Communication with management or law enforcement required
- I do not fully understand the alert

### How to Escalate
1. Investigate and move to In Progress
2. Write report and set verdict
3. Reassign to L2 on shift
4. Ping L2 in chat or in person

### Critical Communication Scenarios
- L2 unavailable on critical alert — call L2, then L3, then manager
- Account compromised on Slack — never use breached chat, call the user
- Too many alerts at once — prioritise correctly and inform L2
- Misclassified alert days later — tell L2 immediately
- SIEM logs not working — investigate what you can, report to L2

## What I Did in the Lab
Practiced writing alert reports using the 5 Ws framework.
Worked through escalation scenarios on the SOC dashboard.
Investigated alerts and made escalation decisions.

## My Key Takeaway
Closing True Positive is just the start.
A proper report and correct escalation is what actually stops the attack.
Always escalate when unsure — better to ask than miss a real breach.