---
name: opportunity-discovery
description: Find venture opportunities from technologies, gaps, regulation, and signals.
version: 1.0.0
metadata:
  hermes:
    tags: [opportunity, discovery, signals]
    category: ethioaiventure
---
# Opportunity Discovery

## When to Use
- "What opportunities exist in X?" questions
- Weekly opportunity scan (cron job attaches this skill)
- Converting research signals into candidate opportunities

## Procedure
1. Scan signal sources for opportunities:
   - Emerging technologies (model capabilities, cost drops, new APIs)
   - Research breakthroughs (arxiv, academic output)
   - Market failures and infrastructure gaps
   - Regulation changes (new rules creating needs)
   - Language gaps (Amharic, Afaan Oromo, Tigrinya, Somali, Afar AI coverage)
   - Data scarcity (what data is missing and who needs it)
   - Workforce constraints (skills gaps, automation candidates)
   - Enterprise inefficiency (document workflows, compliance, procurement)
   - Demographic changes (youth population, urbanization, diaspora)
2. For each candidate opportunity, map it completely:
   ```text
   Problem
   Customer
   Current Alternative
   AI Advantage
   Business Model
   Distribution
   Market
   Competition
   Defensibility
   Expansion
   ```
3. Apply evidence discipline to each element.
4. Do not generate opportunities to fill a quota — quality over quantity.
5. Rank candidates; deep-dive the top ones with opportunity-scoring.

## Output Format
```text
Candidate opportunities (mapped per the 10-element structure)
Evidence notes per element (class + confidence)
Ranks with one-line rationale
Recommended scoring candidates
```

## Pitfalls
- Generating generic AI ideas (chatbot for X) without a specific problem or customer
- Ignoring distribution and payments reality
- Suggesting AI where it adds no leverage

## Verification
- Each opportunity names a specific customer and current alternative
- AI advantage is explicit and non-generic
- Disconfirming evidence considered (why hasn't this been done?)