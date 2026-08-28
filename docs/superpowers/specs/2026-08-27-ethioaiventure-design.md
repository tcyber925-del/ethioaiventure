# Ethioaiventure — Agent Profile Design

**Date:** 2026-08-27
**Status:** Approved for implementation
**Target:** `~/.hermes/profiles/ethioaiventure/` · Hermes Agent v0.20.4
**Source:** `docs/prd` (v2.0, iterated via interview 2026-08-27)

---

## 1. Objective

Build a production-quality Hermes agent profile named **Ethioaiventure**: an Ethiopian & African AI venture intelligence agent. Layered architecture: identity (SOUL.md) → skills (22 thin shells + shared resources) → scheduled intelligence (5 native cron jobs) → storage/memory → evaluation.

Operating loop: **What is true → What is changing → What opportunity exists → What should we test → What should we build next?**

---

## 2. Decisions (from interview + doc verification)

| Topic | Decision |
|---|---|
| Scope | Core-first, 3 iterations + Phase 0 inspection |
| Skills | 22 thin SKILL.md shells + `_shared/` resources (no duplication) |
| Skill location | New category `skills/ethioaiventure/<skill>/SKILL.md`, Hermes frontmatter |
| Scheduler | **Native Hermes cron** (verified: full cron subsystem; systemd only via `hermes gateway install`) |
| Delivery | `deliver: local` now; channel-ready (Telegram/etc. via `.env` + `deliver:` swap) |
| Dedup | Native `--continuity` + `.state/` ledger fingerprints |
| Language | English only; local-language sources valued as evidence |
| Eval | Scenario prompts + rubric + 2 representative runbooks |
| Timezone | `timezone: "Africa/Addis_Ababa"` top-level config key (verified: governs cron + prompt time) |
| Memory | Native auto-memory (`memories/MEMORY.md` + `USER.md`, `memory` tool); SOUL encodes verified-facts-only discipline |
| AGENTS.md | Dropped (Hermes only injects via cron `--workdir`, which serializes jobs) — routing via SOUL section + skill descriptions + per-job `--skill` |
| PRD count fix | PRD says "21 skills", lists 22 — build all 22 |

---

## 3. Filesystem layout

```
~/.hermes/profiles/ethioaiventure/
├── SOUL.md                          # identity, mission, principles, evidence discipline, routing
├── config.yaml                      # timezone, cron.model, terminal.cwd, cron.wrap_response: false
├── .env                             # untouched (no new credentials)
├── skills/ethioaiventure/
│   ├── _shared/                     # ignored by discovery; read via tools
│   │   ├── evidence-classification.md
│   │   ├── source-evaluation.md
│   │   ├── scoring-matrix.md
│   │   └── report-templates/
│   ├── ecosystem-research/SKILL.md
│   ├── ethiopia-intelligence/SKILL.md
│   ├── african-market-analysis/SKILL.md
│   ├── market-research/SKILL.md
│   ├── startup-validation/SKILL.md
│   ├── opportunity-discovery/SKILL.md
│   ├── competitive-intelligence/SKILL.md
│   ├── ai-research/SKILL.md
│   ├── customer-discovery/SKILL.md
│   ├── business-model-analysis/SKILL.md
│   ├── ai-agent-analysis/SKILL.md
│   ├── product-strategy/SKILL.md
│   ├── ai-architecture/SKILL.md
│   ├── ai-economics/SKILL.md
│   ├── policy-regulation/SKILL.md
│   ├── investment-intelligence/SKILL.md
│   ├── due-diligence/SKILL.md
│   ├── opportunity-scoring/SKILL.md
│   ├── validation-experiments/SKILL.md
│   ├── intelligence-dashboard/SKILL.md
│   ├── research-reporting/SKILL.md
│   └── red-team/SKILL.md
├── research/intelligence/
│   ├── daily/        # 2026-08-27.md
│   ├── weekly/       # 2026-W35.md
│   ├── monthly/      # 2026-08.md
│   ├── alerts/
│   └── .state/       # dedup ledger (fingerprints)
├── evaluations/
│   ├── scenarios/    # 10 scenario prompts
│   ├── rubric.md
│   └── runbooks/     # representative tests (PRD §56-57)
└── cron/             # Hermes-managed: jobs.json, output/{job_id}/{ts}.md, executions.db
```

---

## 4. SOUL.md content outline

Identity, mission ("Turn AI knowledge into African intelligence, and African problems into validated AI opportunities"), strategic question, geographic tiers (Ethiopia → East Africa → Africa → Global), 20 reasoning principles (PRD §7), evidence classification (FACT/REPORTED/INFERENCE/ESTIMATE/ASSUMPTION/SCENARIO/SPECULATION/UNVERIFIED), source hierarchy (Tier 1-3), current-information rule, memory discipline (verified facts only), uncertainty behavior, communication style, skill-routing guide (when to invoke which of the 22 skills). No procedural workflows.

---

## 5. Skills

22 skills, each: frontmatter (`name`, `description` ≤60 chars, `version`, `metadata.hermes.tags`, `category: ethioaiventure`) + sections (When to Use / Procedure / Pitfalls / Verification). Shared resources referenced from `_shared/`. No duplication of SOUL content. Core five built in Iteration 1: ecosystem-research, startup-validation, opportunity-scoring, research-reporting, red-team.

---

## 6. Scheduler (native Hermes cron)

| Job | Schedule | Skills | Reasoning effort | Toolsets |
|---|---|---|---|---|
| daily-intelligence | `0 8 * * *` | ecosystem-research, research-reporting | low | web, file |
| weekly-ecosystem | `0 9 * * 1` | ethiopia-intelligence, african-market-analysis, research-reporting | medium | web, file, browser |
| weekly-opportunity | `0 9 * * 4` | opportunity-discovery, opportunity-scoring | medium | web, file |
| monthly-market | `0 9 1 * *` | market-research, competitive-intelligence | high | web, file, browser |
| monthly-strategy | `0 9 2 * *` | intelligence-dashboard, red-team, research-reporting | high | web, file |

All jobs: `--continuity` (native dedup), `--deliver local`, archive prompt → `research/intelligence/<bucket>/<date>.md`, quality filter, "No material developments detected." honesty rule, source retention, failure-safe (native: preflight, executions.db, failure streaks, incidents). Jobs created via `hermes cron create` CLI (pins are user-owned; agent tool cannot set them). Manual control: `ethioaiventure cron list/run/pause/resume/status` + `/cron` in chat.

`config.yaml`: `timezone: Africa/Addis_Ababa`, `cron.model` pinned, `cron.wrap_response: false`, absolute `terminal.cwd`.

---

## 7. Storage & memory

- Reports: `research/intelligence/{daily,weekly,monthly,alerts}/` with date filenames; never overwrite
- Dedup: native `--continuity` (own previous output) + `.state/` ledger (source URL fingerprint, title hash, reported status)
- Memory: only durable verified facts via `memory` tool; inferences stay in research/analysis

---

## 8. Evaluation

- `evaluations/scenarios/`: 10 prompts — identity, research-before-claims, fresh-research, startup-challenge, competitor-depth, Ethiopia-constraints, Africa-heterogeneity, quantitative-exposure, AI-hype-resistance, uncertainty/no-fabrication
- `evaluations/rubric.md`: scoring per PRD §55-60
- `evaluations/runbooks/`: representative tests — §56 ("billion-dollar opportunity" verdict), §57 (daily job dedup on second run)
- Run via `ethioaiventure chat -q` (one-shot)

---

## 9. Phasing

- **Phase 0 — Inspection**: doctor, skills list, cron list, gateway status, .env presence, memories, reusable skills
- **Iteration 1 — Identity + Core**: SOUL.md, `_shared/`, 5 core skills, config.yaml
- **Iteration 2 — Remaining skills**: 16 additional shells
- **Iteration 3 — Scheduler + Eval**: gateway install, 5 cron jobs, archive + ledger, test runs (dedup), eval suite + run, acceptance walkthrough (PRD §60), final deliverable summary (PRD §61)

---

## 10. Safety (PRD §58)

Only touch this profile. Add new skill category only; never modify existing skills. No credentials, no hardcoded keys, no new dependencies, no duplicate schedulers/tools. Reuse existing profile skills where they satisfy a requirement. Do not overwrite `.env` or unrelated config.

---

## 11. Acceptance (PRD §60, condensed)

Identity separated from workflows · SOUL.md exists · Ethiopia/Africa-first reasoning · evidence discipline · 22 skills with activation conditions, workflows, outputs · no duplication · daily/weekly/monthly jobs work · reports archived · dedup works · failures logged · timezone correct · delivery local (channel-ready) · eval suite exists and passes.