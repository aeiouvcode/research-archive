# MNEME

- Repository: https://github.com/aeiouvcode/dev-memory
- Live: https://aeiouvcode.github.io/dev-memory/

## Inspiration

Owner spec (2026-09-19): a "custom developer memory architecture" - vector RAG plus a graph database for preferences and evolving facts, asynchronous extraction of entity facts appended to later system prompts, and summarisation loops that compress old conversation blocks into compact context nodes.

## References

- The owner's pasted spec (2026-09-19 17:10), in chat history.

## Findings

- Built as a working in-browser simulation (no backend, no key): a live conversation stream running a four-stage async extraction pipeline, a visible vector store and knowledge graph.

## Technical decisions

- Simulation rather than a service, per the local-first rule: everything runs in the page.

## Gaps

- Sits next to the on-machine memory spine of Open Muse; unifying the two lines of memory research has not been done.
