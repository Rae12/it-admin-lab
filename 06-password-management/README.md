# Lab 06: Password Management

**Objective:** Deploy a team password manager with sensible structure, sharing and recovery.

## Steps
1. Create an organisation (use a trial if team features need it). Enforce MFA for all members. 📸 `06/pm-org-mfa.png`
2. **Collections/vaults** by function: `Shared-IT`, `Shared-Finance`, `Shared-Engineering`, `Shared-Marketing`. Principle: least privilege, owner per vault. 📸 `06/pm-collections.png`
3. **Policies:** master password length, require 2-step login, disable personal vault export where possible, session timeout. 📸 `06/pm-policies.png`
4. **SSO integration** with Okta if available on your plan; otherwise document the design.
5. **Emergency access / recovery:** configure admin recovery; document the process in a runbook.
6. **Secret rotation drill:** store a fake shared credential, share it, then simulate an offboarding: remove the user, rotate the secret, record the steps. 📸 `06/pm-rotation.png`
7. **User guide:** one-page Confluence guide for staff (install extension, create entries, share safely).

## Verification
- [ ] A user outside Finance cannot see Finance vault
- [ ] Removed user loses access to shared items
- [ ] Recovery tested

## Talking points
Why shared credentials must be rotated at offboarding, secrets sprawl (credentials in Slack/Docs), service-account ownership.
