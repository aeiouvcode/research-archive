# FrameForge Studio

- Repository: https://github.com/aeiouvcode/frameforge-studio
- Live: https://aeiouvcode.github.io/frameforge-studio/

## Inspiration

Benchmarks named in the brief (2026-09-17): Adobe Premiere, DaVinci Resolve and CapCut. Built from scratch with a custom engine and no forks - "dont copy existing projects, make a better one from scratch". The standing instruction is a gauntlet loop: "Keep in building and improving until you reach a level better than the frontier".

## References

- Full feature lists of Premiere, DaVinci Resolve, CapCut and Clipchamp, requested by the owner as the comparison baseline (2026-09-18).

## Findings

- Milestones M1-M55 covered the timeline, keyframes and curve editor, color grading with a luma scope, an audio mixer matched between preview and export, a full caption system (SRT/WebVTT, karaoke cues), Auto Cut and an encrypted project vault.
- M86-M101 (2026-09-23/24): on-device Whisper auto-captions (closes the number one gap vs CapCut; Hindi readable with about 1-in-5 spelling fixes), transcript editing (delete words to cut the clip), 12x faster demo export (90s to 7.3s), scopes (RGB parade, zebras, false colour), frame-exact scrub, pinch zoom, clip virtualization for 150-clip projects.
- Auto-removing "um"s was parked: it cut real words.
- The owner put design, mobile and typography at the front of the queue ahead of features (2026-09-18): "Frameforge needs a complete mobile workaround", "Use professional icons in the video editor".
- CPU compositing is the wrong place for a heavy core at any speed. A Zig compositor ran ~142ms/frame, Rust ~50ms, and the browser's own GPU path 8.3ms - and copying frames off the GPU costs more than the whole composite. Zig kept real wins in LUT grading, waveforms and the speech front end; Rust source stays in the repo under core-rs/, not in the app. Owner accepted: "Ok, then wasm can be used to its limits comfortably" (2026-09-23).

## Technical decisions

- Heavy core in Zig compiled to WebAssembly, per the owner's engine call (2026-09-23): "the best video editors are made using c++, but we are going in a different direction, we will use zig". Browser shell stays; decode/scrub/render-class work moves to WASM.
- Silero VAD running in-browser on ONNX Runtime Web (vendored WASM) for Auto Cut. Silence detection stays on the device.
- On-device Whisper for auto-captions, so transcription never leaves the device.
- Local-first: media, captions and renders never leave the device.
- A hand-built SVG icon set instead of emoji glyphs.

## Gaps

- Auto Cut design notes are in AUTOCUT-SPEC.md in the repo. Per-milestone research is in chat history, 2026-09-17 onward.
- Still ahead: proxy transcodes, pan/EQ automation, codec breadth, pro color/audio finishing, and the AI + touch layer meant to be the actual CapCut-beating differentiator.
- Open bug: realtime export audio truncation.
