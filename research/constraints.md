# Constraints on the choice

## Confirm with organisers

1. **Is this the right repository?** The participant rulebook requires code in an organiser-provided repository, while the handbook only asks for a new public repository.
2. **Are public read APIs allowed** (GitHub, USAspending, Sepolia RPC)? The rulebook limits agents to the team's environment and permitted APIs.
3. **When does submission open?** The handbook says 2:30 PM and the live dashboard says 4:30 PM. Both put code freeze at 6:00 PM.
4. **What Crustdata output may appear** in a public repo or video?

## Design consequences

- The service must accept unseen requests, with no stored results or hard-coded answers.
- Every team member must understand the code well enough for a live fix.
- Teammates play every counterparty. No agent contacts a real person.
- Payments and other irreversible actions wait for approval and use test mode.
- Keep keys, personal data and raw Crustdata records out of this public repository.
- Credit open-source dependencies in the project README.
- Never edit history, timestamps, logs or cost records.
