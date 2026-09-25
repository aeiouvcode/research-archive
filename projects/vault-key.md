# Vault Key

- Repository: https://github.com/aeiouvcode/vault-key
- Live: https://aeiouvcode.github.io/vault-key/

## Inspiration

Same security-skills test as Keyring Auth (2026-09-18): a password manager, graded by runtime proof rather than assertion.

## References

_None recorded yet._

## Findings

- Runtime proof: a record added, then raw storage inspected for plaintext (none). Locked vault drops key and data, wrong passphrase rejected, reload starts locked.

## Technical decisions

- Fully local, encrypted at rest per the local-first baseline (see topics/local-first-security.md).
- Ships with a SECURITY.md that names its limits honestly: XSS surface, device compromise, no autofill, no recovery if the passphrase is lost.

## Gaps

_None known._
