# Jules evaluation

- No repository of its own - Jules's output landed at github.com/Matter-does/test-jules-agent
- Status: ongoing comparative evaluation

## Inspiration

The owner benchmarks other agents against Instinct rather than trusting it (2026-09-18): "a hard prompt, like an existing project we r working on" to run through Jules, then multiple parallel sessions. He wants prompts that expose stub work rather than greenfield toys, and he insists Jules get the same reference material Instinct gets - "doing justice is to provide jules with that as well".

## References

- github.com/Matter-does/test-jules-agent: Jules's output on the Open Muse memory task.

## Findings

- Prompts issued: (1) FrameForge's Auto Cut (VAD-driven silence removal) - dropped because the video-editing repo had not updated; (2) an Open Muse extension - the trap is IndexedDB persistence, dedupe semantics and expiry surviving a reload; (3) Showreel - greenfield browser screen recorder that records the event sidecar (clicks, keystrokes, scrolls) and edits itself, getDisplayMedia + WebCodecs export.
- Jules's Open Muse memory output reviewed at code and runtime level: 7/8 PASS, real AES-GCM at rest including re-encrypting pre-passphrase records; weak dedupe and a session bug.
- The owner's conclusion about the comparison so far: Instinct is valued for holding many projects across time, not for raw in-repo iteration - "I think instinct is not meant for doing high performance requirement coding tasks".
- If Showreel comes out good, the same capability is planned for FrameForge.

## Technical decisions

- Blind, identical-brief evaluation: same prompt and same reference material to both agents.

## Gaps

- Showreel outcome pending.
