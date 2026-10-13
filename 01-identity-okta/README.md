# Lab 01: Identity & Single Sign-On (Okta)

**Objective:** Make Okta the single source of truth for access. Users sign in once with MFA and get app access based on group membership.

## Architecture
```
Okta (IdP) ──SAML/OIDC──► Google Workspace
     │      ──SAML──────► Atlassian (Jira/Confluence)
     │      ──SWA/SAML──► Zoom, Bitwarden (if supported)
     └─ Groups ► app assignments ► licences
```

## Steps
1. **Tenant hardening:** create a super admin with MFA; create a separate break-glass account. 📸 `01/okta-admin-mfa.png`
2. **Directory:** create the groups from the setup guide; create the 5 test users; assign to groups. 📸 `01/okta-groups.png`
3. **Password and MFA policy:** min length 14, lockout after 5 attempts, Okta Verify required for all, no SMS as sole factor. 📸 `01/okta-auth-policy.png`
4. **Sign-on policy:** require MFA every session for admin apps; allow 12 hours for standard apps. Block legacy auth.
5. **Google Workspace SSO:** configure SAML in Google Admin (Security → SSO with third-party IdP) and the Google Workspace app in Okta. Test with a non-admin user first. 📸 `01/okta-google-sso.png`
6. **Atlassian SSO:** set up SAML via Atlassian Guard/Access (check what the free plan allows; otherwise document as design).
7. **Group-based app assignment:** assign apps to groups, not individuals. 📸 `01/okta-app-assignments.png`
8. **System Log review:** trigger a failed login and find it in Reports → System Log. 📸 `01/okta-system-log.png`

## Verification checklist
- [ ] Test user signs in via Okta dashboard, passes MFA, lands in Google Workspace without a second password
- [ ] User removed from a group loses the app tile within minutes
- [ ] Suspended user cannot sign in anywhere
- [ ] Failed login visible in System Log

## Troubleshooting notes to record
SAML ACS URL mismatch, clock skew, users locked out by a mistyped policy (this is why break-glass exists).

## Production notes
Use HR-driven provisioning (Workday/BambooHR → Okta) as the source of truth; SCIM for downstream apps; phishing-resistant MFA (FIDO2/Okta FastPass) for admins; admin roles scoped by least privilege; alert on admin role changes.

## Interview talking points
- Why group-based assignment beats per-user assignment (auditability, offboarding)
- How you would recover from a locked-out super admin
- Difference between SAML, OIDC and SCIM, and what each does in the lifecycle
