# The Godot dual-track rule

Shared across the game projects: ISSEN, SKYTETHER, Tidemill, O Empire, KIN, OUTWARD, KEIRYU/SUIKEI, Moss Ink, KESTREL-9, INCREMENT, NIGHTNET, KEEP THE LIGHT.

## The rule

Set by the owner on 2026-09-23, in steps:

- "Anything that requires a game engine for further improve to stand close to the ground truth, use the game engine godot" (10:36).
- "Keep the issen as is, also build a godot game to match the ground truth" (10:37) - the Three.js build keeps iterating; Godot runs in parallel, never replaces it.
- "make all of the games we are making also in a game engine godot version" (14:29).
- The lesson in his words: "One thing you learn is that an actual tool made to do the job like a game engine for game works" (12:43). The Godot ISSEN caught up with 70 Three.js milestones in about 10 cycles, which is what convinced him.
- "Use the best tools" (14:43) - e.g. ISSEN Android ships as a Godot APK export rather than a Kotlin rewrite.

## How it runs

- Web (Three.js) and Godot are separate tracks in the same repo (Godot on its own branch, published at `<app>/godot/`) or a separate `-godot` repo.
- The web link the owner approved stays untouched when a Godot port goes live.
- Godot web exports are heavy on first load (9-38 MB wasm).
- Some new builds are Godot-first (INCREMENT, NIGHTNET).

## Findings

- KIN is the counter-case: the Godot prototype never beat the live WebGL build, so nothing was replaced; the Godot preview is published only to measure phone frame rate.
- Tidemill's Godot branch exists for the engine-bound water/lighting gap; its first water milestone beat the Three.js foam.
