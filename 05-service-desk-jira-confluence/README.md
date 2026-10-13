# Lab 05: Service Desk & Knowledge Base (Jira + Confluence)

**Objective:** Run a small IT service desk with SLAs, escalation and documentation that help desk staff can actually use.

## Steps
1. **Jira Service Management project** (IT Support). 📸 `05/jsm-project.png`
2. **Request types:** Access request, New hire, Offboarding, Hardware issue, Software/licence, Security incident, General question. Add required fields per type (e.g. manager approval on access requests).
3. **Priorities and SLAs:**

| Priority | Definition | First response | Resolution target |
|---|---|---|---|
| P1 | Company-wide outage, security incident | 15 min | 4 h |
| P2 | Team blocked, no workaround | 1 h | 8 h |
| P3 | Individual impact, workaround exists | 4 h | 24 h (1 business day) |
| P4 | Request / low impact | 1 business day | 72 h |

Configure these in JSM SLAs (if limited on free plan, document the config). 📸 `05/jsm-sla.png`
4. **Workflow:** Open → Triage → In progress → Waiting for customer → Escalated → Resolved. Define who can move tickets to Escalated.
5. **Automation rules:** auto-assign by request type; auto-comment when waiting >2 days; remind on SLA at-risk. 📸 `05/jira-automation.png`
6. **Confluence space (IT Knowledge Base):** home page, how-to articles, runbooks, policy index, on-call/escalation page. 📸 `05/confluence-space.png`
7. **Work the practice queue:** resolve the tickets in [`practice-tickets.md`](practice-tickets.md) in your lab; record each fix in the ticket. 📸 `05/jsm-queue.png`
8. **Cross-training:** deliver (or write as if delivering) [`help-desk-training.md`](help-desk-training.md).

## Metrics to track
First-response and resolution SLA %, tickets by type, reopen rate, top 5 repeated issues (feed Lab 09 automation).

## Talking points
How you decide to escalate, how recurring tickets become KB articles then automations, what "within service timelines" looks like in numbers.
