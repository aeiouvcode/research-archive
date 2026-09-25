# Reference grading: the gauntlet loop and distance-to-reference audits

Shared across every replication and benchmark build.

## The gauntlet loop

Ordered by the owner 2026-09-21 while grading the Stillwater water sim frame by frame: "Become a self critique agent, run yourself in a gauntlet loop and keep build until it is reasonably better than the x post one", immediately followed by "Run this concept for all other projects in parallel as well".

What it means in practice:

- Each project loops render -> critique against its reference or a best-in-class bar -> fix the top gaps -> repeat, and only reports when it can defend the result.
- The acceptance bar is the reference artifact he sent, not an internal spec.
- No frame-by-frame pinging: he does not want to be the critique loop.
- Security and design review ride every cycle (2026-09-22/23): a security check plus a design-and-interactions pass at phone and desktop widths, every pass.
- Loop state lives in the project repos as CURRENT_TASK / CHECKPOINT / HANDOFF files ("Maintain", 2026-09-23).

## Distance-to-reference audits

His 2026-09-23 critique: in every replication project "none of them have you been able to match or exceed quality" versus the original, and the ambitious builds are "sometimes working, sometimes failing". The response now in force:

- Reliability (loads and runs every time) is the floor.
- Each replication cycle does a side-by-side against the reference, lists what still reads worse, and fixes in priority order. Tidemill, Linefold, KIN and ISSEN were first.
- References get corrected when wrong: ISSEN's grading had been running against the wrong Play Store listing until the true reference footage was pinned (2026-09-23).

## The fleet freeze

2026-09-23 21:35: "No more projects for now, these are all there is, you will keep building on these projects and refining them. Refine until they are better than their source of inspiration, but the inspiration itself will grow, so you accelerate." New reference links after that point are input to existing projects, not new builds, unless he explicitly says otherwise.
