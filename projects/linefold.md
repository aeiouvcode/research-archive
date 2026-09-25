# Linefold

- Repository: https://github.com/aeiouvcode/linefold
- Live: https://aeiouvcode.github.io/linefold/

## Inspiration

Mini Metro (Dinosaur Polo Club). The genre reference: draw subway lines while the city grows.

## References

- Mini Metro: the distance-to-reference audit (2026-09-23) graded the build side-by-side against it.

## Findings

- Four self-critique cycles. Checked live at 390px on 2026-09-22.
- Distance-to-reference audit: self-graded about 45/100, improved to about 72 after the fix pass. Still worse than the reference: shared stretches overlap instead of running parallel, end-station trains hide stations, no real city geography.

## Technical decisions

- Canvas 2D and Web Audio in one file. Springy stations, a layered river, a ferry easter egg, palette switching with press states.
- First repo to carry the CURRENT_TASK / CHECKPOINT / HANDOFF state files (see topics/reference-grading.md).

## Gaps

- Remaining distance to Mini Metro is listed above; audit details in chat history (2026-09-23).
