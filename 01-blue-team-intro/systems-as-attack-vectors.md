# Systems as Attack Vectors — Writeup

## What This Room Was About
This room was about how attackers go after systems directly without needing to trick any human first. like even if every single employee is trained and knows what phishing is and never clicks a bad link, if the system itself is weak then it can still get breached and nobody would even know it happened

## What I Learned

### Why Systems Are Targeted
Systems hold everything. emails, banking data, customer records, all of it. so if we breach one mail server we basically get access to thousands of mailboxes at once crazy right..? thats why systems are a bigger target than going after individual users, the reward of compromising a system is much bigger

### How Systems Get Attacked

So there are a few different ways attackers go after systems and they are all pretty different from each other

**Human Led Attacks**
Most breaches actually still come back to users doing something wrong without realising it. weak passwords, plugging in a random USB, downloading pirated software. and 81 percent of breaches involve stolen or weak passwords which is kind of crazy when you think about it

**Vulnerabilities**
Every software has flaws and no system litreally not even a single one is perfectly secured thats just the reality. over 40,000 CVEs were published in 2024 alone. and sometimes these flaws sit there for years without anyone noticing, like Shellshock existed since 1992 but nobody found it until 2014. then theres zero day which is when the attacker finds the vulnerability before anyone else does, even before the vendor knows about it. the only way to catch that in time is through SOC skills

**Supply Chain Attacks**
This one is interesting. instead of attacking a company directly the attacker goes after a library or an app that thousands of companies are already using. then when that app pushes an update, the malware goes to all the users at once. SolarWinds and 3CX are the most famous examples of these kind of attacks  and its really hard to defend against because you literally cannot control every single library your software depends on

**Misconfigurations**
This is not even a bug in the code, its just a human setting something up wrong. like someone set the password to 123456 and that exposed 64 million McDonald's job applications. a misconfigured AWS cloud breached 106 million bank customers. even smart fridges have been silently pulled into botnet attacks. the system worked exactly as configured, it was just configured badly

### Responding to Vulnerabilities
When a vulnerability gets found theres a process to handle it while waiting for a proper fix:
- wait for the vendor to release a patch for that vulnerability
- while waiting restrict access to trusted IPs only
- apply any temporary measures the vendor recommends
- block known attack patterns on your IPS or WAF

### Responding to Misconfigurations
Misconfigurations are actually easier to deal with because theres no patch needed, you just fix what was set up wrong. you do things like penetration testing, vulnerability scans, and configuration audits to find the mistakes. you can also compare your setup against CIS benchmarks to make sure everything is configured the right way

### Mitigation Measures
- Patch Management — keep all software updated so known vulnerabilities get closed
- IT Training — teach the IT team how to avoid making misconfigurations in the first place
- Network Protection — restrict access so only trusted IPs can get in
- Antivirus — catches and stops a lot of attacks automatically without needing manual intervention

## What I Did in the Lab
I opened the SOC dashboard and worked through two tabs. the first one was Systems at Risk where i reviewed flagged systems and decided what action to take for each one. the second was the Remediation Plan where I had to pick the best mitigation measures to actually secure each system

## My Key Takeaway
Humans and systems both need equal protection becuase  both are risk to an organization in my opinion, we cannot just focus on one and ignore the other attackers do not think in categories like okay today I will do social engineering or today I will exploit a vulnerability they just look at what path is easiest and take it. As a SOC analyst I need to understand both sides because the attacker definitely does not care about whether its a human or system all they care about is there goal