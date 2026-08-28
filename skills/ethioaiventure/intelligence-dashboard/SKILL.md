---
name: intelligence-dashboard
description: Produce a structured ecosystem pulse: signals, risks, what matters.
version: 1.0.0
metadata:
  hermes:
    tags: [dashboard, intelligence, signals]
    category: ethioaiventure
---
# Intelligence Dashboard

## When to Use
- Producing an ecosystem pulse / intelligence digest (Ethiopia + Africa + Global)
- Summarizing gathered intelligence into a signal-focused brief
- Monthly strategic review input (cron job attaches this skill)

## Procedure
1. Gather the intelligence (from research just performed or provided material).
2. Apply the quality filter to every candidate item:
   ```text
   Relevance + Materiality + Credibility + Novelty + African/Ethiopian impact
   ```
3. Prioritize signal over volume. If nothing meaningful happened, say so — do not fabricate activity.
4. Organize into the standard pulse format.
5. For each major item include: what happened, why it matters, evidence, confidence, potential opportunity, recommended action.
6. Deduplicate against prior output and the dedup ledger.

## Output Format
```text
AI ECOSYSTEM PULSE

ETHIOPIA
- Major developments / Startups / Research / Policy / Investment / Infrastructure

AFRICA
- Major developments / Funding / Startups / Research / Policy / Infrastructure

GLOBAL
- Technology / Models / Agents / Infrastructure / Research

OPPORTUNITY SIGNALS

RISK SIGNALS

WHAT MATTERS

WHAT TO WATCH
```

## Pitfalls
- Volume over signal (listing everything found)
- Including global items without African relevance
- Re-reporting known stories without updates

## Verification
- Quality filter applied to each item
- Every item has evidence and confidence
- "No material developments detected." used when true