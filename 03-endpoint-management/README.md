# Lab 03: Endpoint Management

**Objective:** Enrol devices, enforce a security baseline, and report on compliance.

Two tracks: **Intune (hands-on on Windows)** and **Jamf (design-only unless you have a Mac)**.

## Track A: Intune with a Windows VM (hands-on)
1. **Tenant setup:** assign Intune licences to test users; set MDM authority. 📸 `03/intune-licences.png`
2. **Enrol the VM:** join it to Microsoft Entra ID (Settings → Accounts → Access work or school → Join this device to Microsoft Entra ID). Confirm it appears in Intune → Devices. 📸 `03/intune-device-enrolled.png`
3. **Compliance policy:** require BitLocker, firewall on, Defender on, minimum OS version, password/PIN. 📸 `03/intune-compliance-policy.png`
4. **Configuration profile:** screen-lock timeout, disable USB autorun, set a wallpaper or similar visible change to prove delivery. 📸 `03/intune-config-profile.png`
5. **App deployment:** deploy one required app (e.g. 7-Zip or Zoom) as a Win32/Store app; verify install on the VM. 📸 `03/intune-app-deployed.png`
6. **Make it non-compliant on purpose:** turn off the firewall; watch the device flag as non-compliant; fix; watch it return. 📸 `03/intune-noncompliant.png`
7. **Conditional access hook:** require a compliant device for Google Workspace via Okta device assurance or Entra CA (document what your tenant allows). 
8. **Remote actions:** sync, restart, retire/wipe the VM; re-enrol from the `clean-install` checkpoint.

## Track B: Jamf Pro for macOS (design-only 📝 unless you have an Apple device)
Write the design in [`jamf-design.md`](jamf-design.md): Apple Business Manager + Automated Device Enrolment, PreStage, smart groups, FileVault escrow, config profiles, patch policy, compliance reporting. Label this clearly as design, not experience.

## Verification checklist
- [ ] VM visible in Intune with correct primary user
- [ ] Non-compliant → compliant cycle captured
- [ ] Wipe and re-enrol tested

## Production notes
Zero-touch (Autopilot / ADE) so devices ship direct to users; separate pilot ring before broad deployment; OS update rings; lost-device runbook; asset inventory reconciled monthly.

## Talking points
Compliance policy vs configuration profile, why encryption key escrow matters, how you stage risky policy changes.
