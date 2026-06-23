## What is a SOC

SOC stands for Security Operations Center, basically its a team that watches over a company's security 24/7. SOC analysts are the first ones responding when something goes wrong — every day they are monitoring alerts, investigating threats, and stopping attacks before they get worse.

## The Team and Who Does What

The SOC isn't just one person doing everything, there are different roles and each one has its own job. junior security analyst is the entry level, monitors and investigates alerts daily. senior analyst handles the more complex cases and helps junior analysts when something is too big. SOC engineer is the one building and maintaining the tools the whole team depends on. SOC manager keeps everything on track and reports up to management. and then there's the incident responder who only gets called in when something really serious happens.

## What a Junior Analyst Actually Does Day to Day

As a junior analyst the daily job is monitoring alerts and investigating anything that looks suspicious. you also sit in on SOC brainstorms to work through problems with the team and cooperate with other teams when needed. and because this field never stops changing you are constantly learning new attack techniques and new defenses, there is no point where you just know everything and stop.

## Lab — Catching a Malicious Login

In the lab i spotted a critical alert, it was a successful SSH login from a suspicious IP `221.181.185.159`. looked it up on AbuseIPDB and it came back confirmed malicious — the IP belonged to China Mobile and had been involved in 4 cyber attacks, categories were Port Scan, C2 Server, and PlugX malware.

So i escalated it to Will Griffin who is the SOC Team Lead. while he was investigating i blocked the IP on the firewall to slow things down and stop any further damage.

## What I Took Away From This

Failed login attempts on their own aren't a huge deal usually, but the moment one succeeds that changes everything. a successful login from a random external IP is worth escalating immediately. and before you escalate, always check the IP reputation first — tools like AbuseIPDB or Cisco Talos will tell you pretty fast whether its actually malicious or just noise.

## As an L1 Analyst

Your job isn't just to look at alerts and close them, its to actually understand what you are looking at. checking an IP takes two minutes and it tells you whether something is worth escalating or not. that habit alone makes you a much better analyst than someone who just clicks through alerts without thinking.