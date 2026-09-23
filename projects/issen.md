# ISSEN

- Repository: https://github.com/aeiouvcode/issen
- Live: https://aeiouvcode.github.io/issen/

## Inspiration

An X post by the developer sensonoken showing a production Unity sword-duel game with a sumi-e ink look. Brief (2026-09-17): build a similar game with a similar art style, without Unity, and make it multiplatform.

## References

- Reference game footage (sensonoken, X, Sept 2026): follow camera, soft watercolor wash, no hard toon outlines, parchment ground, ink figures, slash arcs, dodge afterimages. The exact post URL lives only in chat history (2026-09-17).

## Findings

- The first builds did not match how the reference plays. The game was rebuilt from the reference video itself, not from a description of it.
- The biggest remaining gap to the reference is authored animation: the reference has hand-animated brushwork silhouettes.
- Phone-width audits (390px) are what found later problems: uniform ground speckle, flat grass tufts, a pale bamboo horizon, and the boss blocking the camera.

## Technical decisions

- Three.js r160 as an ES module from jsDelivr with an import map and SRI. No engine install, and it runs on phones.
- Custom ink shaders for figures, ground grain and mist. The look is the product, so it lives in shader code rather than textures.
- Occlusion handling: when the boss crosses between camera and player, the camera slides and lifts slightly and the boss fades to translucent ink. A pure camera move could not keep both fighters readable.
- Hand-drawn canvas textures (brush grass, bamboo crowns) generated at runtime instead of image assets.

## Gaps

- Milestone-by-milestone critique notes (M1-M63) exist only as build reports in chat history, 2026-09-17 to 2026-09-23.
