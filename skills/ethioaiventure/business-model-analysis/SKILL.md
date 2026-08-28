---
name: business-model-analysis
description: Evaluate business models: who pays, why, how much, and unit economics.
version: 1.0.0
metadata:
  hermes:
    tags: [business, model, pricing, economics]
    category: ethioaiventure
---
# Business Model Analysis

## When to Use
- Choosing or evaluating a business model (SaaS, API, vertical AI, agents, marketplace, consulting...)
- Pricing decisions and unit economics
- Investment assessment of a company's model

## Procedure
1. Evaluate candidate models for the specific opportunity:
   - SaaS, API, AI-as-a-Service, vertical AI, enterprise software, agents, automation, managed AI, data products, licensing, consulting, implementation, education, marketplace, transaction fees, usage-based pricing
2. Always determine:
   ```text
   Who pays?
   Why?
   How much? (in local currency, with evidence)
   How often?
   Cost to serve?
   Gross margin?
   Distribution?
   ```
3. Localize economics: Ethiopian/African unit economics, payment rails, forex, infrastructure and inference costs, sales cycles, churn.
4. Expose assumptions for every estimate (evidence-classification.md).
5. Compare models on: reach, margin, capital intensity, defensibility, and fit with local distribution reality.

## Output Format
```text
Candidate models compared (table)
Recommended model with reasoning
Unit economics (assumptions exposed)
Sensitivity: what breaks the economics?
```

## Pitfalls
- Copying Silicon Valley pricing into Ethiopian markets (USD prices, card-only payments)
- Confusing users with payers
- Ignoring cost-to-serve in low-purchasing-power markets

## Verification
- Who-pays/why/how-much answered with evidence or explicit assumptions
- Gross margin and distribution validated against local reality
- A named experiment to test willingness to pay