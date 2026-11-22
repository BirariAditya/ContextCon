# Research — ContextCon 05 · BITS Pilani

Pre-event planning notes only (allowed by the rulebook: "planning and sketching are allowed"). No project code lives here. Compiled 22 Nov 2026.

## Two rule sources disagree — confirm in the room

| | Problem statement PDF (`ContextCon05_BITS_Problem_Statement.pdf`) | `info.md` (Builder Handbook + Participant Rulebook) |
|---|---|---|
| Finals scoring | Live run 20 · Robustness 15 · Design 15 · **Ethics 25 · Financial feasibility 25** | End-to-end 25 · Facts & verification 20 · Robustness 20 · Customer value 20 · Demo 15 |
| Finals format | 12-min slot: 3-min demo incl. kill on stage, 5-min live fix, design question | 2-min demo + 1-min questions |
| Outreach | Emails to a client wait for approval | **No contacting real people at all** — sandbox recipients only |
| Requirement change | At hour 3 | Not mentioned |

Both agree on: live data for at least one decision, a dated source for every fact, "cannot verify" over guessing, human approval before irreversible actions, recorded time and cost per run, exactly-once actions after a crash, and a fictional **mid-size Indian 3PL** client whose records are released at kickoff.

## Files

- [`past-contextcon-winners.md`](past-contextcon-winners.md): what won earlier ContextCons, and the patterns.
- [`market-and-yc-notes.md`](market-and-yc-notes.md): YC requests for startups, market sizes, competitors.
- `ideas/`: one file per idea, ranked below.

## Idea ranking

| # | Idea | Track(s) | Why it ranks here |
|---|---|---|---|
| 01 | [AI Deployment Approval Desk](ideas/01-ai-deployment-approval-desk.md) | Trust & compliance + Infrastructure for agents | **Top pick.** Founder lived the pain (Nomura). Matches YC's AI-compliance and air-gapped requests. Sourcing rules are the product. |
| 02 | [Freight invoice audit & pay](ideas/02-freight-invoice-audit-pay.md) | Buying & paying | Clearest rupee ROI, and exactly-once payment is the job. A YC company (Lighthouz) already sells it in the US. |
| 03 | [Carrier KYC & fake-transporter detector](ideas/03-carrier-kyc-fake-transporter.md) | Trust & compliance | Real Indian fraud, with lookalike-name hard cases built in. |
| 04 | [D2C expansion-trigger SDR](ideas/04-d2c-expansion-trigger-sdr.md) | Revenue | Best fit for Crustdata data. Weakened by the no-contact rule. |
| 05 | [Logistics tender watcher](ideas/05-logistics-tender-watcher.md) | Research & markets | Live government data. Bot access needs checking. |
| 06 | [Goods-in-transit underwriting](ideas/06-goods-in-transit-underwriting.md) | Insurance | Good "quote, refer or decline" structure. |
| 07 | [Packaging & pallet sourcing](ideas/07-packaging-sourcing-rfq.md) | Supply chain | Simple, concrete, but low novelty. |
| 08 | [Credit-miser data buyer](ideas/08-credit-miser-data-buyer.md) | Agents that spend | Clever budget mechanics; hard to sell as a business. |
| 09 | [Provenance re-check + approval gateway (MCP)](ideas/09-provenance-approval-gateway-mcp.md) | Infrastructure for agents | Could be the backbone of #01 or #02. |
| 10 | [Logistics hiring: layoff-triggered + CV checker](ideas/10-logistics-hiring.md) | Hiring | Works, but personal data makes the ethics answer harder. |
| 11 | [Acquisition scout & partner pitch checker](ideas/11-acquisition-scout.md) | Investing | Weak fit for a 3PL client. |
| 12 | [FASTag / toll reconciler](ideas/12-fastag-toll-reconciler.md) | Buying & paying | Deliberately small idea; could be a module of #02. |

## Must-haves for any idea
1. Job state in SQLite, an idempotency key on every side effect, and resume from checkpoint (the kill test).
2. Rates, rules, limits and output fields in config, so a requirement change or live fix is a config edit.
3. An evidence ledger: each fact with source URL or API response, the exact field or passage, the retrieval date and a hash.
4. A cost ledger: tokens, Crustdata `X-Credits-Used` and ₹ for every call, plus a per-run time and cost ceiling.
5. "Cannot verify: missing X" as a first-class output.
6. Keep raw Crustdata records out of the public repo and video (Data Export Terms, see `info.md`).
