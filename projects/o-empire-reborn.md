# O Empire

- Repository: https://github.com/aeiouvcode/o-empire-reborn
- Live: https://aeiouvcode.github.io/o-empire-reborn/ (Godot track: https://aeiouvcode.github.io/o-empire-reborn/godot/)

## Inspiration

The Steam game O EMPIRE! WARD OFF THY ROT (store.steampowered.com/app/4331110). Brief (2026-09-16): a slow, non-combat survival walk across a post-rapture medieval continent carrying a cursed artifact that grows heavier. Built as an original atmospheric survival procession inspired by it, not a copy.

## References

- The developer's key art: misregistered halftone plates, a gray tower, a red flower field. Used as the primary art direction, not a mood reference.
- The developer's gameplay video: held low-frame-rate animation and an elevated oblique camera. Viewing from above changes how the game reads.
- An AwkSilence Games X post (x.com/AwkSilenceGames/status/2099528789126492531) the owner singled out: procession gait, planted-foot silhouettes, exposure trails, independent flower shimmer.
- The Steam screenshots (2026-09-23 audit): scattered scarlet blossoms, drawn ruins, synth sound.

## Findings

- Side-by-side comparison of the red flower snow field scene against the developer's: judged "a close second" by the owner.
- Pacing target is about an 11-minute walk. A smart run finishes in 10:35 with all 8 caches, with a "CACHE NEAR" HUD prompt (M4).
- Nearly every round of owner feedback has been about look and motion, not mechanics.
- Mid-stream the owner narrowed scope to animation fidelity only: rebuild just the red flower field scene for a side-by-side compare.

## Technical decisions

- Canvas rendering in a single file.
- Ash and charcoal palette with crimson as the only saturated color; flowers rebuilt from particles into rooted patches.
- Strict CSP hashes after the last innerHTML sink was removed (M13a, 2026-09-23); design and gameplay PASS at phone width.
- Godot track (3D print-plate halftone world) live at /godot/ since 2026-09-23, graded PARTIAL; M18 adds a rounded old-screen frame and snow stretches.

## Gaps

- The original prototype builds were lost when their temporary hosts expired (2026-09-17). Their notes are in chat history only.
- The full reckless-mode balance sim only ran to 500s before hitting the browser ceiling.
- Media sent earlier in a day does not survive on the agent's side - the reference image had to be resent once.
