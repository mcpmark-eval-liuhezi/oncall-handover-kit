# Escalation Guide

How to escalate when something breaks. Severity definitions are deliberately short — decide fast, adjust later. When in doubt, treat it as the higher severity.

## Sev-1

Customer-facing outage or data loss. Drop everything.

1. Declare the incident in the incident channel and page the primary on-call plus the backup on-call simultaneously.
2. Open an incident bridge call and post the bridge link in the incident channel; assign an Incident Commander and a scribe.
3. Acknowledge within 5 minutes. If no acknowledgement in 5 minutes, page the secondary and the engineering manager.
4. Notify the engineering manager and the product owner within 15 minutes; they own customer communications.
5. Post a status update in the customer-facing status page within 30 minutes, then every 30 minutes until resolution.
6. Begin mitigation: check the most recent deploy, roll back if the deploy is the suspected cause, otherwise follow the service-specific recovery notes in the runbook.
7. If mitigation is unclear after 30 minutes, escalate to the service owner and pull in the platform team.
8. If unresolved after 60 minutes, escalate to the VP of Engineering and consider invoking the external vendor support contract.
9. Before closing: confirm with the Incident Commander that systems are healthy for at least 30 minutes and all customers are confirmed recovered.
10. File the postmortem within 48 hours — it is mandatory for every Sev-1.

## Sev-2

Degradation with customer impact, or internal-only outage. Needs action today, not a bridge call.

1. Acknowledge within 15 minutes and post the issue in the team channel with a short description of the impact.
2. Identify the blast radius: which services, which customers, since when.
3. Attempt a quick fix if one is obvious (roll back the last deploy, restart the affected service, clear a stuck queue).
4. If the quick fix fails or the cause is unclear, open a ticket with severity High and loop in the owning team in Slack.
5. Post a status update in the team channel at least every 2 hours while the issue is open.
6. Escalate to a Sev-1 if customer-facing impact grows or if resolution is not in sight by end of day.
7. De-escalate to a Sev-3 ticket once impact is contained, and hand off any remaining work to the ticket owner.
8. Write a short summary in the on-call notes covering the cause, fix, and follow-ups.
