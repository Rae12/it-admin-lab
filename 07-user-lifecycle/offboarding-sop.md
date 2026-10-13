# SOP: Employee Offboarding

**Owner:** IT | **Trigger:** HR termination notice | **SLA:** access removed at the effective time (voluntary: end of last day; involuntary: immediately)

## Steps
| # | Step | System | Done |
|---|---|---|---|
| 1 | Create linked JSM ticket; confirm effective date/time with HR | Jira | ☐ |
| 2 | Suspend Okta user; clear sessions and revoke tokens | Okta | ☐ |
| 3 | Reset Google password if needed; sign out all sessions | Google | ☐ |
| 4 | Transfer Drive/Calendar to manager; set mail forwarding/auto-reply per HR | Google | ☐ |
| 5 | Lock device via MDM; arrange return; wipe after data check | Intune/Jamf | ☐ |
| 6 | Remove from Zscaler groups (via Okta) and confirm | Zscaler | ☐ |
| 7 | Reclaim Zoom/Jira/Confluence licences | Okta/apps | ☐ |
| 8 | Remove from password manager; **rotate shared credentials** they accessed | PM | ☐ |
| 9 | Remove personal 3rd-party OAuth grants and API tokens | Google/apps | ☐ |
| 10 | Update asset inventory; attach evidence; close ticket | Jira | ☐ |
| 11 | Next day: confirm zero active sessions/accounts (reconciliation) | Okta | ☐ |
| 12 | After retention period (e.g. 30/90 days): delete account per policy | Google | ☐ |

## Escalation
Involuntary or security-sensitive leaver → do steps 2–3 first, then continue in order, with security owner informed.
