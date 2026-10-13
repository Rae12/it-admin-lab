# Practice Ticket Queue

Work each ticket in your lab. Record: root cause, steps taken, time spent, KB article created.

| ID | Priority | Ticket | What to do |
|---|---|---|---|
| T-01 | P2 | "I got a new phone and can't pass MFA" | Reset Okta factor after identity verification; document the verification steps |
| T-02 | P3 | "Can't access shared Finance drive" | Check Google group membership vs access matrix; fix via group, never direct share |
| T-03 | P3 | "My laptop says non-compliant and I can't open Google" | Find failing policy in Intune; guide user to fix (turn firewall on); verify |
| T-04 | P4 | "Need a Zoom licence" | Approval workflow → Okta group → verify licence |
| T-05 | P1 | "Nobody in Sales can sign in" | Investigate Okta System Log, find a policy/app change, roll back, write a post-incident note |
| T-06 | P2 | "Got a suspicious email, clicked the link" | Security incident: reset password, revoke sessions, review sign-in logs, check mailbox rules, document |
| T-07 | P4 | "New hire starts Monday" | Run onboarding SOP (Lab 07) end to end |
| T-08 | P4 | "Tom left Friday" | Run offboarding SOP (Lab 07) end to end |
| T-09 | P3 | "Can I install Docker on my laptop?" | Check software policy; approve or deny with reasoning; record the exception |
| T-10 | P2 | "Please give me admin on Jira" | Evaluate least-privilege alternative; require manager + owner approval; time-box if granted |

After completing the queue, compute SLA performance and identify the top 3 candidates for automation.
