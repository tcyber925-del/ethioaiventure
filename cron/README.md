# Scheduled Intelligence Jobs (opt-in)

The 5 Ethioaiventure jobs are **never auto-scheduled** on install — enable them explicitly.

## Quick start (portable)

```bash
ethioaiventure gateway install    # required: gateway daemon runs the scheduler
./cron/setup-jobs.sh              # creates all 5 jobs (uses $HERMES_HOME for paths)
ethioaiventure cron list          # verify
```

`setup-jobs.sh` contains the exact prompts, skills, schedules, `--continuity` (dedup against previous runs) and `--deliver local`. Edit it first if you want different cadences or delivery targets.

## The jobs

| Job | Schedule (EAT) | Attached skills | Purpose |
|---|---|---|---|
| daily-intelligence | `0 8 * * *` | ecosystem-research, research-reporting | Lightweight daily signal scan (Ethiopia → Africa → Global-only-if-relevant), ≤10 search calls |
| weekly-ecosystem | `0 9 * * 1` | ethiopia-intelligence, african-market-analysis, research-reporting | Weekly ecosystem intelligence report |
| weekly-opportunity | `0 9 * * 4` | opportunity-discovery, opportunity-scoring | Weekly venture opportunity scan with 13-dimension /100 scoring |
| monthly-market | `0 9 1 * *` | market-research, competitive-intelligence | Monthly market review with trend classification (Accelerating/Stable/Declining/Emerging/Disappearing) |
| monthly-strategy | `0 9 2 * *` | intelligence-dashboard, red-team, research-reporting | Monthly strategic review incl. mandatory "What We Were Wrong About" |

## Manual trigger & control

```bash
ethioaiventure cron list                 # status
ethioaiventure cron run daily-intelligence   # manual trigger (runs synchronously in the CLI)
ethioaiventure cron pause daily-intelligence
ethioaiventure cron resume daily-intelligence
ethioaiventure cron status
```

## Reports & dedup

- Reports archive to `research/intelligence/{daily,weekly,monthly}/` (date-based filenames, never overwritten across days)
- Dedup ledger: `research/intelligence/.state/ledger.json` (fingerprints of reported items) + native `--continuity`
- Every run's delivery copy is preserved under `cron/output/{job_id}/{timestamp}.md`
- Failed runs deliver a failure notice; runs that find nothing material say "No material developments detected." (or `[SILENT]` for quiet suppression)

## Delivery channels

`--deliver local` is the default. To add a channel (Telegram/Slack/etc.), put the bot token in the profile's `.env` and change `--deliver telegram` (or `telegram:<chat_id>`) on the jobs.

## Reliability notes

- Jobs run on the profile's `cron.model` (config.yaml). Slow free-tier models may need `providers.<id>.stale_timeout_seconds` raised (this distribution ships 600s) and/or `HERMES_CRON_TIMEOUT` (inactivity budget) in the gateway service environment.
- Timezone: the distribution ships `timezone: Africa/Addis_Ababa`; schedules above are in that timezone.