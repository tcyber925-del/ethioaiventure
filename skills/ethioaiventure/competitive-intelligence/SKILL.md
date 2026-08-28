---
name: competitive-intelligence
description: Map direct, indirect, and substitute competitors with verified detail.
version: 1.0.0
metadata:
  hermes:
    tags: [competition, intelligence, analysis]
    category: ethioaiventure
---
# Competitive Intelligence

## When to Use
- Who are the competitors in market X / for product Y?
- Before entry decisions, pricing, or positioning
- Monthly market review's competitive section (cron job attaches this skill)

## Procedure
1. Map the full competitive set:
   - Direct competitors (same problem, same solution)
   - Indirect competitors (same problem, different solution)
   - Substitutes (including manual/offline/doing-nothing)
   - Incumbents (large players, government, telcos, banks)
   - International companies (entering or expandable)
   - African companies
   - Ethiopian companies
   - Open-source alternatives
2. Never assume lack of search results means lack of competition — search hard: local news, LinkedIn, communities, government registries, app stores, WhatsApp ecosystems.
3. For each important competitor investigate (verify what you can):
   - Product, customer, geography
   - Pricing (only when verified; state source)
   - Technology
   - Strengths and weaknesses
   - Distribution
   - Funding (only when verified)
   - Differentiation
4. Apply evidence classification to every claim about a competitor.
5. Produce a comparison and implications for the user's position.

## Output Format
```text
Competitive map (direct / indirect / substitutes / incumbents / international / African / Ethiopian / open-source)
Per-competitor detail (verified items only, with sources)
Comparison table
Positioning implications
Unknowns (what could not be verified)
```

## Pitfalls
- Only finding the obvious global players and missing local competition
- Repeating funding figures without sources
- Assuming a competitor's absence because search failed

## Verification
- Multiple search strategies used (English + Amharic/local terms, app stores, communities)
- Every pricing/funding claim sourced or marked unverified
- Substitutes and "do nothing" included