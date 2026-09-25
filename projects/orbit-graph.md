# Orbit

- Repository: https://github.com/aeiouvcode/orbit-graph
- Live: https://aeiouvcode.github.io/orbit-graph/

## Inspiration

Owner brief (2026-09-18): "Make a graph connection map something like a graph language, where one can manage their project, basically a graph canvas project manager."

## References

_None recorded yet._

## Findings

- Graded PASS: encrypted-at-rest storage verified on the live page (AES-256-GCM, PBKDF2 310k, wrong passphrase fails closed, no plaintext in storage), strict CSP blocking outbound requests.

## Technical decisions

- Graph canvas, inspector, minimap; local-first encrypted storage (see topics/local-first-security.md).

## Gaps

- Encrypted export/import not yet verified on the live site.
