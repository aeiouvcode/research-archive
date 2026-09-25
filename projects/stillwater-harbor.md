# Stillwater

- Repository: https://github.com/aeiouvcode/stillwater-harbor
- Live: https://aeiouvcode.github.io/stillwater-harbor/

## Inspiration

A night-sailing render presented as made with GPT Astra (claimed 7B tokens, $5,887), sent 2026-09-21 with "Make the exact same and mog on chatgpt astra, if you csn".

## References

- The GPT Astra night-sailing render (X, 2026-09-21). Exact URL in chat history.

## Findings

- The first two passes were rejected on physics, not looks: "Physics not there for fluid sim", "Solve the wave sim". The technical line that came out of it: shader noise is not water.
- A heightfield solver does not need a native C++/Rust engine. A video editor at full scale might - that thread became FrameForge's Zig/WASM core (see projects/frameforge-studio.md).
- First project to run the self-critique gauntlet loop: 8 cycles (see topics/reference-grading.md).
- "Also improve the boat" (2026-09-22): rebuilt as a harbor tug with bow, rub rail, tire fenders, nav lights and a lit cabin, wake trailing its real heading.

## Technical decisions

- A 128x128 damped heightfield with the hull as a pressure source, wake propagation, foam decay, and reflections driven by the simulation.
- Three.js r168.

## Gaps

- Follow-on optics requests (ray tracing, caustics, chromatic aberration in fluid-light interaction) are in chat history (2026-09-22 00:32).
