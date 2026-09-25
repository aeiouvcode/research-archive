# Relay

- Repository: https://github.com/aeiouvcode/relay-agent
- Live: https://aeiouvcode.github.io/relay-agent/

## Inspiration

A local-first personal agent with encrypted memory and a real tool loop. Part of the 2026-09-19 midnight deploy convoy; the originating brief is in chat history.

## References

_None recorded yet._

## Findings

- Real planner/tool/reply loop through an optional Token Harbor or OpenRouter connection: send recent conversation and tool schemas to the planner, validate and execute up to six allow-listed tool calls in-browser, return results to the model for the final answer, encrypt the workspace before writing storage.
- Honest security posture: a local app cannot provide multi-device E2EE or protect an already-compromised browser or device, and Relay says so, describing itself as client-side encrypted storage.
- No direct web search: the CSP permits no search provider and a static app has no safe proxy.

## Technical decisions

- AES-256-GCM at rest (fresh 96-bit IV per save), PBKDF2-SHA-256 310k rounds, passphrase and model credential only in tab memory.
- Strict CSP with only the two model providers reachable; no analytics, cookies, accounts, remote assets or backend.
- Model output can only invoke an allow-listed tool registry.
- Pre-push secret scan (prepush-secret-scan.sh) before every push.

## Gaps

- The originating brief is in chat history (2026-09-18/19).
