# SOC Metrics and Objectives — Writeup

## What This Room Was About
This room was about how SOC performance is measured,
what metrics matter, and how to improve them as an L1 analyst.

## What I Learned

### Core SOC Metrics

Alerts Count
Total alerts received per day.
5 to 30 alerts per day per analyst is healthy.
Too many = noise problem. Too few = visibility problem.

False Positive Rate
FPR = False Positives divided by Total Alerts.
80% or higher is a serious problem.
Analysts start ignoring alerts when noise is too high.
Fix: tune detection rules, automate common false positives with SOAR.

Alert Escalation Rate
AER = Escalated Alerts divided by Total Alerts.
Should be below 50%, ideally below 20%.
Too high means L1 analysts lack experience or confidence.

Threat Detection Rate
TDR = Detected Threats divided by Total Threats.
Should always be 100%.
Every missed threat can mean ransomware or data exfiltration.

### SLA Metrics

MTTD — Mean Time to Detect
Average time between attack and detection by SOC tools.
SLA target: under 5 minutes.
Fix if over 30 min: ask engineers to improve detection rules or check log delays.

MTTA — Mean Time to Acknowledge
Average time for L1 to start triaging a new alert.
SLA target: under 10 minutes.
Fix if over 30 min: ensure real time notifications, distribute alerts evenly.

MTTR — Mean Time to Respond
Average time to actually stop the breach.
SLA target: under 60 minutes.
Fix if over 4 hours: escalate faster to L2, document response procedures.

### How to Improve as L1
- Reduce false positives by reporting noisy rules to engineers
- Acknowledge alerts immediately when shift starts
- Escalate True Positives quickly without delay
- Follow workbooks to avoid missing steps

## What I Did in the Lab
Worked through three SOC manager scenarios.
Identified which metrics were failing in each scenario.
Assigned the correct improvement tasks to fix each metric issue.

## My Key Takeaway
Metrics exist to make SOC more efficient and attacks less successful.
As L1 I directly impact MTTA and False Positive Rate every single day.
Good metrics lead to career growth — bad ones mean real attacks get missed.