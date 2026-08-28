---
name: startup-validation
description: Stress-test a startup idea: problem, solution, market, competition, economics.
version: 1.0.0
metadata:
  hermes:
    tags: [validation, startup, strategy, africa]
    category: ethioaiventure
---
# Startup Validation

## When to Use
- User presents a startup idea or asks "should I build X?"
- Before product strategy, business model, or architecture work
- Representative test: "I want to build an AI platform for Ethiopian small businesses. Is this a billion-dollar opportunity?" — never agree immediately; investigate first

## Procedure
1. Challenge the premise first. Restate the claim and what evidence would change the verdict.
2. Investigate systematically:
   - **Problem**: severity, frequency, cost, alternatives (what do they do today?)
   - **Solution**: AI necessity (is AI needed at all?), feasibility, timing, differentiation
   - **Market**: buyer vs user vs decision maker (never confuse), willingness to pay, distribution channel, realistic reachable market (never TAM)
   - **Competition**: direct, indirect, international, African, Ethiopian, open-source, internal alternatives (spreadsheets, manual work, doing nothing)
   - **Economics**: CAC, LTV, gross margin, inference cost, infrastructure, payback period — as estimates with explicit assumptions
3. Use fresh research for current market state; verify any consequential claim.
4. Apply Ethiopia/Africa localization: Silicon Valley economics do not transfer automatically; foreign startup success does not imply local transferability.
5. Consult `_shared/evidence-classification.md` and `_shared/source-evaluation.md`.
6. End with a verdict and a validation experiment proposal.

## Output Format
```text
Problem:
Solution:
Market:
Competition:
Economics:
Evidence (class + confidence per major claim):
Validation Experiment:
Verdict: BUILD / TEST / WATCH / AVOID
```

## Pitfalls
- Confirming instead of challenging (the user wants truth, not agreement)
- Confusing TAM with obtainable opportunity
- Confusing users with paying customers
- Assuming AI is necessary because it is possible
- Inventing willingness to pay or market sizes

## Verification
- Every major claim classified and sourced
- Competitors searched beyond the obvious (including informal alternatives)
- A named validation experiment with success metric and failure threshold
- Verdict follows the evidence, even when it disappoints