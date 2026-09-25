# KESTREL-9

- Repository: https://github.com/aeiouvcode/kestrel-9 (Godot port: https://github.com/aeiouvcode/kestrel9-godot)
- Live: https://aeiouvcode.github.io/kestrel-9/ and https://aeiouvcode.github.io/kestrel9-godot/

## Inspiration

SHD Games' Sierra 7 (Play Store: air.com.shdgames.sierra7.gp), sent 2026-09-22 with "Make this incredible game".

## References

- Sierra 7 (SHD Games). The owner's read of the reference: "SHD Games these devs make cool but incomplete games." What makes Sierra unique is the aiming mechanism - the character moves on their own, the player just strategises, aims and shoots - which allows for skill usage and makes it addictive.

## Findings

- The skill core is the shot itself: per-shot bloom, headshot kills, hit-stagger. Movement stays on rails.
- The campaign gets a real ending rather than SHD's cliffhanger, since incompleteness was the named weakness of the reference.
- His follow-up order ran the critique agent over design, logic, interactions, UI/UX, animations and lighting, then a Godot port. Original build, not a port of SHD assets.

## Technical decisions

- Canvas 2D web build in one file, plus a separate full GDScript port exported to web (kestrel9-godot). Both live 2026-09-23.
- Dual-track per the Godot fleet rule (see topics/godot-track.md).

## Gaps

- Graded by the self-critique loop; cycle notes live in chat history, 2026-09-22 to 09-23.
