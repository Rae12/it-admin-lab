# Lab 04: Zero-Trust Network Access

**Objective:** Understand and document secure internet access and application access policy.

Zscaler requires a commercial agreement, so this lab has two tracks.

## Track A: Zscaler design (📝 design-only)
Complete [`zscaler-design.md`](zscaler-design.md).

## Track B: Hands-on analog with Cloudflare Zero Trust (free plan)
1. Create a Zero Trust organisation; connect Okta as an identity provider (OIDC/SAML). 📸 `04/zt-idp.png`
2. Install the WARP client on your Windows VM and enrol with your org. 📸 `04/zt-warp-enrolled.png`
3. Create a **Gateway DNS/HTTP policy** that blocks a category (e.g. gambling or newly registered domains). Test: blocked page shows. 📸 `04/zt-blocked.png`
4. Create a **device posture check** (e.g. disk encryption on) and require it in an Access policy. 
5. Review logs to see who accessed what. 📸 `04/zt-logs.png`

## Verification
- [ ] Policy blocks the target category for enrolled VM only
- [ ] Policy change takes effect without touching the device
- [ ] Log entry matches your test request

## Talking points
Why VPN-style flat access is risky, how identity + device posture + policy replaces network location as the trust signal, rollout approach (monitor-only first).
