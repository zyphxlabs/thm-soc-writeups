# SOC Workbooks and Lookups — Writeup

## What This Room Was About
This room was about the tools and resources SOC analysts use
to get context about alerts — identity inventory, asset inventory,
network diagrams, and workbooks.

## What I Learned

### Identity Inventory
A catalogue of all corporate users and service accounts.
Includes their roles, privileges, working hours, and contacts.
Helps answer — who is this user and is their activity expected?

Sources:
- Active Directory — most common, used by most SOC teams
- SSO Providers — Okta, Google Workspace
- HR Systems — BambooHR, SAP
- Custom solutions — CSV or Excel sheets

### Asset Inventory
A list of all servers and workstations in the organisation.
Helps answer — what is this machine and who should access it?

Sources:
- Active Directory — also works as asset database
- SIEM or EDR — Elastic, CrowdStrike collect host info
- MDM Solutions — Microsoft Intune, Jamf
- Custom solutions — CSV or Excel sheets

### Network Diagrams
A visual map of the company network — subnets, locations, connections.
Helps make sense of suspicious IP activity and attack paths.

Example from the lab:
- External IP brute forced VPN login
- Got assigned internal IP from VPN subnet
- Started scanning Database subnet — blocked by firewall
- Switched to Office subnet to find next target
Network diagram helped reconstruct the full attack path.

### SOC Workbooks
Also called playbooks or runbooks.
Step by step guide for investigating specific alert types.
Senior analysts write them to help L1 analysts triage consistently.

Three stages in a typical workbook:
1. Enrichment — use threat intel and identity inventory to get context
2. Investigation — review SIEM logs and make a verdict
3. Escalation — escalate to L2 or communicate with the affected user

Why workbooks matter:
- L1 analysts are junior — workbooks prevent mistakes
- Every analyst follows the same steps — consistent quality
- No vital steps are skipped during investigation

## What I Did in the Lab
Built a workbook by dragging and dropping the correct investigation steps
into the right positions in the workflow.
Practiced structuring an alert investigation into enrichment, investigation
and escalation stages.

## My Key Takeaway
Context is everything in SOC work.
Before making a verdict I need to know who the user is, what the asset is,
and how the network is structured.
Workbooks make sure I never skip a critical step even under pressure.