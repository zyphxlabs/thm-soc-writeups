# Systems as Attack Vectors — Writeup

## What This Room Was About
This room was about how attackers target systems directly
without needing to trick a human first.
Even if every employee is trained and aware, a weak system
can still be breached without anyone knowing.

## What I Learned

### Why Systems Are Targeted
Systems store everything — emails, banking data, customer records.
Breaching one mail server gives access to thousands of mailboxes.
That is why systems are more valuable targets than individual users.

### How Systems Get Attacked

Human Led Attacks
Users cause most breaches without realising it.
Weak passwords, malicious USB drives, pirated software.
81 percent of breaches involve stolen or weak passwords.

Vulnerabilities
Every software has flaws. Over 40,000 CVEs were published in 2024.
Shellshock existed since 1992 but was not discovered until 2014.
Zero day — attacker finds the vulnerability before anyone else.
Only SOC skills can detect zero day exploitation in time.

Supply Chain Attacks
Attacker compromises a library or app used by thousands of companies.
One update pushes malware to all users at once.
SolarWinds and 3CX are the most famous examples.
Hard to defend against because you cannot control every library.

Misconfigurations
Not a bug — a human mistake in how the system was set up.
123456 password exposed 64 million McDonald's job applications.
Misconfigured AWS cloud breached 106 million bank customers.
Smart fridges silently used in botnet attacks.

### Responding to Vulnerabilities
Wait for a patch from the vendor.
While waiting restrict access to trusted IPs only.
Apply temporary vendor measures.
Block known attack patterns on IPS or WAF.

### Responding to Misconfigurations
No patch needed — just fix the setup.
Penetration testing, vulnerability scans, configuration audits.
Match systems against CIS benchmarks.

### Mitigation Measures
Patch Management — keep all software updated.
IT Training — teach IT team to avoid misconfigurations.
Network Protection — restrict access to trusted IPs only.
Antivirus — stops or detects many attacks automatically.

## What I Did in the Lab
Opened the SOC dashboard and worked through two tabs.

Systems at Risk:
Reviewed flagged systems and decided what action to take for each one.

Remediation Plan:
Chose the best mitigation measures to secure each system.

## My Key Takeaway
Humans and systems both need equal protection.
Attackers do not separate human hacking from system hacking.
They take whichever path is easiest.
As a SOC analyst I need to understand both sides equally well.