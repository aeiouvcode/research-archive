# Open Muse

- Repository: https://github.com/aeiouvcode/open-muse
- Live: https://aeiouvcode.github.io/open-muse/

## Inspiration

Meta's Muse agent concept: a personal agent that takes work off your plate. Brief (2026-09-18): build an open-source version that works everywhere, with no region lock.

## References

- THUNLP ProactiveAgent (GitHub): patterns for proactive, unprompted assistance.
- kayba-ai/recursive-improve (GitHub): the self-improvement loop pattern (branch per experiment, failed-attempt log, hard gates, keep or revert). Graded B/C+ when the owner asked.
- OpenViking: tiered filesystem memory, used as the memory spine.
- Mem0: fact-extraction pattern for memory.
- supermemory: considered and left out because it would break on-machine operation.
- Amp orbs: persistent remote machines, the model for work that outlives a session.
- AgentCloak Desktop: the privacy-cloak pattern of synthetic stand-ins for real identifiers before anything leaves the device.
- eigent-ai/eigent (GitHub, sent 2026-09-19): workforce runs, a coordinator decomposing goals into subtask DAGs.
- MiniMax-AI/minimax-code (GitHub, sent 2026-09-19): Coder mode with an inspect-only Plan mode.
- LibreChat and Jan: benchmarked against for the competitive push (2026-09-23/24).
- CopilotKit's OpenMuse (launched 2026-09-22): an MIT self-hostable personal-agent starter with the same name. Different category - theirs is a server-side agent shell, this is a local-first privacy cloak and habits app.

## Findings

- Shipped as three modes: Agent, Chat and Coder. Chat mode covers plain conversation.
- Default visual mode is serious and minimal, with customizable fonts and themes.
- The first ship went out before graded QA and the owner hit it immediately ("Fix the open muse, it is full of bugs"). The sweep found 8 real bugs including a dead mobile menu and a wrong salt in the passphrase lock. Lesson recorded: QA before announcing.
- Provider rescue (2026-09-21/22): a real key failed with "does not recognize that model (404)" and "server trouble (503)". Three real bugs behind it - the model tester demanded text from a 1-token probe, a stale hardcoded default model id Google had retired, and a fallback list of one guessed id. Now the app reads Google's live catalog when a key is saved, with 17 current ids as offline fallback and a Settings test sweep that works for any provider key. Real-key sweep: 9 of 26 chat models answer live.
- Name collision (2026-09-22): CopilotKit launched an MIT agent starter also called OpenMuse. Owner: "We were a little too late." Open decision, waiting on him: keep the name or rename.
- Competitive push (2026-09-23/24): "make open muse substantially better to make it a competitive alternative". Shipped: multi-conversation sessions, checkpoints + fork, retry keeping old replies as flippable variants. Deliberately not chasing: microVMs, agents running while closed.
- A rival model's "open muse but better" output was graded (2026-09-23): PARTIAL, cannot boot (truncated app.js, bad import, default provider is a mock that fakes replies). Ideas folded back in: a single fetch chokepoint scanning outbound requests for raw PII, post-wipe verification on Erase, smarter name-cloaking, a tracking-param URL scrubber, approval-gated memory writes, tree branching with edit-and-regenerate.

## Technical decisions

- Zero-backend static app with bring-your-own-key, so there is no server to trust. Gemini is the default provider.
- Memory runs entirely on the machine.
- On-device engine via transformers.js (vendored, pinned; WebGPU with WASM fallback) so chat models run locally with no key. Verified loading and chatting; small models follow instructions weakly.
- EDGE//AI selectable as the on-device engine (inter-project compatibility pilot), verified live.
- Privacy cloak verified against real provider traffic: the provider only ever saw the synthetic twins.
- Self-improvement proposals are gated and logged, never self-applied: a static page cannot rewrite its own deployed code.
- MIT licensed.

## Gaps

- Comparison notes on rival Muse builds live in chat history (2026-09-23).
- Idle auto-lock is unprovable in a session (manual Lock button queued); Swarm/Studio not exercised; Evolve once proposed a feature the app already had - its self-knowledge is weak.
- Unanswered owner question: whether the opencode API should back Open Muse as a coding-agent server (2026-09-22).
