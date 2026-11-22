# Round 3: out-of-the-box ideas

## 1. OfferSure: insurance against a revoked job offer

> "Here is my offer letter. I join in July. Cover me for ₹1 lakh if they revoke it."

**Replaces:** the underwriter and the claims adjuster.
**Buyers:** insurers, college placement cells, and students through them.

1. Read any offer letter and resolve the employer.
2. Check that the employer is real and the named signatory works there (Company Identify, Person Search).
3. Underwrite on headcount trend, funding age, hiring and layoff news (Company Enrich, Job Search, Web Search).
4. Quote, refer or decline with dated reasons, then issue the policy.
5. On a claim, check the revocation, the waiting period and what was public before purchase.
6. After a person approves, MetaMask sends test USDC on Sepolia. A policy ID can be paid only once.

**Two-minute demo:** a genuine offer gets a quote, a forged one is held, a teammate playing HR revokes the genuine one,
the claim is approved and paid, and a repeated claim is blocked.

**Hard cases:** forged letter, signatory who left, self-withdrawal dressed as revocation, deferred joining,
purchase after layoffs became public, namesake employer.

**Risks:**

- A revocation is rarely public, so a claim needs employer confirmation or goes to a person.
- A missing profile is not evidence of fraud. Refer it instead of declining it.
- Prices are illustrative until there is loss data.
- Production needs a licensed insurer and rupee payouts. Testnet USDC is only the demo rail.

**Competition:** job-loss cover exists ([SafetyNet](https://siliconprairienews.com/2017/12/madison-based-insurtech-startup-safetynet-launches-new-insurance-program/)).
A quick search found no product for rescinded offers.

**Kill test (30 min):** three stable and three troubled employers must separate, and four of six known signatories must resolve.

## 2. Objection: challenge the company that beat you

> "We lost this small-business contract. Is the winner really small?"

**Replaces:** the first billable hours of a government-contracts lawyer.
**Buyers:** losing bidders and their law firms.

1. Pull the award from USAspending.
2. Resolve the winner, its parents, shared executives and possible affiliates with Crustdata.
3. Apply the size standard for the award's industry code.
4. Return "no grounds", "cannot verify", or a cited protest draft with the filing deadline.

**Why it is strong:** any live award is an unseen request. The public API needed no key and returned awards starting as late as 21 November 2026.
Evidence matters, because [protests without it get dismissed](https://smallgovcon.com/sba-size-protests/oha-says-for-a-size-protest-bring-the-receipts-or-face-dismissal/).

**Risks:**

- Many standards use average revenue, which Crustdata only estimates. Start with employee-based manufacturing standards.
- Affiliation is a legal judgement, and only eligible parties can protest.
- The window is often five business days. Confirm against [13 CFR 121.1004](https://www.law.cornell.edu/cfr/text/13/121.1004).
- SBA [proposed new size standards in August 2026](https://www.hklaw.com/en/insights/publications/2026/08/sba-proposes-sweeping-overhaul-of-small-business-size-standards).
- A real violator may not turn up today.

## 3. Vesting Police: stop paying tokens to people who left

> "Here are our 40 token-vesting streams and the contributor agreements. Fix what is wrong."

**Replaces:** token-operations administrators.
**Buyers:** crypto companies, foundations and exchanges that grant tokens.

Detect a departure or role change, apply the agreement, calculate vested and unvested tokens, draft the notice,
and after approval cancel the stream through MetaMask on Sepolia.

**Risks:**

- Profiles lag, and departed staff may remain advisers. A profile change opens a case and never cancels by itself.
- The customer's HR system may already know, which weakens the need for Crustdata.

## The wider pool

Competition and data are unchecked unless noted.

### Money nobody is collecting

| Idea | Request to finished work | Catch |
| --- | --- | --- |
| Orphaned Money | Renamed or acquired company to an unclaimed-funds claim for its successor | Recovery firms exist. California's download page returned 403 in our test |
| Earn-Out Referee | Acquisition milestones to a dispute memo on whether they were met | Deal terms are private |
| Claims Buyer | Bankrupt company's creditor list to priced offers for their claims | Data is hard to get in a day |
| Referral Collector | Past introductions to finder-fee invoices once the hire or deal happened | Attribution |

### Agents for the underdog

| Idea | Request to finished work | Catch |
| --- | --- | --- |
| Counter-Offer | Offer letter to a negotiated offer, using the employer's hiring urgency | A teammate must play the employer |
| WARN Watch | Layoff to a missing-notice check and claim brief | Headcount cannot prove a site-level layoff. California's WARN file is downloadable |
| Placement Truth | College placement claims to a cited audit for an education lender | Alumni coverage is partial |
| Creditor's Alarm | Customer list to a stop-shipment notice before a customer collapses | Close to credit monitoring |

### Endings as a service

| Idea | Request to finished work | Catch |
| --- | --- | --- |
| Soft Landing | Dying startup to ranked acqui-hire buyers, teaser and simulated term sheet | Success takes months to prove |
| Startup Undertaker | Shutdown decision to staff placements, notices and asset sale | SimpleClosure works in this area |
| Office Vulture | Shrinking companies to priced buyout offers for their furniture | Weak proof of intent |
| Key-Person Cover | Fund or lender agreement to a notice when a named executive leaves | Agreements are private |

### Is this person who they say they are?

| Idea | Request to finished work | Catch |
| --- | --- | --- |
| Confirm | Auditor's receivables to completed confirmations from verified signatories | Confirmation.com exists |
| Fake Boss | Urgent payment request to pay or block after checking the requester's role | Close to the payables sample |
| Logo Police | "Trusted by" wall to evidence of false customer claims and a takedown | Absence of evidence is weak |
| Critical Role | Career history to an evidence pack for an O-1 visa | Immigration services are crowded |

### Crypto, sideways

| Idea | Request to finished work | Catch |
| --- | --- | --- |
| DAO Proxy Adviser | Grant proposal to a team check and signed Snapshot testnet vote | Small buyer pool. The testnet hub responded in our test |
| Rug Cover | Token holding to a parametric payout when the team disappears | Easy to game |
| Founder Bond | New listing to a bond released while the named team stays | No existing buyer |
