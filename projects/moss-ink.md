# Moss Ink

- Repository: https://github.com/aeiouvcode/moss-ink (Godot rebuild: https://github.com/aeiouvcode/moss-ink-godot)
- Live: https://aeiouvcode.github.io/moss-ink-godot/

## Inspiration

A living generative dither garden and warm-paper design system, later rebuilt in Godot on the owner's order (2026-09-23): "Can you make the 3d dither world again but now using godot" - "i meant moss ink". Reference: the leafalia dither-render post by @eschadiol.

## References

- The leafalia dither-render post (@eschadiol, X, re-sent 2026-09-23 20:09): two tones, pixel-scale dots, hard ink shadows, fine-stroke foliage. Graded against it each pass.

## Findings

- Owner steers: "As yours one is densely packed, it feels less resolutipn, btw the blobs in the reference follow something similar to softbody physics" (2026-09-23); "the objects were able to be remove from the plane, moved up and would be thrown down due to gravitational field" (2026-09-24).
- Passes 1-6 live by 2026-09-24: density down, jelly-wobble blobs, grab-and-pull softbody. Next: lifting objects off the ground plane and dropping them under gravity.
- Composition (close-up of a few big forms vs the whole island) is the standing gap.

## Technical decisions

- Godot 4 export for the web; dithered 3D island rendered in two tones with pixel-scale dots.

## Gaps

- Softbody-gravity interaction work continues; per-pass notes in chat history (2026-09-23/24).
