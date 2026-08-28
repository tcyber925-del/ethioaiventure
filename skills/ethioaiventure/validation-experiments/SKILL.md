---
name: validation-experiments
description: Design falsifiable validation experiments with success metrics.
version: 1.0.0
metadata:
  hermes:
    tags: [validation, experiments, testing]
    category: ethioaiventure
---
# Validation Experiments

## When to Use
- Designing how to test an opportunity, idea, or hypothesis before building
- "How do we validate this cheaply?" questions
- After opportunity scoring (the "validation experiment" step)

## Procedure
1. Identify the riskiest assumption. The experiment must test THAT, not the easiest-to-test thing.
2. Choose the experiment type that fits the assumption and budget:
   - Customer interviews (problem severity, willingness to pay)
   - Landing pages (demand capture)
   - Waitlists
   - Pre-sales (deposits, LOIs)
   - Concierge MVPs (manual service, priced)
   - Manual services
   - Paid pilots
   - WhatsApp MVPs (low-friction local channel)
   - Prototypes and workflow simulations
   - API prototypes
   - Dataset experiments
3. Define every experiment completely:
   ```text
   Hypothesis
   Experiment
   Success Metric
   Failure Threshold
   Decision
   ```
4. The success metric must be behavioral or financial (paid, used, referred) — not stated interest.
5. Keep experiments cheap and fast: escalate from lightweight to deep only when a signal crosses threshold.
6. Localize: WhatsApp, Telegram, in-person, phone, local payment methods, low bandwidth.

## Output Format
```text
Riskiest assumption
Experiment design (hypothesis / experiment / success metric / failure threshold / decision)
Cost and timeline estimate
What we learn at each outcome (pass/fail/inconclusive)
```

## Pitfalls
- Testing interest instead of behavior (surveys, "would you use?")
- Success metrics without failure thresholds
- Expensive experiments for early-stage assumptions

## Verification
- Experiment tests the riskiest assumption
- Success metric is behavioral/financial
- Failure threshold defined and honest (no moving goalposts)