## Alert Reporting Is Not Optional

After you triage an alert and figure out its a true positive, the job is not done yet. You have to document what you found before you close or escalate anything. A proper report is what actually makes the SOC work, without it L2 has no idea what you already looked at and has to start from scratch.

Why reports actually matter:

- Saves L2 time because they get full context immediately without asking you anything
- SIEM logs get deleted after 3 to 12 months but alert reports are kept forever
- Writing it out forces you to think clearly and actually improves your own analysis

## The 5 Ws Framework

Every report should answer these five things:

- Who — the user, account, or system that was involved
- What — the exact action or event that triggered the alert
- When — when the activity started and when it ended
- Where — the device, IP, or website involved
- Why — your reasoning for whatever verdict you gave

In the lab I practiced writing reports using exactly this framework on the SOC dashboard. Once you actually fill these out for a real alert it clicks — if your report answers all five then L2 can pick it up and understand everything without needing to call you.

## When to Escalate to L2

Not every alert needs to go up but some definitely do:

- Major cyberattack that needs deeper investigation than L1 can handle
- Remediation is needed like malware removal, host isolation, or password reset
- Management or law enforcement needs to be contacted
- You just do not fully understand the alert and are not sure what you are looking at

That last one is important. If you are unsure, escalate. Do not guess on something that could be a real breach.

## How to Actually Escalate

- Investigate the alert and move it to In Progress
- Write the report and set your verdict
- Reassign it to whoever the L2 is on shift
- Ping L2 in chat or just go tell them in person

The lab had escalation scenarios on the dashboard where I had to make the call on whether to escalate or close, and honestly the hardest part was the ones where you are not fully sure — that is exactly when you escalate.

## Critical Situations and What to Do

These are the scenarios where you have to think fast:

- L2 unavailable on a critical alert — call L2, if no answer call L3, then the manager
- Account compromised on Slack — never use the breached channel to communicate, call the user directly
- Too many alerts at once — prioritise by severity and let L2 know what is happening
- You misclassified an alert days ago and just realised — tell L2 immediately, do not sit on it
- SIEM logs not working — investigate whatever you still can and report the issue to L2 right away

## As an L1 Analyst

Closing a true positive is just the beginning of what needs to happen. The report and the escalation decision is what actually stops the attack from going further. A lazy report means L2 wastes time, a wrong escalation decision means the attacker gets more time inside the network. Get good at the 5 Ws, escalate when you are unsure, and communicate fast when something critical is happening.