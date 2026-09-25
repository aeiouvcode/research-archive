# NIGHTNET

- Repository: https://github.com/aeiouvcode/nightnet
- Live: not yet live as of 2026-09-25

## Inspiration

The Genex browser-basketball post, sent 2026-09-23 with "i Want the basketball game, make it godot".

## References

- The Genex browser-basketball post (X, 2026-09-23 21:03). Exact URL in chat history.

## Findings

- The first build agent died silently overnight with no source written; restarted 2026-09-24 morning, first playable by 07:27: dark arena, joystick plus hold-release shot meter, dunks, 60s runs.
- The owner approved pass 2 (jointed player, rim-outs), but publish was blocked by a GitHub browser outage and the staged pass 2 was lost before push. Being rebuilt.

## Technical decisions

- Godot 4 web build, after-hours solo hoops.

## Gaps

- Pass 2 rebuild and first publish are in flight; the push-token-cannot-create-repos constraint applies (see projects/wildlight.md).
