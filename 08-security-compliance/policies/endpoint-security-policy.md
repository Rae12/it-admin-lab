# Endpoint Security Policy

**Version 1.0 | Owner: IT**

1. All company devices are enrolled in MDM (Intune for Windows, Jamf for macOS) before use.
2. Full-disk encryption (BitLocker/FileVault) is required; recovery keys are escrowed in the MDM.
3. OS must be within one major version of current and patched within 14 days of release (critical: 72 hours).
4. Screen lock after 5 minutes; firewall and endpoint protection enabled.
5. Zscaler client must be installed and active on company devices.
6. Non-compliant devices are blocked from company apps after a 24-hour grace period.
7. Lost or stolen devices are reported to IT immediately; IT locks and wipes remotely.
8. Personal devices are not permitted to enrol; web-only access follows the acceptable use policy.
9. Local administrator rights are not granted by default; requests follow the exception process.
