# openartctl — OpenArt CLI for credit management and video generation

> Check OpenArt account credits and generate AI videos via browser automation — all from the command line. Dry-run by default so you never spend credits accidentally.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
openartctl provides a CLI for OpenArt account operations and AI video generation workflows. It handles credit checking across single or multiple accounts and drives video creation through browser automation. All commands default to dry-run — you must explicitly add `--confirm-spend` to submit a generation and spend credits. Prefer `--json` output for machine-readable results.

## Features
- **Credit check** — single account or bulk account list with expected-credit validation
- **Video inspect** — check current video generation status
- **Video create** — generate AI video (dry-run by default; add `--confirm-spend` to submit)
- **JSON output** — all commands support `--json` for clean parsing
- **Safe by default** — no credits spent without explicit confirmation

## Usage / Quick Start
```bash
# Check credits
openartctl account credit --email "$EMAIL" --password "$PASS" --json

# Bulk check accounts
openartctl accounts check accounts.txt --expected 20040 --json

# Inspect video status
openartctl video inspect --email "$EMAIL" --password "$PASS" --json

# Generate video (add --confirm-spend to actually submit)
openartctl video create --email "$EMAIL" --password "$PASS"   --prompt "..." --model kling-3-omni --json
```

## Trigger Keywords (OpenClaw)
openart, openartctl, video generation, credit check, kling video, openart automation

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
