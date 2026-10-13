# Lab 09: Automation & AI-Driven Process Improvement

**Objective:** Find manual, repetitive work, evaluate solutions, implement at least one, and measure the result.

## Process
1. **Inventory:** use the ticket data from Lab 05 and SOP timings from Lab 07. Fill in [`automation-backlog.md`](automation-backlog.md).
2. **Score** each candidate: frequency × time per occurrence × risk reduction ÷ effort.
3. **Pick one to implement.** Good lab options:
   - Okta group rules: department attribute → groups → app access (removes onboarding steps)
   - Jira Automation: auto-route requests, SLA reminders, offboarding checklist subtasks
   - Okta Workflows or webhook (if available on your plan) to create a Jira ticket on user suspension
   - Scheduled access review reminder
4. **Implement and document:** screenshots, config, rollback plan. 📸 `09/automation-before.png`, `09/automation-after.png`
5. **Measure:** fill the results table in the backlog.
6. **AI use-case evaluation** (design): see [`ai-evaluation.md`](ai-evaluation.md).

## Talking points
How you choose what to automate (and what not to), how you avoid breaking things (pilot, rollback, monitoring), how you quantify impact.
