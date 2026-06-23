## Context Is What Makes Triage Actually Work

When an alert comes in you cannot just look at the alert name and make a call. You need context — who is this user, what machine is involved, does this activity even make sense for them. That is what identity inventory, asset inventory, network diagrams, and workbooks are for. They are the resources sitting behind every investigation.

## Identity Inventory

This is basically a catalogue of every user and service account in the company. It has their roles, what privileges they have, when they normally work, and how to contact them. When an alert fires on a user account you check here first to answer — is this person even supposed to be doing this at this time.

Where this data usually comes from:

- Active Directory — most common, almost every SOC team has this
- SSO Providers — Okta, Google Workspace
- HR Systems — BambooHR, SAP
- Custom solutions — sometimes just a CSV or Excel sheet

## Asset Inventory

Same idea but for machines instead of people. It is a list of all servers and workstations in the organisation with details about what each one does and who should be accessing it. So when an alert fires on a hostname you can immediately check what that machine is and whether the access makes sense.

Where it comes from:

- Active Directory — works as an asset database too
- SIEM or EDR — tools like Elastic and CrowdStrike collect host information automatically
- MDM Solutions — Microsoft Intune, Jamf
- Custom solutions — again, sometimes just a spreadsheet

## Network Diagrams

This is a visual map of the company network — subnets, physical locations, how everything connects. It sounds like something only engineers care about but it is actually really useful during an investigation because it helps you understand attack paths.

In the lab there was a scenario where an external IP brute forced a VPN login and got in. It got assigned an internal IP from the VPN subnet, then started scanning the Database subnet but got blocked by the firewall. So it switched to the Office subnet to find its next target. Without the network diagram you are just looking at a bunch of IPs with no idea how they relate to each other. With it you can reconstruct exactly how the attacker moved through the network.

## SOC Workbooks

Workbooks are also called playbooks or runbooks depending on the team. They are step by step guides written by senior analysts that tell L1 exactly how to investigate a specific type of alert. The idea is that no matter who is on shift the investigation follows the same steps every time.

A typical workbook has three stages:

- Enrichment — use threat intel tools and identity inventory to get context on the alert
- Investigation — go through SIEM logs, make sense of what happened, decide on a verdict
- Escalation — either escalate to L2 or communicate directly with the affected user

In the lab I built a workbook by dragging and dropping investigation steps into the correct positions across these three stages. It made it much clearer why the order matters — you cannot investigate properly without enrichment first, and you cannot escalate without a verdict.

Why workbooks matter is pretty simple. L1 analysts are junior, mistakes happen, and pressure makes people skip steps. Workbooks make sure that does not happen by giving you a checklist you actually follow instead of just winging it.

## As an L1 Analyst

Before making any verdict you need to know who the user is, what the asset is, and how the network is laid out. Without that context you are just guessing. And without a workbook you are probably skipping steps you do not even realise are important. These resources exist so that every investigation you run is consistent, complete, and actually leads to the right call.