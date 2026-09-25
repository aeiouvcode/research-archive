# OUTWARD

- Repository: https://github.com/aeiouvcode/outward
- Live: https://aeiouvcode.github.io/outward/ (Godot port: https://aeiouvcode.github.io/outward/godot/)

## Inspiration

The Play Store game com.oakever.arrows (interlocked arrows puzzle), sent 2026-09-23: "make our version of this game as a both web version and godot".

## References

- The oakever arrows game (Play Store, 2026-09-23): long winding arrow lines filling picture silhouettes; a tapped line slides out along its bends; blocked taps cost a droplet.
- "the amaze go game devs" - the owner's pointer for level-design variety (2026-09-23).

## Findings

- v1 built single-cell tiles; the owner rejected it ("This is not like the interlocked arrows game as i sent"). v2 rebuilt to the reference and approved: "This version of outward was good enough."
- Level-design steer: creative variety once every 5 levels - twist boards (mirror, ice/frozen, shackled, one-drop).
- The Godot port looked broken on his phone; diagnosed as a stale cached copy, fix is one reload.

## Technical decisions

- Calm tile puzzle on the web plus a Godot port, dual-track per the fleet rule.

## Gaps

_None known._
