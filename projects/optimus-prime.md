# Optimus Prime

- Repository: https://github.com/aeiouvcode/optimus-prime
- Live: https://aeiouvcode.github.io/optimus-prime/

## Inspiration

Reference images of Optimus Prime (Last Knight armor) sent 2026-09-19: "make this as a 3d model, be true to the source", then a minute later "Parellely try to make this in three js" - both tracks at once.

## References

- The owner's Optimus Prime reference images (2026-09-19 20:23), in chat history.
- Hunyuan3D-2 (Tencent free demo, no account): the AI image-to-3D track.
- Hunyuan3D 2.1 six-view paint pipeline: the offered escalation for film-grade fidelity, not started.

## Findings

- AI track graded PARTIAL: a real GLB (121k vertices, correct silhouette, hand-painted red/blue/silver blocking) but not film-accurate - base mesh, no fine mechanical detail, no textures or rig.
- Three.js track PASS: hand-coded procedural sculpt, about 200 parts, orbit view.
- Unofficial fan study; flagged for the license decision because it uses Transformers IP.

## Technical decisions

- Delivery as a download page because WhatsApp cannot carry .glb files.

## Gaps

- Open, awaiting the owner: escalation to Hunyuan3D 2.1's six-view paint pipeline needs real GPU compute and likely a paid account.
