# Tidemill

- Repository: https://github.com/aeiouvcode/tidemill
- Live: https://aeiouvcode.github.io/tidemill/

## Inspiration

Townscaper (Oskar Stålberg). The owner graded the first build his worst-looking project, then sent the official Townscaper trailer (2026-09-21): "This is what the townscaper game actually looks like."

## References

- Townscaper official trailer (2026-09-21).
- The owner's own exact Townscaper town, sent as oskarstalberg.com/Townscaper and townscaper.org links (2026-09-23): coral bell-cap tower, gabled houses, T pier. Tidemill v4 was built directly against it.

## Findings

- The first version was fake 3D (a flat tilemap), and the trailer comparison exposed it.
- Rebuilt in true 3D: blocks snap into houses with roofs, windows and arches, plus an orbit camera, a lighthouse beam and gulls.
- First distance-to-reference audit (2026-09-23), side-by-side against Townscaper: fixed terracotta roofs, brighter palette, doors, window frames, and a color-pipeline bug.
- Tidemill v4 went live 2026-09-24 on the owner's go, replacing the old build; old saved towns do not carry over.

## Technical decisions

- Three.js r160 via import map.
- Towns save to a shareable URL (v4). Towns made in the old 2D version carried over across reload until v4 replaced the build.
- Godot branch started 2026-09-23 for the engine-bound water/lighting gap; its first water milestone beat the Three.js foam. See topics/godot-track.md.

## Gaps

- Engine-bound water and lighting are the standing gap vs Townscaper; the Godot branch is where that gets closed.
