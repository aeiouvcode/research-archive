# Afternoon

- Repository: https://github.com/aeiouvcode/afternoon
- Live: https://aeiouvcode.github.io/afternoon/

## Inspiration

An X post claiming Instinct's chat surface is an afternoon build. The owner's reply (2026-09-17): "If that is true build an instinct clone."

## References

- The X post claiming Instinct is an afternoon build (2026-09-17). Exact URL in chat history.
- OpenClaw (open-source self-hosted chat agent): the owner's evidence that integrations and plumbing are commoditized - "I mean theres the claw".

## Findings

- A personal agent page with real streaming chat, a local memory panel, and a task list the agent edits mid-conversation is buildable in an afternoon; the moat is memory, hosting and distribution, not the chat UI (the owner's thesis).
- Known defect (2026-09-19): Token Harbor's CORS block means real model calls fail through that provider; OpenRouter works. The owner asked for an in-flight status line instead of silence-then-error.

## Technical decisions

- Bring-your-own OpenRouter key, strict CSP, opt-in E2EE, an Instinct-shaped agent layer (memory it references, open-task count, pending approvals).
- Rebuilt 2026-09-18 with Token Harbor as default provider plus a model selector; default later de facto reverted because of the CORS defect above.

## Gaps

- Token Harbor provider remains broken end-to-end pending a CORS-friendly path.
