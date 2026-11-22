# 01 · AI Deployment Approval Desk ⭐ top pick

**Tracks:** Trust & compliance + Infrastructure for agents (the rules allow joining 2).
**One line:** Give it an AI agent's repo and its intended use, and it returns a finished, evidence-linked AI risk and approval pack plus a ready-to-file change request. Months of compliance back-and-forth shrink to one run.

## Origin (founder-problem fit)
At Nomura, deploying an internal agent service meant:
- filling an AI compliance form that senior management had to sign;
- an audit run in ServiceNow;
- test and final runs that stretched to **about a year** before the service could go on the firm's internal network.

Raising a change ticket was its own painful process, and the internal browser tooling was too complex to automate. Open the pitch with this story.

## The job firms pay for today
- **Internal model-risk and IT-risk teams** spend 100+ hours per model writing documentation.
- **Big-4 / consultancy AI risk assessments** and model validation.
- **ServiceNow implementation partners** who run change management.
- **Buyer:** head of IT risk or CISO at a mid-size company; later, model-risk teams at banks and NBFCs.

## Fit to the fictional 3PL client
The 3PL wants to deploy AI agents (every other ContextCon team is building one for it). Before any agent goes live, it needs a DPDP- and RBI-style risk review plus a change ticket. The service clears agents for deployment.

## Request → result
**Input:** a repo URL plus one line of intended use (e.g. "agent pays transporter invoices").
**Output:**
1. **A risk tier:** light, standard or full review.
2. **A filled risk form.** Every field is answered from evidence and labelled **Verified / Contradicted / Cannot verify**.
3. **A draft change request** with risk, rollback plan, test evidence and approvers.
4. **Approval routing.** Submitting and approving are irreversible, so a named person must do them.

### Pipeline
1. **Inventory:** models called, external APIs, data in and out, secrets handling, storage.
2. **Classify:** personal data (DPDP)? Moves money? Contacts outsiders? From that, pick the tier.
3. **Evidence per field.** Examples:
   - "Stores PII?" → the exact line in the schema file.
   - "Human approval before payment?" → the approval function plus a log line showing it ran.
   - "Model provider retains data?" → the provider's live policy page with retrieval date.
4. **Live checks:**
   - dependency vulnerabilities from OSV.dev (or NVD);
   - software licences;
   - vendor companies verified via Crustdata company identify;
   - vendors' data-processor lists fetched live.
5. **Run the agent's own tests** and attach the results.
6. **Create the change request** via the ServiceNow Change Management REST API (`POST /api/sn_chg_rest/change/normal`) on a free developer instance. No UI scraping.

## Hard test cases
- **README says one thing, code does another:** "PII is masked" but the code logs raw phone numbers → **Contradicted**, both sources linked.
- **Unmentioned retention:** the model provider allows data retention and the README never mentions it → flagged.
- **No rollback plan** anywhere → **Cannot verify**, and the change request is blocked from submission.
- **Lookalike package:** a typo-squatted dependency name → held.
- **Requirement change:** organizers add a mandatory form field → edit the form template in config, no code change.

## Robustness (kill test)
- Each pack is a state machine stored in SQLite.
- Creating the ServiceNow change uses an idempotency key (repo commit hash + pack version).
- Restart resumes from the last state, and exactly one ticket ever exists.

## Ethics answer
- **Never fabricates evidence.** Cite the Delve case, where a $300M company was accused of fake audit evidence and dropped by YC.
- **Reads code and metadata only.** It flags personal data, never copies it into the pack.
- **People approve; the agent prepares.**
- **No real-world contact.** Approver notifications go to sandbox recipients, per the rulebook.

## Finance answer
- **Price:** per approval pack, e.g. ₹50,000, against ₹2–4 lakh of analyst and consultant time. These numbers are illustrative and must be defended.
- **Cost per run:** measured from the cost ledger; expect tens of rupees.
- **The real sell:** months off time-to-production.
- **Why now:** DPDP obligations apply from 13 May 2027, and the RBI FREE-AI framework expects board-approved AI policies.

## Why YC
- **Fall 2026:** "AI compliance infrastructure" and "software for regulated industries".
- **Winter 2027:** "AI for the Air-Gapped Economy". The bank version runs on-prem or as an MCP server inside the network.

## Risks
- **Hidden tests follow the 3PL's requests.** Confirm at kickoff that this counts as a client request, or use the Open track (it requires 3 test cases by 11 AM).
- **ServiceNow could build this.** Position: we plug into ServiceNow and do the work its dashboard doesn't.
- **Bank sales are slow.** Lead with Indian mid-market companies facing the DPDP deadline.

## Demo (2–3 min)
1. Paste another team's repo.
2. The pack fills live: green means sourced, red means contradicted, grey means cannot verify.
3. Approve, and a real ticket appears in the ServiceNow dev instance.
4. Kill and restart: still exactly one ticket.
