# Junior Security Analyst Intro

## What is a SOC

SOC stands for Security Operations Center basically its a team that protects a company 24/7, SOC analysts are the first one repsonding to an incident every day they are monitoring alerts investigating threats and stopping attacks.

## SOC Team Roles

The team has different roles like junior security analyst who monitors and investigates alerts daily, senior analyst who  handles the complex cases and helps junior analysts, SOC engineer is the one who develop and maintain the security tools to aid the team, SOC manager reports results to management and keeps the team on track, and incident responder only gets called in when something really major happens.

## Daily Duties of a Junior Analyst

As a junior analyst our daily job is to monitor and investigate security alerts, we also participate in SOC brainstorms  to solve different problems and cooperate with other teams, and we are constantly learning new attacks and defenses because this field keeps evolving.

## What I Practiced in the Lab

I spotted a critical alert which was a successful SSH login from a suspicious IP 221.181.185.159, I looked it up on AbuseIPDB(tools) and it was confirmed malicious, the IP was from China Mobile and was involved in 4 cyber attacks, categories were Port Scan, C2 Server and PlugX malware so i escalated it to Will Griffin who is the SOC Team Lead, and while the senior analyst investigates i blocked the malicious IP 221.181.185.159 on the firewall to stop or slow down the attack.

## Key Lesson

Failed login attempts are gernally not a big risk untill they are successful so weshould always escalate these but before escalating always check the IP reputation on tools like AbuseIPDB or Cisco Talos.