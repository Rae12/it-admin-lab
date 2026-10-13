# Role-Based Access Matrix

● = assigned by default | ○ = on request with approval | – = none

| Group / Role | Okta | Google | Jira/Confluence | Zoom | Password mgr vault | Finance drive | Admin rights |
|---|---|---|---|---|---|---|---|
| dept-engineering | ● | ● | ● | ● | Shared-Engineering | – | ○ (time-boxed) |
| dept-finance | ● | ● | ○ | ● | Shared-Finance | ● | – |
| dept-sales | ● | ● | ○ | ● | Shared-Sales | – | – |
| dept-it | ● | ● | ● | ● | Shared-IT | – | ● (separate admin account) |
| contractors | ● (expiry date) | limited OU | ○ | ○ | – | – | – |

**Rules:** access assigned via groups only; every exception has a ticket, approver and expiry; admin accounts are separate from daily accounts.
