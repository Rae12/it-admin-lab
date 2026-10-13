# Control Mapping

Illustrative mapping to SOC 2 Common Criteria themes. Confirm mappings against your actual framework.

| Control | Policy ref | Technical implementation | Evidence | Lab |
|---|---|---|---|---|
| MFA for all users | Access §4 | Okta authentication policy; Google 2SV | Policy screenshot, MFA enrolment report | 01, 02 |
| Role-based access | Access §5 | Okta groups → app assignments | Group list, access matrix | 01, 07 |
| Timely deprovisioning | Access §7 | Offboarding SOP, Okta suspension | Offboarding ticket with timestamps | 07 |
| Periodic access review | Access §8 | Quarterly review template | Completed review + tickets | 07 |
| Encryption at rest | Endpoint §2 | BitLocker/FileVault via MDM | Compliance report | 03 |
| Patch management | Endpoint §3 | Intune update rings / Jamf patch | Patch compliance report | 03 |
| Secure web access | Endpoint §5 | Zscaler policy (design) / Cloudflare analog | Policy export, block log | 04 |
| Secrets management | Password §1–2 | Password manager policies | Policy screenshot, rotation record | 06 |
| Incident response | – | Security incident request type | Incident ticket T-06 | 05 |
