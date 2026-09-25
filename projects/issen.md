# ISSEN

- Repository: https://github.com/aeiouvcode/issen
- Live: https://aeiouvcode.github.io/issen/ (Godot track: https://aeiouvcode.github.io/issen/godot/)

## Inspiration

An X post by the developer sensonoken showing a production Unity sword-duel game with a sumi-e ink look. Brief (2026-09-17): build a similar game with a similar art style, without Unity, and make it multiplatform.

## References

- Reference game footage (sensonoken, X, Sept 2026): follow camera, soft watercolor wash, no hard toon outlines, parchment ground, ink figures, slash arcs, dodge afterimages. The exact post URL lives only in chat history (2026-09-17).
- Reference corrected on 2026-09-23: grading had been running against the Ronin Play Store listing; the true reference is sensonoken's "Thousands Layered Blade" Unity footage. Every cycle since does a side-by-side against it.

## Findings

- The first builds did not match how the reference plays. The game was rebuilt from the reference video itself, not from a description of it.
- The biggest remaining gap to the reference is authored animation: the reference has hand-animated brushwork silhouettes, plus dense grass swaths and dry-brush ragged edges.
- Phone-width audits (390px) are what found later problems: uniform ground speckle, flat grass tufts, a pale bamboo horizon, and the boss blocking the camera.
- Blade feel (parry window, perfect vs late parry, slow-mo finisher, ink kill trails) was the owner's named priority (2026-09-23) and closed on both the web and Godot tracks.
- The Godot take caught up with ~70 Three.js milestones in about 10 cycles, which is what convinced the owner that an actual game engine beats hand-rolled web for games (see topics/godot-track.md).
- Owner verdict so far: "Gold" and "Its good" (2026-09-23).

## Technical decisions

- Three.js r160 as an ES module from jsDelivr with an import map and SRI. No engine install, and it runs on phones.
- Custom ink shaders for figures, ground grain and mist. The look is the product, so it lives in shader code rather than textures.
- Occlusion handling: when the boss crosses between camera and player, the camera slides and lifts slightly and the boss fades to translucent ink. A pure camera move could not keep both fighters readable.
- Hand-drawn canvas textures (brush grass, bamboo crowns) generated at runtime instead of image assets.
- Godot track on its own branch, published at /godot/ without touching the approved web link. Web build kept iterating in parallel (M67-M88 by 2026-09-24: shade and lancer foes, stances, per-chapter bosses, reactive shamisen/taiko).
- Android ships as a Godot APK export (offline, zero permissions, self-signed, installs over previous versions) rather than a Kotlin rewrite - "use the best tools". Distributed via GitHub releases. Signing key backed up at the owner's request.

## Gaps

- Milestone-by-milestone critique notes (M1-M88) exist only as build reports in chat history, 2026-09-17 to 2026-09-24.
- Godot cycles c19-c33 (armored/spear/twin-blade/archer foes, two-phase boss Kageyama, chapter map, save file) are source-only, awaiting the owner's deploy go.
- Play Store listing "ISSEN: Ink Blade Duel" is drafted; submission needs a Play Console dev account, a contact email, and a privacy-policy page from the owner.
- The APK (v0.12) has not been tested on the owner's actual phone.
