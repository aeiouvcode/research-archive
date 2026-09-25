# Bend $10k soundness bounty

- No repository - security research
- Status: technical target confirmed soft, bounty not claimable

## Inspiration

Victor Taelin's X post forwarded by the owner on 2026-09-20 with two words: "Challenge accepted". The target: a Bend file that parses and type-checks clean ("All terms check.", no unsafes or holes) while defining a top-level term of type Empty - i.e. proving a falsehood. $10k.

## References

- Victor Taelin's bounty post (X, 2026-09-20 01:41). Exact URL in chat history.
- bendlang/bend issue #852: the identical exploit filed publicly the day before.
- bendlang/bend PR #863 (fix for #852) and #994 (proof-gate fix, open and unmerged as of 2026-09-24).

## Findings

- A clean Empty proof was reproduced on Bend 2.0.16 and current main. Root cause: a nat-literal pattern that bypasses constructor arity checks, letting the termination checker swallow a non-decreasing recursive call.
- Not claimable, honestly: the identical exploit was already public (issue #852), Taelin's terms only open the bounty after he resyncs the implementation with the formalization (1-2 weeks out at the time), and a fix PR already exists. Claiming it would not be honest.
- 2026-09-24: someone else publicly filed two proof-gate breaks (name-resolution hijack, silent @unsafe fill), so both are dead for the bounty too.
- Graded PARTIAL. The continuing play: hunt a distinct unsoundness that survives the resync - that is the one worth the money.

## Technical decisions

- Reproduce first, claim never: verification on two Bend versions before any public move.

## Gaps

- Distinct-unsoundness hunt continues.
