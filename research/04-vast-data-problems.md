# Round 4: business problems that need vast people and company data

The test for this list: **the answer does not exist in any one record.** It appears only after scanning or comparing thousands.

The problem statement PDF gives every team a fictional mid-size Indian 3PL (third-party logistics company) as client.
The top three work for that client and as standalone businesses.

## 1. Shadow Manifest: rebuild rivals' customer lists from job posts

> "Find shippers we can win from Delhivery and Blue Dart this month."

Shippers name their logistics providers when they hire ("manage Delhivery, Blue Dart and Shadowfax"). One post is trivia.
Every post in India is a map of who uses whom.

1. Search the last 30 days of job descriptions for each rival's name (exact-phrase match on `content.description`).
2. Remove the rivals' own posts, recruiters and "experience with X preferred" mentions.
3. Resolve each employer to one company, then score size, growth, new cities and signs of switching.
4. Find the owner of the logistics budget and write a proposal priced from the client's rate card.
5. After approval, book the meeting with a teammate playing the buyer, exactly once.

- **Tracks:** Revenue (meetings on triggers from the last 30 days), plus Research and markets.
- **Paid today:** sales-development agencies and market research firms.
- **Illustrative price:** ₹15,000 per accepted opportunity. Validate before pitching.
- **Estimated data cost:** about 70 to 100 credits per run (1,000 posts at 0.03, plus 20 enrichments at 2, plus lookups). Not measured.
- **Evidence so far:** search snippets showed Cult.fit and Purplle postings naming specific carriers. The pages returned 403 to our fetch, so neither the text nor the dates are confirmed.
- **Hard cases:** a recruiter posting for a hidden client, an agency or aggregator, a past-employer mention, an old repost, a namesake.
- **Ethics:** company-level public evidence, one business contact per account, no outreach without approval.
- **Competition:** job-post technographics exist (TheirStack), and trade-data firms such as Descartes sell shipper intelligence. Generic outbound agents are crowded.
- **Kill test (15 min):** at least 15 distinct Indian shippers across five rivals in 30 days, and at least 8 of a random 10 are real relationships.

## 2. Three Quotes: catch suppliers who are secretly connected

> "Here are three quotes and our vendor master. Can we award this?"

Compare every bidder's founders and staff with each other and with the client's procurement team.
Return award, hold or cannot verify, with the connection path.

- **Tracks:** Trust and compliance, plus Buying and paying.
- **Paid today:** forensic audit and investigation firms.
- **Why it needs scale:** 500 vendors is 124,750 possible pairs, before counting people.
- **Hard cases:** namesakes, large shared ex-employers, declared group companies. A link is a reason to review, never proof of fraud.
- **Kill test:** people data exists for at least 6 of 10 small Indian transporters. This is the likely failure point.

## 3. Canary: spot the customer who will not pay

> "We give 600 shippers 60-day credit. Whose limit should change this week?"

Compare each customer's headcount, hiring, finance-team exits and news with its peers, then draft the credit decision.

- **Tracks:** Insurance, plus Trust and compliance.
- **Paid today:** credit insurers and credit-rating firms.
- **Why it needs scale:** a 10% headcount drop means nothing until it is compared with the whole sector.
- **Hard cases:** seasonal staffing, acquisitions, stale profiles. Data signals alone never cut credit.
- **Kill test:** signals separate five known distressed Indian companies from five healthy peers.

## More problems of this shape

| Problem | The scan it needs | Who pays | Catch |
| --- | --- | --- | --- |
| No-poach cartel detection | Hiring flows between every pair of rivals, looking for missing flows | Antitrust law firms | Absence is not proof of agreement |
| Team-raid evidence | All departures over years, against peer baselines | Employment litigators | Needs internal evidence too |
| Auditor revolving door | Audit-firm alumni in finance roles across audit clients | Audit committees, regulators | Engagement-team membership is private |
| Interlocking directors | Every director across every pair of competitors | Antitrust counsel | Board data is partial |
| Insider-trading links | Traders against insiders, via employers and schools | Brokers, exchanges | Very sensitive personal data |
| M&A buyer list | Every plausible acquirer, its deals and its gaps | Investment banks | Crowded |
| Commercial due diligence | A target's ex-staff, customers and every competitor | Private equity | Interviews still matter |
| Site selection | Talent supply against hiring demand in every city | Companies opening offices or warehouses | Blue-collar coverage is weak |
| Hidden supplier concentration | Vendors' own vendors, inferred from posts and tools | Banks, large buyers | Inference only |
| Missing pension or class members | Thousands of former employees to current employers | Plan and settlement administrators | Identity errors, privacy |

## Scale limits

- Person and job search return up to 1,000 results per page.
- Job search supports count and group-by aggregations, so some market-wide questions need no rows.
- 15,000 credits buys about 500,000 basic search results, about 65,000 people when filtering on and returning experience (0.23 each), or 7,500 company enrichments.
- Default limits are 30 searches and 15 enrichments a minute, so search wide and enrich only finalists.
- Batch jobs need an enterprise plan, so do not design around them.
