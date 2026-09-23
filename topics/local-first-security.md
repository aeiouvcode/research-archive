# Local-first and security baseline

Shared across the tools on this account (Afternoon, Relay, Orbit, Vault Key, Keyring Auth, Flipside, Proposal Forge, LeadForge, NoCatch, EDGE//AI, Open Muse).

## Decisions

- **No backend unless the brief needs one.** Static apps on GitHub Pages; user data stays in the browser.
- **Encryption at rest.** AES-256-GCM with a fresh 96-bit IV per save; keys derived with PBKDF2-SHA-256 (310,000 to 650,000 iterations) and a random salt; passphrase never stored.
- **Strict Content Security Policy.** `default-src 'none'`, and `connect-src` limited to the providers the user chooses, or `'none'`.
- **Bring your own key** for model providers, held in memory or encrypted, sent only to that provider.
- **No analytics, trackers or remote assets**; remote scripts pinned with SRI or vendored.
- **Pre-push secret scan** in repos that handle keys (`scan.sh`, `prepush-secret-scan.sh`).

## Sources

- Per-repo `SECURITY.md` files: vault-key, keyring-auth, orbit-graph, frameforge-studio
- Web Crypto API (MDN): https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API
