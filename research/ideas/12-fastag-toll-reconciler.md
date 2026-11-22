# 12 · FASTag / toll reconciler (the "dumb" one)

**Track:** Buying & paying.
**One line:** Match bank or FASTag statement lines like "NETC FASTAG ₹845" to actual trips, and flag tolls with no trip, double charges and wrong vehicle classes.

## Request → result
**Input:** FASTag statement, trip log.
**Output:** each line → **Matched trip** / **Duplicate, held** / **No trip, held for a person** / **Cannot verify**.

## Hard cases
- Two charges at the same plaza within minutes → possible double charge.
- A vehicle-class mismatch (charged as a larger truck than the one on the trip) → refund claim drafted for approval.

## Why keep it
Tiny, very concrete, and easy to demo. Best as a module inside #02.
