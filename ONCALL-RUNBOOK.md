# On-Call Runbook

This runbook covers the day-to-day on-call routine and the end-of-week handover. Work through it top to bottom; every step exists because skipping it has bitten us before.

## Morning Checklist

- [ ] Check the pager and Slack for any alerts that fired overnight — do not clear alerts until you understand what happened.
- [ ] Review the last 12 hours of dashboards (error rate, latency p95/p99, saturation) for anomalies that did not page.
- [ ] Read the previous day's on-call notes and any open Sev-3 items left in triage.
- [ ] Scan the incident channel for unresolved threads and confirm no Sev-2 is still unowned.
- [ ] Verify all scheduled jobs and cron pipelines completed (ETL, backups, nightly builds) and investigate any failures.
- [ ] Confirm backup success for production databases and object storage.
- [ ] Check certificate and disk-space expiry warnings for anything due within 7 days.
- [ ] Acknowledge or triage every new monitoring alert in the queue before 10:00 local time.
- [ ] Update the on-call status message in the team channel with anything worth flagging.

## Handover Checklist

- [ ] Write a summary of the week: incidents handled, ongoing investigations, and anything unusual you noticed.
- [ ] Document every open issue with its current state, owner, and the next concrete action.
- [ ] Record which alerts were noisy or flaky so we can tune thresholds and reduce pager fatigue.
- [ ] Confirm no unresolved incidents remain — anything Sev-1 or Sev-2 must be closed or formally transferred with a named owner.
- [ ] Tag follow-up tickets for anything you did not have time to finish, with links to relevant logs.
- [ ] Walk the incoming on-call engineer through the notes verbally (15 minutes) and let them ask questions.
- [ ] Hand over the credentials, phone, and any physical access you were holding for the rotation.
- [ ] Confirm the incoming on-call has acknowledged the handover in the shared channel.
- [ ] Archive the incident channels that are resolved and file the postmortem actions as tickets.
- [ ] Take a final look at the alert queue and leave it empty or clearly annotated.
