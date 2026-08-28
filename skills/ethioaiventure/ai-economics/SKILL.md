---
name: ai-economics
description: Estimate AI system costs: tokens, inference, GPUs, storage, engineering.
version: 1.0.0
metadata:
  hermes:
    tags: [economics, cost, inference]
    category: ethioaiventure
---
# AI Economics

## When to Use
- Cost estimation for AI products or features
- Unit economics of AI systems (cost per transaction, per user)
- Comparing hosting/deployment cost options

## Procedure
1. Break down costs:
   - Tokens (input/output volumes, per-model pricing)
   - Inference (compute, GPU hours if self-hosted)
   - Storage (databases, vectors, files)
   - Bandwidth
   - Engineering time
   - Monitoring and observability
   - Security and compliance
   - Third-party services
2. Build the model bottom-up: estimate actual usage volumes first (users × actions × tokens), then apply pricing.
3. Convert to local reality: USD prices → forex cost in Ethiopia; infrastructure (power, connectivity) for self-hosted options.
4. Expose every assumption (evidence-classification.md): *"Estimate — based on the following assumptions."*
5. Compute: cost per transaction, cost per user per month, gross margin impact, break-even.
6. Sensitivity: what volume or price change breaks the economics?

## Output Format
```text
Cost breakdown (each line: item, volume, unit cost, total, assumption)
Cost per transaction / per user
Gross margin impact
Sensitivity analysis
Cheapest sufficient option
```

## Pitfalls
- Forgetting engineering and maintenance costs
- USD pricing applied without forex/local context
- Hidden assumption chains (each assumption unstated)

## Verification
- Every line has an explicit assumption
- Volume estimates derived from real usage patterns, not guesses
- Sensitivity tested