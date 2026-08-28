# Ethioaiventure — Ethiopian & African AI Venture Intelligence Agent

A Hermes Agent profile distribution: an AI ecosystem intelligence, research, market validation, strategy, and venture-building agent focused on Ethiopia, East Africa, Africa, and emerging markets.

> **Turn AI knowledge into African intelligence, and African problems into validated AI opportunities.**

## What's included

- **SOUL.md** — identity, mission, 20 reasoning principles, evidence discipline, source hierarchy, skill routing
- **22 skills** (`skills/ethioaiventure/`) — ecosystem-research, ethiopia-intelligence, african-market-analysis, market-research, startup-validation, opportunity-discovery, competitive-intelligence, ai-research, customer-discovery, business-model-analysis, ai-agent-analysis, product-strategy, ai-architecture, ai-economics, policy-regulation, investment-intelligence, due-diligence, opportunity-scoring, validation-experiments, intelligence-dashboard, research-reporting, red-team — plus shared resources (`_shared/`: evidence classification, source evaluation, scoring matrix, report templates)
- **config.yaml** — Nous Portal provider, `timezone: Africa/Addis_Ababa`, pinned cron model, 600s API patience for slow models
- **evaluations/** — scenario prompts + rubric + runbooks (PRD §55–57)
- **docs/** — the original PRD, design spec, and implementation summary
- **cron/** — the 5 scheduled intelligence jobs (defined in `cron/README.md`; **not auto-scheduled** — you enable them explicitly)

## Install

```bash
hermes profile install github.com/tcyber925-del/ethioaiventure --alias
```

Then configure a model for the profile:

```bash
ethioaiventure setup                    # interactive wizard, or:
ethioaiventure setup --portal           # Nous Portal OAuth (one-shot, recommended)
# or point it at any provider you already use:
ethioaiventure config set model.provider openrouter
ethioaiventure config set model.default anthropic/claude-sonnet-4
```

Start chatting:

```bash
ethioaiventure chat
```

## Scheduled intelligence (optional, opt-in)

The 5 jobs are defined in `cron/README.md` with exact `hermes cron create` commands:

| Job | Schedule (EAT) | Purpose |
|---|---|---|
| daily-intelligence | 0 8 * * * | Lightweight daily signal scan (Ethiopia → Africa → Global) |
| weekly-ecosystem | 0 9 * * 1 | Weekly ecosystem intelligence report |
| weekly-opportunity | 0 9 * * 4 | Weekly venture opportunity scan with /100 scoring |
| monthly-market | 0 9 1 * * | Monthly market review with trend classification |
| monthly-strategy | 0 9 2 * * | Monthly strategic review incl. "What We Were Wrong About" |

All jobs use `--continuity` (native dedup against previous runs) and `--deliver local` (archive + local delivery; add a Telegram/Slack token to `.env` and swap `--deliver telegram` for channel delivery).

Enable the gateway for scheduled fires:

```bash
ethioaiventure gateway install
```

## Update

```bash
hermes profile update ethioaiventure
```

Your memories, sessions, `.env`, and local config are never touched by updates.

## Notes

- Reports archive to `research/intelligence/{daily,weekly,monthly}/` with a dedup ledger at `research/intelligence/.state/ledger.json`
- Evidence discipline is baked into the SOUL: FACT/REPORTED/INFERENCE/ESTIMATE/ASSUMPTION/SCENARIO/SPECULATION/UNVERIFIED, Tier 1–3 source hierarchy, "I could not verify this." honesty rule
- Cron jobs from a distribution are never auto-scheduled — enable them yourself (see `cron/README.md`)

## License

MIT