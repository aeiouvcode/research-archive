# FrameForge Studio

- Repository: https://github.com/aeiouvcode/frameforge-studio
- Live: https://aeiouvcode.github.io/frameforge-studio/

## Inspiration

Benchmarks named in the brief (2026-09-17): Adobe Premiere, DaVinci Resolve and CapCut. Built from scratch with a custom engine and no forks.

## References

_None recorded yet._

## Findings

- Milestones M1-M55 covered the timeline, keyframes and curve editor, color grading with a luma scope, an audio mixer matched between preview and export, a full caption system (SRT/WebVTT, karaoke cues), Auto Cut and an encrypted project vault.

## Technical decisions

- Silero VAD running in-browser on ONNX Runtime Web (vendored WASM) for Auto Cut. Silence detection stays on the device.
- Local-first: media, captions and renders never leave the device.
- A hand-built SVG icon set instead of emoji glyphs.

## Gaps

- Auto Cut design notes are in AUTOCUT-SPEC.md in the repo. Per-milestone research is in chat history, 2026-09-17 onward.
