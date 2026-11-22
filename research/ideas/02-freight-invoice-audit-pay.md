# 02 · Freight invoice audit & pay ("PayOnce" / "Bhada")

**Track:** Buying & paying (+ Trust & compliance for the bank-detail fraud checks).
**One line:** Audit every transporter invoice against the contract and the live diesel price, catch duplicates and payment-redirection fraud, and pay the correct amount exactly once.

## The job firms pay for today
- **Who does it:** in-house AP clerks at 3PLs and manufacturers, and outsourced freight audit and payment firms.
- **How it's priced:** outsourced firms often charge a share of what they recover.
- **Comparables:**
  - Lighthouz AI (YC S24): US freight-broker AP, AR and audit.
  - Evos: $9M pre-seed, auditing LTL invoices.
  - Indian SaaS: Fretron, SuperProcure (tools for shippers, not a done-for-you service).

## Request → result
**Input:** a batch of transporter invoices (PDF or CSV), rate cards, the vendor master list.
**Output:** a verdict per invoice:
- **Approve**
- **Short-pay**, with a dispute note
- **Hold**: duplicate
- **Hold**: bank details changed
- **Cannot verify**

Each verdict comes with the amount broken down (base rate + fuel surcharge + allowed extras) and a dated source per fact. Approved invoices are paid in Razorpay/Stripe test mode after a person clicks approve.

### Checks
1. **Extract:** vendor, GSTIN, lane, truck type, weight, consignment note number, charges, bank details.
2. **Vendor match:** confirm the legal entity (Crustdata company identify + vendor master). Flag lookalikes such as "Shree Ganesh Roadlines" vs "Shri Ganesh Road Lines".
3. **Rate:** contract lane rate plus fuel surcharge from the live diesel price (PPAC/IOCL daily page) against the contract's base price.
4. **Duplicates:** same consignment note, amount or date; re-sent invoices with a new number for the same trip.
5. **Bank details:** a change against the vendor master → hold, and draft a callback request to an independently found contact (sandbox only; no real outreach).
6. **MSME deadline:** Section 43B(h) gives 15 or 45 days, so pay invoices close to the deadline first.
7. **Pay:** test-mode payout with an idempotency key, after approval.

## Hard test cases
- The same trip billed twice under two invoice numbers → hold as a duplicate.
- Fuel surcharge computed on an old, higher diesel price → short-pay the difference, with the dated source.
- New bank account sent in the same email as the invoice → hold.
- Lookalike vendor with a different GSTIN → hold; don't merge.
- Lane missing from the rate card → cannot verify, naming the missing rate.

## Data sources to verify in hour 1
- **Crustdata:** company identify/enrich; person search for an independent contact.
- **Diesel price:** PPAC / IOCL pages (scrape, cache, store the date).
- **IFSC lookup API.**
- **GSTIN status:** portals may have captchas; mark "cannot verify" if blocked.
- **Gotcha:** RazorpayX penny drop is not available in test mode, so rely on the callback hold.

## Finance
- **Illustrative maths:** on a ₹50 Cr freight spend, 2% overbilling is ₹1 Cr a year; at a 25% share of recoveries that's ₹25 lakh a year per client.
- **Alternative:** a flat ₹/invoice fee.
- **Cost per invoice:** from the cost ledger.

## Ethics
- No payment, dispute or vendor-master change without approval.
- Never pay a changed account on the strength of the invoice's own contact details.
- Prefer cannot-verify delays to wrong payments.
- Respect MSME deadlines, so automation doesn't starve small transporters.

## Risks
- Requires the client's invoice/rate-card format (released at kickoff); keep extraction swappable.
- Less founder-problem fit than #01.
