# Open Muse

- Repository: https://github.com/aeiouvcode/open-muse
- Live: https://aeiouvcode.github.io/open-muse/

## Inspiration

Meta's Muse agent concept: a personal agent that takes work off your plate. Brief (2026-09-18): build an open-source version that works everywhere, with no region lock.

## References

- THUNLP ProactiveAgent (GitHub): patterns for proactive, unprompted assistance.
- kayba-ai/recursive-improve (GitHub): the self-improvement loop pattern (branch per experiment, failed-attempt log, hard gates, keep or revert).
- OpenViking: tiered filesystem memory, used as the memory spine.
- Mem0: fact-extraction pattern for memory.
- supermemory: considered and left out because it would break on-machine operation.
- Amp orbs: persistent remote machines, the model for work that outlives a session.
- AgentCloak Desktop: the privacy-cloak pattern of synthetic stand-ins for real identifiers before anything leaves the device.

## Findings

- Shipped as three modes: Agent, Chat and Coder. Chat mode covers plain conversation.
- Default visual mode is serious and minimal, with customizable fonts and themes.

## Technical decisions

- Zero-backend static app with bring-your-own-key, so there is no server to trust.
- Memory runs entirely on the machine.
- Self-improvement proposals are gated and logged, never self-applied: a static page cannot rewrite its own deployed code.
- MIT licensed.

## Gaps

- Comparison notes on rival Muse builds live in chat history (2026-09-23).
