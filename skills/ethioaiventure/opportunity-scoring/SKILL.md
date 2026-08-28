---
name: opportunity-scoring
description: Score opportunities across 13 dimensions with evidence and a /100 verdict.
version: 1.0.0
metadata:
  hermes:
    tags: [scoring, opportunity, ranking]
    category: ethioaiventure
---
# Opportunity Scoring

## When to Use
- Ranking or scoring opportunities, options, or venture ideas
- Weekly opportunity scan report (cron job attaches this skill)
- Comparing competing opportunities for prioritization

## Procedure
1. Load the scoring matrix: `_shared/scoring-matrix.md`.
2. Gather evidence for each dimension BEFORE scoring. Do not score on intuition alone.
3. Score all 13 dimensions /10 with a one-line justification each:
   problem severity, market size, growth, AI leverage, willingness to pay, competition, technical feasibility, data availability, distribution, defensibility, capital efficiency, Ethiopia/Africa advantage, expansion potential.
4. Attach evidence class + confidence to each justification (see `_shared/evidence-classification.md`).
5. Compute overall /100.
6. Red-team the score: what evidence would change it? What was assumed?
7. Assign verdict: BUILD (70+, strong evidence), TEST (50-69), WATCH (30-49), AVOID (<30 or fatal flaw).

## Output Format
```text
Dimension scores (table with justifications, class, confidence)
Overall Score: /100
Verdict: BUILD / TEST / WATCH / AVOID
Evidence that would change the score:
Validation experiment:
```

## Pitfalls
- Letting the score replace reasoning (it never does)
- Scoring without evidence — a score without a source is speculation
- Inflating market size with TAM fantasy instead of reachable market
- Ignoring the Ethiopia/Africa structural dimension

## Verification
- Each of the 13 dimensions has a written justification with evidence class
- Confidence stated for consequential dimensions
- Disconfirming evidence considered before finalizing