# KIN

- Repository: https://github.com/aeiouvcode/kin-living-pond
- Live: https://aeiouvcode.github.io/kin-living-pond/

## Inspiration

RYUKIN by Masataka Hakozaki (Google Play: https://play.google.com/store/apps/details?id=com.hacoapp.ggla.ryukin), pinned as the source reference on 2026-09-21.

## References

- RYUKIN (Hakozaki): lighting realism, caustics, fish motion.

## Findings

- Lighting realism matters most: caustics, refraction, chromatic aberration.
- An engagement layer (feeding streaks, pond care) was requested for this app specifically.
- Latest grade against the reference: PARTIAL+.

## Technical decisions

- Hand-written WebGL: travelling caustic filaments, chromatic fringe, fin deformation.
- True refraction and ray-traced bounce left out to keep phone performance.
- A move to the Godot engine was requested on 2026-09-22 and had not started when this was written.

## Gaps

_None known._
