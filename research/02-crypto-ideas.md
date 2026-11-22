# Round 2: crypto and MetaMask

| Idea | MetaMask's role | Main risk | Status |
| --- | --- | --- | --- |
| Proof of Team | Refund or hold a listing deposit on Sepolia | Team-data coverage, anonymous teams | Shortlisted |
| Grant milestone agent | Release each tranche | Similar projects, e.g. [GrantGuard](https://hackquest.io/projects/GrantGuard) | Parked |
| Fake-developer screen | Hold contractor payroll | High harm from a wrong accusation | Parked |
| Investing agent | Testnet swaps | No provable edge, crowded, exchanges are not the buyer | Rejected |

## Proof of Team

An agent reviews a listed token (keep, monitor, delist, or cannot verify), writes the committee memo, and acts after approval.
The refundable-deposit flow is our model, not a confirmed exchange process.
[Elliptic](https://www.elliptic.co/products/asset-due-diligence/) already sells token due diligence.

## Signal test: public GitHub commits

Binance [updated its tags on 20 November 2026](https://blockchainreporter.net/binance-monitoring-tag-six-tokens/).
Windows compared: 21 August to 19 November, in 2025 and in 2026.

| Token | GitHub organisation | Binance action | 2025 | 2026 | Change |
| --- | --- | --- | ---: | ---: | ---: |
| ZIL | Zilliqa | Monitoring added | 162 | 286 | +77% |
| ONE | harmony-one | Monitoring added | 2,623 | 1,879 | -28% |
| INIT | initia-labs | Monitoring added | 842 | 83 | -90% |
| MITO | mitosis-org | Monitoring added | 73 | 0 | -100% |
| THE | ThenafiBNB | Monitoring added | 0 | 0 | no data |
| BANK | Lorenzo-Protocol | Monitoring added | 7 | 2 | -71% |
| MORPHO | morpho-org | Seed tag removed | 1,365 | 3,192 | +134% |
| HYPE | hyperliquid-dex | Seed tag removed | 43 | 0 | -100% |

A "down more than 50%" rule catches three of six flagged tokens and wrongly flags HYPE, so GitHub alone is not enough.

Limits:

- One organisation per project, and the THENA organisation is unconfirmed.
- Bot commits are not separated, and private work is invisible.
- Removing a Seed tag does not prove a project is healthy.
- Eight cases are too few to tune on.
- A demo replay must be computed live, using only facts dated before the cutoff.
