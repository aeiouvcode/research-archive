# NoCatch

- Repository: https://github.com/aeiouvcode/nocatch
- Live: https://aeiouvcode.github.io/nocatch/

## Inspiration

There's An AI For That (TAAFT), as a free and serious alternative. It started as a rebuild of a basic AI deal hub (2026-09-17).

## References

_None recorded yet._

## Findings

- Every entry needs a dated usage-limit field: free quota, credits, whether a card is required.
- License labels must be exact. Open source, open weights and closed service are kept separate after mislabelling was caught.
- The target is a few hundred genuinely verified entries, never a scrape.
- A prediction-market layer for AI tools was floated and parked over legal and liquidity concerns.

## Technical decisions

- Official vendor pages are the only source for limits.
- Hash-only CSP, default-src none, zero external assets, no analytics.

## Gaps

- Naming and positioning discussion is in chat history (2026-09-17/18).
