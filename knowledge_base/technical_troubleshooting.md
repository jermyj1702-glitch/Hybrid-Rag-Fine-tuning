# Technical Troubleshooting

## Scope
Covers product and platform technical issues: app crashes, login failures
caused by the client, sync errors, broken features, errors on checkout, and
performance problems. Account access policy questions follow account recovery.

## First-Line Steps
1. Capture the exact symptom, when it started, and whether it is reproducible.
2. Record environment: app or browser version, operating system, and device.
3. Try the standard recovery sequence: update to the latest version, restart
   the app, clear cache, and retry on another network or device.
4. Confirm whether the issue is account-specific or affects all users (check
   the status dashboard for a known incident).

## Crashes And Errors
For repeatable crashes, collect the action that triggers it and any error
code or screenshot. For checkout or payment errors, do not retry charges
repeatedly — confirm whether any charge actually posted before advising a
second attempt.

## Data And Sync
If data is missing or not syncing, avoid destructive steps (reinstall,
account reset) until a backup or server-side copy is confirmed, to prevent
permanent loss.

## Escalation To Engineering
Escalate when: the issue is reproducible after first-line steps, multiple
customers report the same symptom, data loss is involved, or a security flaw
is suspected. Provide the reproduction steps, environment, and timestamps so
engineering can act without re-contacting the customer.

## Communication
Give one clear instruction at a time, set expectations for investigation
time, and never blame the customer. Follow the escalation matrix for severity
and routing.
