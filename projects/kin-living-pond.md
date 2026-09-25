# KIN

- Repository: https://github.com/aeiouvcode/kin-living-pond
- Live: https://aeiouvcode.github.io/kin-living-pond/ (Godot preview: https://aeiouvcode.github.io/kin-living-pond/godot/)

## Inspiration

RYUKIN by Masataka Hakozaki (Google Play: https://play.google.com/store/apps/details?id=com.hacoapp.ggla.ryukin), pinned as the source reference by the owner on 2026-09-21. Re-pinned on 2026-09-23 as Hakozaki's RYUKIN X post: "The reference for koi" - pastel lavender bowl, silk veil fins.

## References

- RYUKIN (Hakozaki): lighting realism, caustics, fish motion; the X post is now the grading bar.
- "Koi - Aquarium" (Play Store, com.netk.Koi, sent 2026-09-22): became the working visual reference for a from-scratch rebuild as a top-down pond.

## Findings

- Lighting realism matters most: caustics, refraction, chromatic aberration.
- An engagement layer (feeding streaks, pond care) was requested for this app specifically.
- Latest grade against the reference: PARTIAL+ (KIN VII). The distance-to-reference audit against the Koi app drives the fix order: fish skin and fins, water murk, stone ring, pads.
- True refraction and ray-traced bounce are deliberately left out for phone performance.
- Fish craft was reset after the owner found the demekin wrong (2026-09-23).
- On 2026-09-24 the owner chose both koi pond and fish bowl scenes; the two-scene build sits on a branch awaiting his live-switch yes.

## Technical decisions

- Hand-written WebGL: travelling caustic filaments, chromatic fringe, fin deformation. Rebuilt as a top-down pond with a GPU water sim (tap ripples, wakes, caustics), 9 koi varieties with personalities, feeding that builds a bond, lilies that bloom with trust.
- A Godot engine move was requested on 2026-09-22; the prototype never beat the live WebGL build, so nothing was replaced. A Godot preview was published at /godot/ on 2026-09-23 to measure phone frame rate against the 9MB engine load.

## Gaps

- Open questions to the owner (2026-09-23): whether the Koi app is the right target or he has original koi references.
