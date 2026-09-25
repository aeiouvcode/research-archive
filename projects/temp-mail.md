# Ghostpost

- Repository: https://github.com/aeiouvcode/temp-mail
- Live: https://aeiouvcode.github.io/temp-mail/

## Inspiration

Owner brief (2026-09-20): "Create temp mail like service."

## References

- mail.tm API: the provider chosen; documented as the blocker below.

## Findings

- UI PASS: custom aliases, multiple inboxes, live polling, copy/QR/burn, expiry countdown, sandboxed HTML mail preview, AES-GCM local vault, session-only default.
- The one thing that matters FAILS: mail.tm's API sends no browser CORS headers, so a Pages-hosted front end cannot fetch it - confirmed in live Chrome. Same CORS wall that hit Token Harbor (see projects/afternoon.md).
- Graded PARTIAL and blocked on the owner's decision between: (1) a tiny stateless Cloudflare Worker relay - works tonight but is a backend, which the local-first rule says no to; (2) a temp-mail provider whose API allows browser CORS - none known among the free no-key ones.

## Technical decisions

- Local AES-GCM vault with session-only default.

## Gaps

- Awaiting the owner's pick between the relay and a CORS-friendly provider (unanswered since 2026-09-20).
