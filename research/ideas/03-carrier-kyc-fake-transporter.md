# 03 · Carrier KYC & fake-transporter detector

**Track:** Trust & compliance.
**One line:** Before the 3PL hands a load to a new transporter, prove the transporter is real, active and who it claims to be, and catch impersonators and lookalike brands.

## The problem
- **Fake brokers:** "dummy brokers" collect advance payments under fake company names, then vanish.
- **Impersonation:** Delhi Police (30 Sep 2026) busted a gang impersonating logistics companies and promising truck bookings.
- **Industry warnings:** rising cargo theft, identity fraud and double-brokering (Oct–Nov 2026).

## Request → result
**Input:** the transporter's onboarding request (name, GSTIN, contact, bank, website, fleet claims).
**Output:** **Clear**, **Refer** or **Reject**, with a dated source for every reason, plus a list of documents to request.

### Checks
1. **Resolve the legal entity:** Crustdata company identify plus a registry lookup. If more than one company matches, stop and ask rather than guess.
2. **Activity signals:** headcount trend, web traffic, job posts, news.
3. **Lookalike detection:** "Delhivary Logistics" vs Delhivery; domain registration age; email domain vs website.
4. **Directors and owners:** screen against the news; clear namesakes rather than flag them.
5. **Fleet-claim plausibility:** "500 trucks" vs company size.
6. **Bank account name** vs legal name (penny drop only in live mode; otherwise cannot verify).

## Hard cases
- A real brand with a fake domain → **Reject**.
- A namesake director → cleared, with the evidence that it's a different person.
- A brand-new legitimate company with a thin footprint → **Refer**, not Reject. This is the fairness point.

## Ethics
- Personal data on directors is limited to what's needed and never published.
- Thin-footprint small transporters aren't auto-rejected.

## Finance
- **Price:** per onboarding check (e.g. ₹500–2,000), or a monthly fee for continuous re-checks.
- **Buyer:** a 3PL's procurement or risk team.

## Risks
- Harder to show rupees saved than #02. Best used as a module inside #02.
