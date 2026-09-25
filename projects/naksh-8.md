# NAKSH-8

- No repository - project zip delivered by email (WhatsApp rejects archives)

## Inspiration

Owner brief (2026-09-16): "using kicad write a circuit and script it a simulation of a simple computer which itself simulates a smaller computer."

## References

_None recorded yet._

## Findings

- Delivered: an 8-bit Harvard CPU in 74-series logic (NE555 clock, 74HC181 ALU, 28C64 ROM), KiCad 7 schematic generated programmatically. It runs a 237-byte emulator for PICO-4, a 4-bit machine in its RAM computing Fibonacci to overflow, 2,627 cycles to halt.
- Claims audit verdict: the recursion holds in software (reran twice, hashes match); the hardware claim does not - the schematic drives only 16 RAM addresses, grounds branch-load inputs, and lacks decode/sequencer/control logic. Fix plan exists, not executed.
- No KiCad binary was available to the agent, so the schematic was validated by parsing; the owner needs to open naksh8.kicad_sch himself for the final check.

## Technical decisions

- Programmatic KiCad 7 schematic generation.

## Gaps

- Hardware-claim fix plan not executed; see topics/honest-claims-audit.md.
