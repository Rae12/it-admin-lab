# Access Control Policy

**Version 1.0 | Owner: IT | Review: annually**

1. **Purpose:** ensure only authorised people access company systems and data, at the minimum level needed.
2. **Scope:** all employees, contractors and systems (Okta, Google Workspace, Atlassian, Zoom, password manager, MDM, Zscaler).
3. **Identity:** each person has one unique identity in Okta. Shared accounts are prohibited unless an owner is assigned and approved.
4. **Authentication:** MFA is required for all users. Admins use phishing-resistant factors where available.
5. **Authorisation:** access is granted by role group (see access matrix). Exceptions require a ticket, manager and system-owner approval, and an expiry date.
6. **Privileged access:** admin accounts are separate from daily accounts, approved by the security owner, and reviewed quarterly.
7. **Provisioning:** within 1 business day of a complete request. **Deprovisioning:** at the effective termination time.
8. **Review:** quarterly access reviews; findings tracked to closure.
9. **Logging:** authentication and admin activity logs are retained for at least 12 months.
10. **Enforcement:** violations are reported to IT and may result in access removal and disciplinary action.
