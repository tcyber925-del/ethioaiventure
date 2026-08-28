---
name: ecosystem-research
description: Map an ecosystem's players, institutions, capital, talent, and signals.
version: 1.0.0
metadata:
  hermes:
    tags: [research, ecosystem, ethiopia, africa]
    category: ethioaiventure
---
# Ecosystem Research

## When to Use
- User asks to map an ecosystem: Ethiopian, East African, African, or sector-specific (AI, fintech, agritech, healthtech, etc.)
- Before evaluating a startup, market, or opportunity in an unfamiliar ecosystem
- Weekly ecosystem report generation (cron job attaches this skill)

## Procedure
1. Confirm scope: geography (tier), sector, and time horizon. Clarify if ambiguous.
2. Research, in order of priority:
   - Companies and startups (founded, stage, focus, evidence class)
   - Founders and teams
   - Researchers and research groups (universities, labs)
   - Investors, accelerators, incubators, DFIs, grant programs
   - Government and regulatory actors, policy signals
   - Infrastructure: payments, connectivity, identity, logistics, compute
   - Communities: developer groups, meetups, associations
   - Technologies in use and emerging
3. Use fresh research for current state (current-information rule); use Tier 1 sources first.
4. For each entity found, record: what it is, stage, funding (verified only), focus, and source.
5. Consult `_shared/source-evaluation.md` and `_shared/evidence-classification.md` for discipline.
6. Produce output in the structured format below.

## Output Format
```text
Ecosystem Overview
Major Players
Institutions
Infrastructure
Capital
Research
Talent
Policy
Emerging Signals
Opportunities
Risks
Unknowns
```

## Pitfalls
- Treating absence of search results as absence of players (never assume no competition)
- Fabricating companies, funding, or market sizes — every entity must trace to a source
- Treating Africa or even Ethiopia as homogeneous — segment by sector, city, income
- Relying on stale memory for current state

## Verification
- Every named company/funding figure has a source (class + confidence)
- Unknowns section lists what could not be verified
- At least one attempt at disconfirming evidence (e.g., searching for who might NOT exist or failed attempts)