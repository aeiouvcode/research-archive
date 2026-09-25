# AURORA-Sigma

- No repository - code package delivered by email
- Status: completed

## Inspiration

Owner brief: "create a software which simulates realistic probabilistic outcomes of circuits… beyond the frontier of circuit simulation." He then merged threads: "run the recursive loop code in the circuit simulation verifier as well", so the NAKSH-8-style recursive program became the workload being analysed.

## References

_None recorded yet._

## Findings

- Rare-event tails via importance sampling: 5.2 sigma on a calibration ring where crude Monte Carlo saw no failures; 3.9 sigma / 5.7e-5 on an 88 MHz deadline.
- 10-year BTI + electromigration aging across 20k virtual devices.
- A 580k-sample voltage/temperature yield map off a surrogate at 0.53% RMSE.

## Technical decisions

- Importance sampling over crude Monte Carlo for rare-event tails; surrogate modelling for the yield map.

## Gaps

_None known._
