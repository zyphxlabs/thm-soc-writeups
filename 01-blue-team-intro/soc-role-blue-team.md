# SOC Role in Blue Team

## Security Hierarchy

Every company has different things they care about the most, like a law firm cares about keeping things private, a hospital cares about patient safety, and a factory cares about keeping things running and available. so security priorities change depending on what the company does.

the CEO is focused on the business side so they hire a CISO to handle all the security stuff, and the CISO then oversees all the security departments under them.

## Security Departments

There are different teams handling different sides of security

- Red Team — offensive security, these are the ethical hackers and pentesters
- GRC Team — handles policies and compliance stuff like PCI DSS
- Blue Team — defensive security, this is where SOC analysts and incident responders sit

## Blue Team Structure

The blue team is the one monitoring attacks and responding to them quickly, depending on the company size it can have anywhere from 3 to 50 members.
inside the blue team the SOC is the first line of defense and handles most of the alerts and attacks that come in, it has different levels like L1 analyst who triages alerts and passes the complex ones to L2, L2 analyst who digs into the more advanced attacks, the engineer who configures tools like EDR and SIEM, and the manager who handles the whole SOC team.
then there is the CIRT which only gets called when the SOC cannot handle the incident on their own, they deal with major breaches and they do it without depending on tools, examples of CIRTs are JPCERT, Mandiant and AWS CIRT.
there are also some specialized roles in the blue team

- Digital Forensics Analyst — uncovers hidden threats in disk and memory
- Threat Intelligence Analyst — researches emerging threat groups
- AppSec Engineer — secures the software development lifecycle
- AI Researcher — studies AI threats and defenses

## Internal SOC vs MSSP

Internal SOC means you are protecting one single company, the pace is calmer, we  have fewer tools but we know them really deeply. MSSP is the opposite, we are protecting many clients at the same time, it is high pressure, we are dealing with many tools and you see a lot more incidents a lot faster.
both are fine places to start but MSSP gives us way more exposure to real attacks early on which is valuable.

## SOC Career Path

we as a fresher start as L1 and as we gain experience we can move to L2 or go into a specialization, the options after L1 are L2 Analyst, SOC Engineer, CIRT, Threat Intel, or even the CISO path if we want to go that far.

four tips that actually matter as a SOC analyst

- learn from every single alert no matter how small
- think like an attacker so you understand what they are doing
- verify everything before you act on it
- get involved in real incidents whenever you get the chance