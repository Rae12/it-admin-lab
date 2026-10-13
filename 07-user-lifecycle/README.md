# Lab 07: User Lifecycle (Joiner / Mover / Leaver)

**Objective:** Standardise provisioning and deprovisioning, measure it, and then remove manual steps.

## Documents
- [Onboarding SOP](onboarding-sop.md)
- [Offboarding SOP](offboarding-sop.md)
- [Access matrix](access-matrix.md)
- [Quarterly access review](access-review-template.md)

## Exercise
1. **Baseline (manual):** run the onboarding SOP for `new.hire`, timing each step. Run offboarding for `tom.becker`. Record the time and mistakes in the table below. 📸 `07/onboarding-checklist.png`, `07/offboarding-checklist.png`
2. **Audit existing accounts:** list all Okta users, compare to your HR roster (a spreadsheet is fine), and flag orphaned, shared, and over-privileged accounts. 📸 `07/access-review.png`
3. **Optimise:** convert per-user assignments into group-based rules; add Okta group rules based on department attribute; remove redundant steps.
4. **Re-run (after):** onboard another test user and record the new time.

| Metric | Before | After |
|---|---|---|
| Onboarding time (min) | | |
| Offboarding time (min) | | |
| Manual steps | | |
| Errors/missed steps | | |

## Talking points
How you'd make the leaver process meet a 1-hour SLA, handling movers (department change) which is where access creep happens, evidence for auditors.
