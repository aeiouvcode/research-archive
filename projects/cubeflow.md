# CUBEFLOW

- Repository: https://github.com/aeiouvcode/cubeflow
- Live: https://aeiouvcode.github.io/cubeflow/

## Inspiration

A local-first camera Rubik's cube coach: scan, correct, and follow the solve move by move. The originating brief is in chat history.

## References

_None recorded yet._

## Findings

- Verified end to end on the live deploy (2026-09-22), including an earlier scan-crash fix.

## Technical decisions

- Scan the cube face by face with the camera, solve locally, coach one move at a time (about 20-move solutions).
- Carries the shadcn-derived pressed states and spring easing from the 2026-09-21 design-resource steer.

## Gaps

- The originating brief and scan-pipeline notes are in chat history (2026-09-21/22).
