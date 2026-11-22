# 04 · D2C expansion-trigger SDR

**Track:** Revenue.
**One line:** Find D2C brands that just raised money or posted warehouse or supply-chain jobs in a new city in the last 30 days. Identify the head of supply chain, write a sourced pitch for the 3PL's warehousing, and queue a meeting request for approval.

## The job firms pay for today
Sales development and lead qualification agencies, paid per meeting booked.

## Request → result
**Input:** e.g. "Find 20 brands likely to need a Bengaluru warehouse this quarter."
**Output:** a ranked list. For each brand: the trigger (funding round, job post, new GSTIN state) with date and source, the decision-maker, a drafted outreach message, and a meeting slot proposal held for approval.

## Data
Crustdata funding, job search and person search; web search for news.

## Hard cases
- A trigger older than 30 days → excluded.
- The person has moved to another company → not contacted; the new person is found.
- A brand already a client in the vendor master → skipped.

## Constraint
`info.md` says the rulebook bans contacting real people. Outreach must go to sandbox recipients, which makes the demo less impressive.

## Finance
Price per qualified meeting (e.g. ₹3,000–8,000), measured against the cost of one run.

## Risks
- Crowded idea at every hackathon (Markit took 2nd at IIT Bombay with a close cousin).
- The ethics judge will push on cold outreach.
