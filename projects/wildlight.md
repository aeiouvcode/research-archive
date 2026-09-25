# WILDLIGHT: Valley Run

- Repository: https://github.com/aeiouvcode/wildlight
- Live: https://aeiouvcode.github.io/wildlight/

## Inspiration

A forest-valley demo shown as made with Unreal / GPT Astra, sent by the owner on 2026-09-21 with "Show them whos the boss". Brief: beat it in a browser.

## References

- The Unreal/GPT-Astra valley demo (X, 2026-09-21). Exact URL in chat history.

## Findings

- The first cut graded FAIL on design: it was CSS scenery tricks, not a real 3D valley. Rebuilt from scratch and passed 2026-09-22: real 3D birch valley, god rays on the trail, wind-blown grass, shader stream, minimap HUD.
- Known residuals: canopy reads puffy up close; the stream is rarely in frame.
- Deploy note: the push token cannot create repos, so new repos need the browser session; this one's push was blocked until the owner refreshed the GitHub browser session (2026-09-23).

## Technical decisions

- Browser third-person run with a touch joystick and WASD, zero install.
- Warm light shafts, dust and haze are the core of the look.

## Gaps

- The reference demo link is in chat history (2026-09-21 20:57).
