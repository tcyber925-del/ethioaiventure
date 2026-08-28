---
name: research-reporting
description: Structure deep research into a complete evidence-based report.
version: 1.0.0
metadata:
  hermes:
    tags: [reporting, research, writing]
    category: ethioaiventure
---
# Research Reporting

## When to Use
- Producing deep research output for the user
- Daily/weekly/monthly scheduled reports (cron jobs attach this skill)
- Any output that must end in strategic recommendations

## Procedure
1. Ensure the underlying research is complete: ecosystem mapped, claims verified, sources retained.
2. Apply the research quality gate before writing:
   ```text
   [ ] Important claims verified
   [ ] Primary sources prioritized
   [ ] Facts separated from inference
   [ ] Estimates expose assumptions
   [ ] Competitors searched
   [ ] Ethiopia localization considered
   [ ] Africa treated as heterogeneous
   [ ] Quantification attempted where useful
   [ ] Uncertainty identified
   [ ] Disconfirming evidence considered
   [ ] Recommended action provided
   ```
3. For scheduled reports additionally check:
   ```text
   [ ] Story is genuinely new or materially updated
   [ ] Duplicate detection performed (prior output + dedup ledger)
   [ ] Sources retained
   [ ] No fabricated activity
   [ ] No unsupported conclusions
   ```
4. For daily/weekly/monthly reports, use the matching template in `_shared/report-templates/`.
5. For deep research, use the structure below.

## Output Format (deep research)
```text
Executive Summary
Key Findings
Market Overview
Ecosystem Map
Major Players
Technology Landscape
Competitive Landscape
Customer Segments
Business Models
Opportunities
Risks
Ethiopia-Specific Analysis
Africa Expansion Analysis
Quantitative Analysis
Strategic Recommendations
What I Would Do
Open Questions
Sources
```

## Pitfalls
- Writing before research is complete
- Vague claims without classification or sources
- Fabricating activity in scheduled reports to look productive
- Re-reporting previously reported stories without material updates

## Verification
- Quality gate checklist passed
- Every major claim classified and sourced
- Sources section complete (source, publication date, discovery date, source type, confidence, verification status)
- Recommended actions present and actionable