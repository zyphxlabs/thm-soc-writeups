# SOC L1 Alert Reporting — Writeup

## What This Room Was About
This room taught me what happens after I triage an alert.
How to write a proper report, when to escalate to L2,
and how to communicate in critical situations.

## Three New Skills

### Alert Reporting
Before closing or passing an alert to L2 I need to document my investigation.
This is especially important for True Positives.
A good report saves L2 time and preserves evidence for the future.

Why reports matter:
- Gives L2 context so they do not start from scratch
- SIEM logs are deleted after 3-12 months but alerts are kept forever
- Writing reports improves my own investigation skills

### The 5 Ws Framework
Every alert report should answer these five questions:
- Who — which user, account, or system is involved
- What — what exact action or event happened
- When — when did the suspicious activity start and end
- Where — which device, IP address, or website was involved
- Why — my reasoning for the final verdict

### Alert Escalation
Escalate to L2 when:
- The alert indicates a major cyberattack needing deeper investigation
- Remediation is needed — malware removal, host isolation, password reset
- Communication with management or law enforcement is required
- I do not fully understand the alert and need senior help

How to escalate:
1. Move alert to In Progress and investigate
2. Write the alert report and set verdict
3. Reassign alert to L2 on shift
4. Ping L2 in chat or in person

### Communication Cases I Learned
- L2 unavailable for 30 minutes on critical alert — call L2, then L3, then manager
- Account compromise on Slack — do not use breached chat, call the user instead
- Too many critical alerts at once — prioritise and inform L2 immediately
- Realised I misclassified an alert days later — tell L2 immediately
- SIEM logs not parsing — investigate what I can and report to L2

## What I Did in the Lab
Opened the SOC dashboard and worked through real alert scenarios.
Practiced writing alert reports using the 5 Ws framework.
Investigated alerts and decided whether to escalate or close them.

## My Key Takeaway
Closing an alert as True Positive is just the start.
A proper report and correct escalation is what actually stops the attack.
Never skip reporting even if it feels like extra work.
If I am unsure about anything escalate — always better to ask than miss a real attack.