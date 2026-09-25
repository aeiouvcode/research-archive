# HARBOR//MIND

- Repository: https://github.com/aeiouvcode/harbor-mind
- Live: https://aeiouvcode.github.io/harbor-mind/

## Inspiration

An X post of a browser driving sim steered by Jev (typesafe-ai's structured-decision model, about 4 calls/sec over a constrained action tree), sent 2026-09-17 with "Its time for you to do as well."

## References

- The Jev driving-sim post (X, 2026-09-17). Exact URL in chat history.
- typesafe-ai console (console.typesafe.ai): the real-model path, gated early access with no free anonymous tier.

## Findings

- Built with a heuristic stand-in brain after the owner said "You can use anything else to build it": three vessels, structured state in, dock/hold/divert/rescue out at 4 Hz with probabilities, confidence and reasons on screen. The stand-in is labeled on the page itself.
- A v02 added live incident controls (person overboard, close berth, surge storm) and a recorded decision stream.
- The real-model swap is one file. Blocked: Jev needs an API key and access is gated; the owner was asked to sign in and drop a key in the vault, no response yet. He had already waved off an earlier waitlist attempt ("Leave it"), so the appetite may be for the demo, not the signup.

## Technical decisions

- Structured-decision loop at visible cadence with on-screen confidence, mirroring the reference's 4 calls/sec action-tree pattern.

## Gaps

- Real Jev model integration awaits the owner's console.typesafe.ai key.
