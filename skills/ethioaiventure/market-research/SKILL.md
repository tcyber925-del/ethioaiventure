---
name: market-research
description: Analyze TAM, SAM, SOM, segments, adoption, competition, and distribution.
version: 1.0.0
metadata:
  hermes:
    tags: [market, research, sizing]
    category: ethioaiventure
---
# Market Research

## When to Use
- Sizing a market (TAM/SAM/SOM)
- Understanding customer segments, growth, adoption, competition, substitutes, supply chain, purchasing behavior, distribution
- Monthly market review (cron job attaches this skill)

## Procedure
1. Define the market precisely: geography, sector, customer type, currency.
2. Build bottom-up: identify the actual population of buyers (not users), segment by affordability and access, then derive SOM from distribution reality. Never start from a top-down TAM headline.
3. Analyze:
   - TAM (with method and assumptions), SAM, SOM
   - Customer segments (who buys, who uses, who decides — never confuse)
   - Growth and adoption (observed data vs derived estimates)
   - Competitors and substitutes (including informal/doing-nothing)
   - Supply chain and distribution channels
   - Purchasing behavior (budget cycles, procurement, cash vs digital)
4. Clearly separate observed data from derived estimates; expose all assumptions (evidence-classification.md).
5. Localize: Ethiopian and African unit economics, affordability, and infrastructure.

## Output Format
```text
Market definition
TAM / SAM / SOM (each with method, assumptions, evidence class)
Segments (buyer / user / decision maker per segment)
Growth & adoption evidence
Competition & substitutes
Distribution reality
Purchasing behavior
Key uncertainties
```

## Pitfalls
- TAM fantasy: a billion-dollar TAM that is unreachable is not an opportunity
- Confusing users with paying customers
- Presenting derived estimates as observed data

## Verification
- Every number has method + assumptions + class
- SOM derived from distribution reality, not percentage of TAM
- Ethiopia/Africa affordability checked