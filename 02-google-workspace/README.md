# Lab 02: Google Workspace Administration

**Objective:** Configure a secure, well-organised Workspace tenant managed through Okta.

## Steps
1. **Verify the domain** and create the super admin plus a break-glass admin. 📸 `02/gws-domain-verified.png`
2. **Org units:** `/Engineering`, `/Finance`, `/Sales`, `/IT`, `/Contractors`. Apply settings per OU rather than globally. 📸 `02/gws-orgunits.png`
3. **Groups:** mailing and security groups mirroring Okta groups. 📸 `02/gws-groups.png`
4. **Security settings:** enforce 2-Step Verification, disable less-secure apps, set session length, restrict third-party app access (allowlist OAuth apps). 📸 `02/gws-security.png`
5. **Sharing:** restrict external Drive sharing by OU; Finance cannot share externally; warn on external shares. 📸 `02/gws-sharing.png`
6. **Admin roles:** create a custom `Help Desk` role (reset passwords, view users only). Assign to a test help desk user. 📸 `02/gws-custom-role.png`
7. **Data protection:** configure a DLP rule for SSN/credit card patterns if your edition supports it; otherwise document as design.
8. **Audit logs:** find an admin action, a Drive external share, and a login in the Reporting/Audit logs. 📸 `02/gws-audit-log.png`
9. **Offboarding feature:** practise transferring a user's Drive data and suspending the account (used again in Lab 07).

## Verification checklist
- [ ] Help desk role can reset a password but cannot see Drive content or change security settings
- [ ] External share blocked for Finance, allowed with warning for Sales
- [ ] Data transfer completed to manager on test offboarding

## Production notes
Billing/licence reclamation, retention rules (Vault), alert centre rules, email authentication (SPF/DKIM/DMARC) records on the domain.

## Talking points
Least privilege admin roles, why OUs and groups serve different purposes, how SPF/DKIM/DMARC protect the domain.
