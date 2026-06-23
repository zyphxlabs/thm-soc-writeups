## Why Systems Are a Bigger Target

Systems hold everything — emails, banking data, customer records, all of it in one place. So if an attacker breaches one mail server they basically get access to thousands of mailboxes at once. That is why going after a system is way more attractive than trying to trick individual users one by one, the reward is just much bigger. And the scary part is even if every single employee is trained and never clicks a bad link, if the system itself is weak it can still get breached and nobody would even know it happened.

## How Systems Actually Get Attacked

### Human Mistakes

Most breaches still come back to a user doing something wrong without realising it. Weak passwords, plugging in a random USB, downloading pirated software. 81 percent of breaches involve stolen or weak credentials which is honestly a crazy number when you think about it.

### Vulnerabilities

Every software has flaws, not a single system exists that is perfectly secured. Over 40,000 CVEs were published in 2024 alone. Sometimes these flaws just sit there for years without anyone noticing — Shellshock existed since 1992 but nobody found it until 2014. Then there is zero day which is when the attacker finds the flaw before even the vendor does, and the only way to catch something like that is good SOC skills because there is no patch coming yet.

### Supply Chain Attacks

Instead of attacking a company directly the attacker goes after a library or tool that thousands of companies already use. When that software pushes an update the malware goes to everyone at once. SolarWinds and 3CX are the famous examples of this. Hard to defend against because you cannot control every single library your software depends on.

### Misconfigurations

Not even a bug, just someone setting something up wrong. A password set to 123456 exposed 64 million McDonalds job applications. A misconfigured AWS bucket breached 106 million bank customers. Even smart fridges got pulled into botnets. The system worked exactly as it was configured, it was just configured badly.

## When a Vulnerability Is Found

While waiting for a patch to come out:

- Wait for the vendor to release an official patch
- Restrict access to trusted IPs only in the meantime
- Apply whatever temporary measures the vendor recommends
- Block known attack patterns on IPS or WAF

## When a Misconfiguration Is Found

No patch needed here, just fix what was set wrong. Run penetration tests, vulnerability scans, and config audits regularly. Compare everything against CIS benchmarks to catch what is off.

## Mitigation Measures

- Patch Management — keep all software updated so known vulnerabilities get closed
- IT Training — teach the IT team to avoid misconfigurations before they happen
- Network Protection — restrict access to trusted IPs and limit exposure
- Antivirus — catches and stops known attacks automatically

## As an L1 Analyst

Attackers do not think in categories like today I will do social engineering or today I will exploit a vulnerability. They just look at whatever path is easiest and go through it. So as an L1 analyst you have to understand both sides — the human side and the system side — because the attacker definitely does not care which one it is. If you only know one you are already behind.