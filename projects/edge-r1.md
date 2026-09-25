# EDGE-R1

- No repository - code zips delivered by email
- Status: completed

## Inspiration

Escalation after the owner called the first desk/circuit diagram "very basic": simulate an ESP32-class SoC with a native AI chip running an SLM that hosts a smaller instance of itself.

## References

_None recorded yet._

## Findings

- Delivered: a dual-core RV32 SoC sim with RTOS, 16x16 INT8 systolic NPU, DMA and memory map; a quantized transformer emits SPAWN_CHILD, the MCU DMA-loads a smaller model and runs it on the same NPU. 63,104 MACs, 8,391 cycles, separate SHA-256 model identities.
- The owner rejected the first architecture diagram as "a representative diagram not the actual configuration". His standing bar: figures must be generated from the simulator's real state (address map, byte offsets, NPU register values), and they were regenerated that way.
- Audit boundary, stated honestly: proves recursive runtime orchestration with two microscopic scripted models - not useful SLM ability, not silicon, not self-replication.

## Technical decisions

- See topics/honest-claims-audit.md for the derived-not-illustrated artifacts rule.

## Gaps

_None known._
