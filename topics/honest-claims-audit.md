# Honest claims audits

Shared across the hardware, simulation and design-research projects: NAKSH-8, EDGE-R1, AURORA-Sigma, NIVEL-1, VANTA R1, and the app fleet generally.

## The pattern

Each deliverable ships with an audit of its own claims, and the audit is allowed to fail the deliverable:

- NAKSH-8: recursion claim holds in software (rerun twice, hashes match); the hardware claim does not - missing decode/sequencer/control logic. Verdict stated plainly.
- EDGE-R1: proves recursive runtime orchestration with two microscopic scripted models - "not useful SLM ability, not silicon, not self-replication".
- NIVEL-1: the 97.2% classifier figure reproduces only on its own synthetic data; 600 ms anti-pinch, 120 kg load and market-uniqueness claims did not survive scrutiny and were corrected.
- VANTA R1: "promising, not proven" - targets, not measurements; literature-backed at category level, not for this shoe.
- Vault Key: SECURITY.md names its own limits (XSS surface, device compromise, no autofill, no recovery).

## The owner's bars behind it

- Artifacts must be derived from the actual run, not illustrated. He rejected EDGE-R1's first diagram as "a representative diagram not the actual configuration"; figures were regenerated from the simulator's real state.
- Error handling is a design requirement: a raw error screen read to him as "Felt like i downloaded malware" (EDGE//AI).
- He held back sending agent-generated source because "i dont know, if it contains secrets as plaintext" - pre-push secret scans are the answer (see topics/local-first-security.md).
