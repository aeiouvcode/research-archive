# NIVEL-1

- No repository - dossiers delivered as documents
- Status: completed

## Inspiration

Owner brief: a desk that learns the user's standing height and work posture, with the minimum number of motors, better than market options, plus a DIY build process.

## References

_None recorded yet._

## Findings

- Delivered: 3 motors total (two hall-synced lift columns, one self-locking tilt actuator, zero for the monitor - passive gas arm), a work-mode classifier at 97.2% on held-out poses, a Gaussian Process learning from manual nudges, and classic PID retained for pinch safety so learning never touches protection.
- 8-page dossier, DIY build (three evenings + a weekend, about Rs 35-42k India-sourced), and a 9-page manufacturing guide (pilot BOM Rs 48-70k at 100 units, Rs 39-48k at 1,000).
- Audit caveat: the 97.2% figure reproduces only on its own synthetic data - a simulator result. Claims about 600 ms anti-pinch, 120 kg load and market uniqueness did not survive scrutiny and were corrected.

## Technical decisions

- Learning is kept away from the safety path: PID owns pinch protection, the GP only adjusts comfort.

## Gaps

- See topics/honest-claims-audit.md.
