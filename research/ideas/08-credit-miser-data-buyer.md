# 08 · Credit-miser data buyer

**Track:** Agents that spend.
**One line:** Buy only the data a job needs, inside a budget the client can cut mid-run.

## Request → result
**Input:** "Find 50 D2C brands in Bengaluru that need warehousing, within X credits."
**Output:** the answer plus a spend report, e.g. "used 412 of 500 credits; stopped enriching at #38 when the budget was cut".

## Mechanics
- Free endpoints first (autocomplete, identify), then cheap search, enrichment only when a fact changes the decision.
- Respect rate limits (30/15/10 requests per minute from the handbook) and back off on HTTP 429.
- A live budget-cut event shrinks the plan and returns partial but honest results.

## Risks
Clever, but hard to sell as a business on its own. Better as a module inside other ideas.
