# IT Systems Administrator Lab

A hands-on lab simulating the work of a **remote Systems Administrator** at a small SaaS company: identity, endpoints, SaaS administration, security compliance, service desk, user lifecycle and automation.

> **Honesty note:** each lab has a status. ✅ = I built and tested it and have screenshots. 📝 = design/documentation only (no hardware or licence to build it). Nothing here is claimed as production experience.

## The scenario: Northwind Labs
A fictional 25-person fully remote company. Staff use MacBooks (engineering/design) and Windows laptops (finance/ops). Everything is SaaS: Okta is the identity provider (SSO + MFA), Google Workspace for email and files, Jira/Confluence for tickets and docs, Zoom for meetings, a password manager for secrets, and Zscaler for secure internet access. IT is a team of one admin plus two help desk staff.

## Lab index

| # | Lab | Tools | Hands-on on Windows? | Status |
|---|---|---|---|---|
| 01 | [Identity & SSO](01-identity-okta/) | Okta | Yes (free tenant) | ⬜ |
| 02 | [Google Workspace admin](02-google-workspace/) | Google Workspace | Yes (trial + domain) | ⬜ |
| 03 | [Endpoint management](03-endpoint-management/) | Intune (Windows), Jamf (design) | Intune yes; Jamf design-only | ⬜ |
| 04 | [Zero-trust network access](04-zero-trust-network/) | Zscaler (design), Cloudflare Zero Trust (hands-on analog) | Analog yes | ⬜ |
| 05 | [Service desk & knowledge base](05-service-desk-jira-confluence/) | Jira, Confluence | Yes (free plans) | ⬜ |
| 06 | [Password management](06-password-management/) | Bitwarden (or similar) | Yes | ⬜ |
| 07 | [User lifecycle](07-user-lifecycle/) | All of the above | Yes | ⬜ |
| 08 | [Security & compliance](08-security-compliance/) | Policies, evidence | Yes | ⬜ |
| 09 | [Automation & AI](09-automation/) | Okta workflows / scripts | Yes | ⬜ |

Update the status column as you complete each lab (⬜ not started, 🟨 in progress, ✅ done, 📝 design only).

## Start here
1. Read [docs/00-setup/lab-setup-windows.md](docs/00-setup/lab-setup-windows.md) to create accounts and your Windows test VM.
2. Do labs in order; 01 and 02 everything else depends on.
3. Work the [practice ticket queue](05-service-desk-jira-confluence/practice-tickets.md) once Jira is set up.
4. Save screenshots to `screenshots/NN/` using the filenames each lab lists. **Blur emails, tenant IDs, tokens and anything secret.**

## Job-requirement coverage

| Role requirement | Where it's covered |
|---|---|
| Maintain internal IT infrastructure, cloud and SaaS | Labs 01, 02, 05 |
| Resolve escalated tickets within service timelines | Lab 05 (SLAs, practice tickets) |
| Endpoint management and user access controls | Labs 01, 03, 04 |
| Data and internet security standards, documentation, policy enforcement | Labs 06, 08 |
| Audit evidence for internal security compliance | Lab 08 |
| Streamline provisioning and deprovisioning | Lab 07 |
| Identify and implement automation / AI enhancements | Lab 09 |
| Cross-train help desk staff | Lab 05 training guide, Lab 07 SOPs |

## Repo conventions
Each lab folder contains: `README.md` (objective, steps, verification, evidence list, production notes, talking points). Use [docs/lab-writeup-template.md](docs/lab-writeup-template.md) for extra write-ups.
