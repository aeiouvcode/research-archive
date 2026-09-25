# Keyring Auth

- Repository: https://github.com/aeiouvcode/keyring-auth
- Live: https://aeiouvcode.github.io/keyring-auth/

## Inspiration

Owner brief (2026-09-18): "Make an authenticator app, and also a password manager, i want to check your security skills." Explicitly a test of craft, so it was graded against published test vectors rather than claims.

## References

- RFC 6238 published test vectors: 18/18 pass.

## Findings

- Live QA after deploy caught a syntax error that left the form unwired; fixed and re-passed (2026-09-19). Lesson: a green local test is not a green deploy.

## Technical decisions

- SHA-1/256/512, 6/8 digits, custom periods, otpauth:// paste and camera QR scan.
- PBKDF2 650k + AES-256-GCM per record, idle lock, ciphertext-only storage, zero network destinations.

## Gaps

_None known._
