# Situation monitor

- Repository: https://github.com/aeiouvcode/situation
- Live: https://aeiouvcode.github.io/situation/

## Inspiration

A @levelsio post sent 2026-09-23 with "How do i do the same" - read as a personal dashboard: stacked revenue per product per year, margin, other metrics.

## References

- The @levelsio dashboard post (X, 2026-09-23 20:52). Exact URL in chat history.

## Findings

- One file: warm paper/charcoal/serif, load a CSV (year,kind,name,value), forecasts the current year.
- Data stays encrypted in the browser and never touches the repo; the public page ships sample data only.
- Side thread: everything he ships is free; charging on 1-2 products was suggested and he has not acted on it.

## Technical decisions

- Local-first encrypted metrics dashboard, no backend.

## Gaps

_None known._
