---
name: ai-architecture
description: Design AI systems: models, RAG, agents, data, and deployment trade-offs.
version: 1.0.0
metadata:
  hermes:
    tags: [architecture, ai, systems, design]
    category: ethioaiventure
---
# AI Architecture

## When to Use
- Designing the technical architecture of an AI product
- Choosing models, RAG vs fine-tuning, agents, databases, deployment
- Technical feasibility assessment for opportunities

## Procedure
1. Ground the design in the validated use case: inputs, outputs, volume, latency needs, error tolerance, users.
2. Choose from the toolbox:
   - Foundation models (hosted APIs vs open-source)
   - RAG (retrieval, chunking, vector DBs)
   - Agents (tools, orchestration, guardrails)
   - Knowledge graphs, relational databases
   - OCR, speech, computer vision components
   - Fine-tuning (when needed, and when not)
   - Local inference, cloud, edge deployment
3. Evaluate along:
   ```text
   Cost
   Latency
   Reliability
   Privacy
   Security
   Data Sovereignty
   Availability
   Maintainability
   ```
4. Localize: Ethiopian/African constraints — power reliability, connectivity cost, forex for USD API spend, local hosting options, data residency regulation, offline tolerance.
5. Prefer the simplest architecture that meets requirements. YAGNI.

## Output Format
```text
Architecture diagram (text) and component choices
Per-component rationale (why this model/DB/deployment)
Trade-off evaluation table
Cost estimate (see ai-economics)
Risks and failure modes
```

## Pitfalls
- Over-engineering (agents + fine-tuning + knowledge graphs for a form-filler)
- Ignoring forex/infrastructure costs of hosted APIs in Ethiopia
- No failure-mode analysis for unreliable connectivity

## Verification
- Each choice justified against the 8 evaluation axes
- Simplest sufficient architecture explicitly considered
- Local constraints addressed