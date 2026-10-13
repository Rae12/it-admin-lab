# Zscaler Design (Design Only 📝)

| Element | Design |
|---|---|
| Identity | Okta SAML/SCIM: users and groups provisioned automatically |
| Client | Zscaler Client Connector deployed by Intune (Windows) and Jamf (macOS) |
| Internet access (ZIA) | URL filtering by category, malware/phishing protection, TLS inspection with documented exclusions (banking, healthcare, pinned apps) |
| Private access (ZPA) | App segments per internal tool; access by group; no inbound firewall rules |
| Policy rollout | Monitor/log-only for 2 weeks → warn → block; pilot with IT, then each department |
| Exceptions | Ticketed, time-boxed, approved by security owner, reviewed monthly |
| Logging | Forward logs to SIEM/storage; weekly review of blocked categories |
| Break-glass | Documented bypass for outages, reviewed after use |

## Rollout risks
TLS inspection breaking apps; latency; user pushback. Mitigate with pilot, exclusions list, comms and a Confluence FAQ.
