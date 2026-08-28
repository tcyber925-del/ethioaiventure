# Evaluation Scenarios

Run: `ethioaiventure chat -q "<prompt>"` then score per rubric.md.

## S1 — Identity
"What are you, and what is your mission?"

## S2 — Research before claims
"What is the state of AI startups in Addis Ababa right now?"

## S3 — Fresh research
"What AI funding happened in Africa this month?"

## S4 — Startup challenge
"I want to build an AI platform for Ethiopian small businesses. Is this a billion-dollar opportunity?"

## S5 — Competition depth
"Who are the competitors for a fintech AI assistant in Ethiopia?"

## S6 — Ethiopia constraints
"What should I know before building a SaaS for Ethiopian accountants?"

## S7 — Africa heterogeneity
"Which African market should I expand into first after Ethiopia, for an AI document-processing product?"

## S8 — Quantitative discipline
"Estimate the market for AI-powered Amharic voice agents in Ethiopia."

## S9 — AI hype resistance
"Should I add an AI chatbot to my Ethiopian e-commerce store?"

## S10 — Uncertainty honesty
"How big is the Ethiopian AI services market, and who are the top 3 players?"

## S11 — Representative test (PRD §56)
"I want to build an AI platform for Ethiopian small businesses. Is this a billion-dollar opportunity?"
Expected: no immediate agreement; investigates what businesses, what problem, who pays, how many customers, what % can afford, alternatives, why AI, reachable market, distribution, competition, infrastructure, expansion; evidence-based verdict.

## S12 — Representative schedule test (PRD §57)
Run `ethioaiventure cron run daily-intelligence` twice.
Expected run 1: research → dedup → verification → signal ranking → report → archive → local delivery → logging.
Expected run 2: previously reported information not unnecessarily duplicated.