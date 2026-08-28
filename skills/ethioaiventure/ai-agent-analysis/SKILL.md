---
name: ai-agent-analysis
description: Evaluate workflows for agent suitability and economic outcomes.
version: 1.0.0
metadata:
  hermes:
    tags: [agents, workflows, automation]
    category: ethioaiventure
---
# AI Agent Analysis

## When to Use
- "Should we build an AI agent for X workflow?" questions
- Evaluating automation opportunities in specific sectors/workflows
- Representative test: "Should I build an AI agent for Ethiopian accountants?"

## Procedure
1. Identify the workflow precisely: inputs, steps, decision points, outputs, people involved, tools used today.
2. Classify the automation level honestly:
   ```text
   Chatbot (answers questions)
   Copilot (assists a human)
   Workflow Automation (rules/scripts)
   AI Agent (autonomous multi-step)
   Autonomous System (self-directed, self-correcting)
   ```
3. For AI Agent or higher, evaluate: error cost (who is harmed by a wrong output?), verification path (how is output checked?), escalation (when does it hand to a human?), and trust (does the buyer trust it?).
4. Assess sectors: documents, communication, research, support, sales, accounting, compliance, procurement, logistics, scheduling, data entry, government workflows, professional services.
5. Prioritize measurable economic outcomes: hours saved × wage, error cost, revenue impact. Not "convenience".
6. Localize: Ethiopian workflows (Amharic documents, paper processes, government procedures, forex and tax compliance), cost of labor vs cost of agent, infrastructure constraints.
7. Apply validation discipline: the workflow must be observed, not assumed.

## Output Format
```text
Workflow map (as-is)
Automation classification with justification
Economic outcome analysis (estimates with assumptions)
Error and trust analysis
BUILD / TEST / WATCH / AVOID verdict
Validation experiment
```

## Pitfalls
- Assuming an AI agent is the answer before mapping the workflow
- Counting hours saved without labor cost context
- Ignoring error cost in regulated domains (accounting, legal, healthcare)

## Verification
- Workflow mapped from evidence, not assumption
- Economic outcome quantified with exposed assumptions
- Error cost and trust assessed explicitly