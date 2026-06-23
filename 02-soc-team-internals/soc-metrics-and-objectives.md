## How SOC Performance Is Actually Measured

A SOC is not just vibes and alerts, there are actual numbers that tell you if the team is doing well or quietly failing. These metrics matter because if something is off in the numbers it usually means real attacks are slipping through or analysts are burning out from too much noise.

### Alerts Count

This is just the total alerts an analyst receives per day. The healthy range is 5 to 30 alerts per analyst per day. Too many means there is a noise problem where bad detection rules are firing on everything. Too few means the tools are not seeing enough of the network, which is a visibility problem and honestly scarier.

### False Positive Rate

FPR is false positives divided by total alerts. If this hits 80 percent or above that is a serious problem because analysts start ignoring alerts when most of them turn out to be nothing. You cannot blame them either, if 8 out of every 10 alerts are fake eventually your brain stops taking them seriously and that is exactly when a real one slips through. Fix is to tune the detection rules and use SOAR to automatically handle the common false positives so they stop cluttering the queue.

### Alert Escalation Rate

AER is escalated alerts divided by total alerts and it should stay below 50 percent, ideally below 20. If L1 is escalating more than half of everything it usually means analysts do not have enough experience or confidence to make the call themselves. In the lab one of the scenarios had a high AER and the fix was getting L1 analysts more training and clearer workbooks to follow.

### Threat Detection Rate

TDR is detected threats divided by total threats and this one should always be 100 percent. There is no acceptable number below that. Every single missed threat is a potential ransomware infection or data exfiltration that nobody caught.

## SLA Metrics — The Time-Based Ones

These three are about how fast the SOC reacts and each one has a target.

MTTD is Mean Time to Detect — average time between an attack starting and the SOC tools catching it. Target is under 5 minutes. If it is going over 30 minutes you need to talk to engineers about improving detection rules or check if there are log delays somewhere.

MTTA is Mean Time to Acknowledge — average time for L1 to start triaging a new alert after it comes in. Target is under 10 minutes. If it is over 30 you need better real time notifications and more even alert distribution across the team.

MTTR is Mean Time to Respond — average time to actually stop the breach after it is detected. Target is under 60 minutes. If it is going over 4 hours that means escalation to L2 is too slow or response procedures are not documented clearly enough.

In the lab there were three SOC manager scenarios and each one had specific metrics failing. The task was to figure out which metric was the problem and assign the right fix for it. The MTTA one was interesting because the alert queue was not being picked up fast enough at shift start, simple fix but it has a big impact on the number.

## How L1 Directly Affects These Numbers

- Report noisy detection rules to engineers so false positive rate goes down
- Acknowledge alerts immediately when shift starts so MTTA stays low
- Escalate true positives fast without sitting on them so MTTR does not blow up
- Follow workbooks properly so no steps get skipped during investigation

## As an L1 Analyst

These metrics are not just management stuff to ignore. MTTA and false positive rate are literally things you personally move every single day depending on how fast you acknowledge alerts and how accurately you close them. Good numbers mean real attacks get caught faster and the team runs smoother. Bad numbers mean something is broken and eventually a breach goes unnoticed. Knowing what the metrics mean and how you affect them is what separates someone who just closes tickets from someone who actually makes the SOC better.