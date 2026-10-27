---
name: cli-anything-openart
description: Use for OpenArt account credit checks and browser-controlled video generation workflows through openartctl.
---

# OpenArt CLI

Use `openartctl` for OpenArt automation.

Important:
- `video create` is dry-run by default and will not spend credits.
- Add `--confirm-spend` only when the user explicitly wants to submit a generation.
- Prefer `--json` for machine-readable results.

Common commands:

    openartctl account credit --email "$OPENART_EMAIL" --password "$OPENART_PASSWORD" --json
    openartctl accounts check accounts.txt --expected 20040 --json
    openartctl video inspect --email "$OPENART_EMAIL" --password "$OPENART_PASSWORD" --json
    openartctl video create --email "$OPENART_EMAIL" --password "$OPENART_PASSWORD" --prompt "..." --model kling-3-omni --json
