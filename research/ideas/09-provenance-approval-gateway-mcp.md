# 09 · Provenance re-check + approval gateway (MCP server)

**Track:** Infrastructure for agents.
**One line:** An MCP server any agent can call to (a) record where each fact came from and re-check it on demand, and (b) approve, hold or block each side effect before it happens, exactly once.

## Pieces
- **`record_fact`:** stores source URL or API response, exact field, retrieval date and hash.
- **`recheck_fact`:** re-fetches and reports whether the fact still holds ("carrier's registration still active today?").
- **`request_action`:** payment or email with an idempotency key; held until a person approves; survives restarts.
- **Cost ledger tool:** each call's tokens, credits and ₹.

## Why it matters
This is the backbone the handbook itself mentions (evidence ledger + human sign-off gate). On its own it's harder to name a buyer, so pair it with #01 or #02 and present it as the reusable core.
