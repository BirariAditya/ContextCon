# 06 · Goods-in-transit underwriting

**Track:** Insurance.
**One line:** For a new shipper (or a single truckload), check the application against outside records, then quote, refer or decline, with a source for every reason.

## Request → result
**Input:** shipper application (company, cargo type, declared value, lanes).
**Output:** **Quote** (with premium logic), **Refer** or **Decline**, with each risk factor sourced:
- the company is real and active;
- size matches what it declared;
- news shows no fire or fraud history;
- route weather and theft-hotspot news.

## Dumb-but-useful version
A per-truckload risk quote from cargo type, live route weather and recent theft news on the lane.

## Hard cases
- Declared size far above what the records show → **Refer**.
- No news either way → not "safe", but cannot verify.

## Risks
- Pricing logic is hard to justify without actuarial data; keep it rules-based and transparent.
