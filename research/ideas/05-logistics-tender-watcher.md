# 05 · Logistics tender watcher

**Track:** Research & markets.
**One line:** Pull logistics and warehousing tenders posted after 1 Sep 2026 from government procurement portals, tell the 3PL which it qualifies for, and show who won similar tenders before.

## Request → result
**Input:** "Which tenders can we bid on this month?" plus the client's capabilities.
**Output:** each eligible tender with deadline, value, eligibility match (each criterion sourced), and similar past awards. If the source can't settle it: cannot verify, or name the false premise.

## Data
Government e-procurement portals, company data for competitors.

## Hard cases
- A tender has been extended or cancelled → use the latest dated notice.
- A question built on a false premise ("the Pune tender closes Friday" when it closed last week) → say so, with the source.

## Risks
**Check bot access first:** government portals often use captchas. If blocked, this idea dies.

## Finance
Subscription per month, or a success fee on won bids.
