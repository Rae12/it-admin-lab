# AI Use-Case Evaluation (Design)

| Use case | Value | Data involved | Risks | Controls | Decision |
|---|---|---|---|---|---|
| Suggest KB article for incoming ticket | Faster first response | Ticket text (may include PII) | Wrong suggestion, data leakage | Approved vendor/enterprise agreement, redact PII, human approves | Pilot |
| Draft replies to common tickets | Saves time | Ticket text | Incorrect or off-policy answers | Agent reviews every reply | Pilot |
| Summarise long incident threads | Better handoffs | Internal chat/ticket | Confidential data exposure | Approved tool only | Consider |
| Auto-approve access requests | Speed | Identity data | Over-privilege, audit failure | **Do not automate** without policy-based rules and logging | Reject |

## Principles
Human in the loop for decisions affecting access; no credentials or customer data in unapproved tools; measure accuracy before rollout; keep an opt-out and an audit trail.
