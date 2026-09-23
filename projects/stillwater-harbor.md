# Stillwater

- Repository: https://github.com/aeiouvcode/stillwater-harbor
- Live: https://aeiouvcode.github.io/stillwater-harbor/

## Inspiration

A night-sailing render presented as made with GPT Astra (sent 2026-09-21).

## References

_None recorded yet._

## Findings

- The first two passes were rejected on physics, not looks. Shader noise is not water.
- A heightfield solver does not need a native C++/Rust engine. A video editor at full scale might.

## Technical decisions

- A 128x128 damped heightfield with the hull as a pressure source, wake propagation, foam decay, and reflections driven by the simulation.
- Three.js r168. First project to run the eight-cycle self-critique loop.

## Gaps

- Follow-on optics requests (ray tracing, caustics, chromatic aberration) are in chat history (2026-09-22 00:32).
