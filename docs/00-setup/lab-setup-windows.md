# Lab Setup on Windows

Free tiers and trial terms change often. **Check each vendor's current signup page** before you start.

## 1. Accounts to create

| Tool | How to get it | Notes |
|---|---|---|
| Domain name | Any registrar (~$10/yr) | Needed for Google Workspace and clean SSO. Use something like `northwind-lab.example` style of your own choosing |
| Okta | Okta developer / Integrator free tenant (developer.okta.com) | Some features (e.g. Workflows, Device Trust) may be limited on free plans |
| Google Workspace | Free trial (typically 14 days) | Plan your work: finish Labs 02 and 07 inside the trial and take screenshots early |
| Microsoft Intune | Microsoft Intune/Microsoft 365 trial (30 days typical) or Microsoft 365 Developer Program sandbox if you are eligible | Used for the Windows endpoint labs |
| Atlassian | Free plans for Jira, Confluence, Jira Service Management | Small user/agent limits; fine for a lab |
| Bitwarden | Free account; org trial for team features | Or any password manager you prefer |
| Cloudflare Zero Trust | Free plan | Hands-on analog for Zscaler concepts |
| Zoom | Free (Basic) | Enough for SSO/licence concepts |
| Jamf | Trial requires an Apple device to enrol | Design-only unless you have access to a real Mac. Do **not** run macOS on non-Apple hardware (licence violation) |

## 2. Windows test machine
You need a throwaway Windows device to enrol, so you don't manage your daily PC.
- Windows 10/11 **Pro or Enterprise** host: enable **Hyper-V** (Turn Windows features on or off → Hyper-V, reboot).
- Create a VM from Windows 11 Enterprise evaluation ISO (Microsoft Evaluation Center). Give it 4 GB RAM, 60 GB disk, TPM enabled.
- On Windows Home: use VirtualBox or VMware Workstation Player instead.
- Take a VM checkpoint named `clean-install` so you can reset and re-enrol.

## 3. Naming and conventions (use these everywhere)
- Company: Northwind Labs. Test users: `ana.ruiz`, `sam.lee` (manager), `priya.nair` (finance), `tom.becker` (to be offboarded), `lina.cho` (IT).
- Groups: `dept-engineering`, `dept-finance`, `dept-sales`, `dept-it`, `role-admin-it`.
- Admin accounts are separate from daily accounts (`lina.cho` vs `adm-lina.cho`).

## 4. Safety rules for the lab
- Never use real employer or customer data.
- Enable MFA on **your own admin accounts first**, and store recovery codes offline.
- Keep a break-glass admin account that bypasses SSO, documented in Lab 08.
- Blur sensitive data in screenshots before committing.
