# Junior Security Analyst Intro

## What is a SOC
A Security Operations Center is a team that protects a company 24/7.
SOC analysts are the first line of defense against cyber attacks.
Every day you monitor alerts, investigate threats and stop attacks.

## SOC Team Roles
- Junior Security Analyst — monitors and investigates alerts daily
- Senior Analyst — handles complex cases, helps junior analysts
- SOC Engineer — maintains and configures security tools
- SOC Manager — reports results to management, keeps team on track
- Incident Responder — called in during major incidents only

## Daily Duties of a Junior Analyst
- Monitor and investigate security alerts
- Participate in SOC brainstorms
- Cooperate with other teams
- Constantly learn new attacks and defenses

## What I Practiced in the Lab

Alert Investigation:
- Spotted critical alert — successful SSH login from suspicious IP 221.181.185.159
- Looked up IP on AbuseIPDB — confirmed malicious
- IP was from China Mobile, involved in 4 cyber attacks
- Categories: Port Scan, C2 Server, PlugX malware

Escalation:
- Escalated to Will Griffin — SOC Team Lead
- Never escalate to wrong person — know your team structure

Firewall Block:
- Blocked malicious IP 221.181.185.159 on the firewall
- This stops or slows down the attack while senior analyst investigates

## Key Lesson
Failed login attempts are low priority.
Successful login from malicious IP is critical — escalate immediately.
Always check IP reputation on AbuseIPDB or Cisco Talos before escalating.