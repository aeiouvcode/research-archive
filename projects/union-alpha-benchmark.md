# Union Alpha benchmark

- No repository - evaluation harness saved
- Status: rerunnable, not yet rerun

## Inspiration

Owner brief (2026-09-17): "Use union alpha model and make a project, compare that model with the internal model on instinct and if i compares better on benchmarks, use that to do most of coding tasks." A real bakeoff with consequences: the winner gets his coding errands. He supplied an OpenRouter key.

## References

_None recorded yet._

## Findings

- Harness: 8 identical coding fixtures (parser, bug fix, game mechanic, async refactor, SQL, route compiler, interval algorithm, React repair), deterministic tests, blind A/B scoring, synthetic fixtures only so nothing private reaches an anonymous provider.
- 2026-09-17 result: Instinct 100/100, Union Alpha unscored - every run hit the free pool's 429 wall. No winner, no switch.
- A parallel subagent probe to unmask the stealth model was inconclusive - it gave up nothing.
- 2026-09-18: rate limits cleared because the cloak came off (it is Unbiased's Pareto router). The benchmark is rerunnable and not yet rerun.

## Technical decisions

- Synthetic fixtures only, blind scoring, deterministic tests.

## Gaps

- Rerun pending.
