# FRAME ZERO

- Repository: https://github.com/aeiouvcode/frame-zero
- Live: https://aeiouvcode.github.io/frame-zero/

## Inspiration

An original production brief from the owner (2026-09-19): an interactive animated manga whose pages control reality instead of depicting it. Five chapters, cinematic motion, atmospheric sound. The brief ruled out mockups, slideshows and visual-novel templates.

## References

- No external competitor. The brief itself is the reference, written as a director's document covering direction, narrative, storyboard, motion and WebGL engineering.

## Findings

- The climax choice screen was the weakest screen at 390px: art bled through the options, and a key clue only showed on hover, so touch players never saw it. Fixed with a denser overlay and a timed reveal.

## Technical decisions

- Single self-contained HTML file with no dependencies, so it stays portable and easy to audit.
- A strict CSP with connect-src 'none'. The manga never needs the network.
- All dynamic art passes through an SVG sanitizer before reaching the DOM.
- LocalStorage for saves and chapter unlocks.

## Gaps

- The full production brief text lives in chat history (2026-09-19 17:00) and is not reproduced here.
