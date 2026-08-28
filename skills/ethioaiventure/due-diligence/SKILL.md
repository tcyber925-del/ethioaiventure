---
name: due-diligence
description: Investigate a company or opportunity across all risk dimensions.
version: 1.0.0
metadata:
  hermes:
    tags: [due-diligence, investigation, risk]
    category: ethioaiventure
---
# Due Diligence

## When to Use
- Investigating a specific company, startup, or investment target
- Separating company claims from independently verified information
- Partner/vendor/competitor deep-dives

## Procedure
1. Investigate systematically:
   ```text
   Company
   Founders
   Product
   Customers
   Market
   Competition
   Technology
   Traction
   Funding
   Economics
   Legal
   Regulatory
   Risks
   Claims
   Evidence
   Unknowns
   ```
2. For every company claim, mark verification status: independently verified / reported by company / unverifiable.
3. Search beyond the obvious: registries (Ethiopian trade/license registries where available), court/regulatory records, LinkedIn, local press, app stores, customer reviews, developer communities.
4. Verify funding and traction figures with sources; do not repeat unverified figures.
5. Assess legal/regulatory exposure: licenses, compliance, pending cases.
6. Produce a verdict: PASS / PASS WITH CONDITIONS / FAIL / INSUFFICIENT EVIDENCE.

## Output Format
```text
Per-dimension findings (company claim vs verified fact, with sources)
Verification matrix (claim | status | source | class)
Risk register
Verdict: PASS / PASS WITH CONDITIONS / FAIL / INSUFFICIENT EVIDENCE
Open questions and recommended next verification steps
```

## Pitfalls
- Trusting company materials as fact
- Missing local registries and local press
- Unverified funding figures repeated as fact

## Verification
- Each major claim categorized as company-reported vs independently verified
- Sources retained for everything verified
- Verdict justified by evidence