---
name: red-team
description: Challenge strong claims, assumptions, and conclusions adversarially.
version: 1.0.0
metadata:
  hermes:
    tags: [red-team, challenge, risk]
    category: ethioaiventure
---
# Red-Team

## When to Use
- Before finalizing any major recommendation, score, or verdict
- User asks "challenge this", "what's wrong with this", "is this too optimistic"
- Monthly strategic review (cron job attaches this skill)

## Procedure
1. Identify every strong claim in the material: market sizes, willingness to pay, AI necessity, defensibility, economics, execution ability, distribution, competition.
2. For each claim, attack it:
   - **Market size**: Is this TAM or reachable? Who actually pays, in this economy, in this currency?
   - **Willingness to pay**: Is there evidence, or assumption? What do alternatives cost?
   - **Alternatives**: What are people doing today without this product? Is "do nothing" the competitor?
   - **Incumbents**: Who loses if this wins? What will they do?
   - **AI necessity**: Would this work as well with rules, humans, or paper?
   - **Economics**: CAC vs LTV with Ethiopian unit economics. Inference costs. Payback.
   - **Distribution**: How do you actually reach customers here — payments, trust, channels?
   - **Defensibility**: If it works, what stops a copy?
   - **Execution**: Has this team done this before? In this market?
   - **Assumptions**: List every assumption and rate its fragility.
3. Search for disconfirming evidence actively — do not rely on the existing research only.
4. Always answer: **What evidence would change our conclusion?**

## Output Format
```text
Claims Under Attack: (each with verdict: SURVIVES / WEAKENED / FAILS)
Attack details per claim (evidence class + confidence)
Assumptions and their fragility
Disconfirming evidence found (or: none found despite search)
What evidence would change the conclusion:
Revised conclusion (if warranted):
```

## Pitfalls
- Performative doubt without actual research — attacks must be evidence-based, not rhetorical
- Attacking only easy targets and sparing the user's favorite idea
- Ignoring Ethiopia/Africa-specific attack angles

## Verification
- Every major claim in the original material was attacked
- At least one fresh disconfirming search performed
- The "what evidence would change" question answered for the central claim