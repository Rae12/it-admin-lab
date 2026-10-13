# Break-Glass Procedure

**Purpose:** regain control if SSO/MFA fails or all admins are locked out.

- Two emergency super-admin accounts in Okta, excluded from SSO-dependent policies, with long random passwords stored offline in two physical locations.
- Hardware key registered to each.
- **Use requires:** a P1 ticket and a second person's approval; use is alerted to the security owner.
- After use: rotate credentials, review logs for the use period, write a post-incident review.
- Test every 6 months; record test date and result here.
