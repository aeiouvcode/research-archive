# EDGE//AI

- Repository: https://github.com/aeiouvcode/edge-ai
- Live: https://aeiouvcode.github.io/edge-ai/

## Inspiration

PocketPal and google-ai-edge/gallery (GitHub). Brief (2026-09-19): on-device inference for any model on any phone, clearly better than those.

## References

- google-ai-edge/gallery: https://github.com/google-ai-edge/gallery
- PocketPal (mobile app): the on-device chat baseline.
- AgentCloak Desktop (incountry.com): privacy-cloak pattern.

## Findings

- A device probe that tells users honestly what their phone can run is worth more than a long model list.
- Model downloads failed through the app's own CSP because the model host redirects to a CDN. Fixed by allowing the exact redirect targets.

## Technical decisions

- WebGPU with a WASM fallback, so it runs on any phone.
- Models are cached for offline use, with no backend, key or account.
- Engine files are pinned and integrity-checked, and no remote code runs.

## Gaps

- Phase plans 2-6 (compat validator, dual engine, arena, voice loop, cloud escalation) are only in chat history, 2026-09-19/20.
