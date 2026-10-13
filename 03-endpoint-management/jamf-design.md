# Jamf Pro Design for macOS Fleet (Design Only 📝)

| Area | Design |
|---|---|
| Enrolment | Apple Business Manager → Automated Device Enrolment → Jamf PreStage; user authenticates with Okta; skip unneeded Setup Assistant panes |
| Smart groups | Unencrypted Macs, macOS < required version, no check-in 14+ days, by department |
| Baseline profiles | FileVault with recovery key escrow, firewall on, screen lock 5 min, Gatekeeper enforced, restricted kernel extensions |
| Apps | Self Service catalogue: Zoom, Slack, browsers, Okta Verify; required: Zscaler client, password manager |
| Patching | Patch policies with 3-day deferral and a pilot group first |
| Compliance reporting | Weekly report of failing smart groups → Jira tickets |
| Offboarding | Lock device via MDM, collect, wipe, re-assign |
| Integration | Okta device trust for sign-in, Zscaler device posture |

## Risks
Misconfigured profile that locks users out of Wi-Fi: always pilot first. FileVault key loss: escrow before enforcing.
