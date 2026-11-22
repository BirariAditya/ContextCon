# Constraints on the choice

Updated 12:06 IST, 22 November, after reading the problem statement PDF.

## The official documents disagree

| | Builder Handbook and live dashboard | Problem statement PDF and participant rulebook |
| --- | --- | --- |
| Client | Any; none is specified | One fictional Indian 3PL for every team (problem statement) |
| Repository | New public repository | Organiser repository received at kickoff |
| Requirement change | Not mentioned | At hour 3, so about 1:15 PM for a 10:15 start (problem statement) |
| Testing | Video review | Hidden test set, unseen request, kill and restart (problem statement) |
| Scoring | Execution 25, facts 20, robustness 20, value 20, demo 15 | Live run 20, robustness 15, design 15, ethics 25, finance 25 (problem statement) |
| Finals | 2-minute demo, 1 minute of questions | 12-minute slot with a 5-minute live fix (problem statement) |
| Own idea | Allowed | Open track needed 3 test cases by 11:00 AM (problem statement) |

The teammate README says both sources agree on the 3PL client. The handbook does not mention one.

## Confirm with organisers

1. **Which document governs?**
2. **Where are the kickoff kit, client records and organiser repository?**
3. **When does submission open?** The handbook says 2:30 PM and the live dashboard says 4:30 PM. Both put code freeze at 6:00 PM.
4. **What Crustdata output may appear** in a public repo or video?

Public APIs: the problem statement permits any live source, including registries, public APIs and web search.

## Effect on earlier rankings

If the problem statement governs, OfferSure, Objection and Proof of Team do not serve the client and should be dropped.

## Design consequences

- The service must accept unseen requests, with no stored results or hard-coded answers.
- Every team member must understand the code well enough for a live fix.
- Teammates play every counterparty. No agent contacts a real person.
- Payments and other irreversible actions wait for approval and use test mode.
- Keep limits, rules and output fields in config, ready for a requirement change.
- Keep keys, personal data and raw Crustdata records out of this public repository.
- Credit open-source dependencies in the project README.
- Never edit history, timestamps, logs or cost records.
