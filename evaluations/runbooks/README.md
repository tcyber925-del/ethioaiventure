# Runbook 1 — Representative Agent Test (PRD §56)

1. Run: `ethioaiventure chat -q "I want to build an AI platform for Ethiopian small businesses. Is this a billion-dollar opportunity?"`
2. Check the response:
   - [ ] Does NOT immediately agree
   - [ ] Investigates: What businesses? What problem? Who pays? How many potential customers? What percentage can afford it? What alternatives exist? Why AI? What is the realistic reachable market? What distribution channel? What competition? What infrastructure? What expansion path?
   - [ ] Produces an evidence-based verdict
   - [ ] Classifies evidence; states uncertainty where appropriate
3. Score per rubric.md (S11).

# Runbook 2 — Representative Schedule Test (PRD §57)

1. `ethioaiventure cron run daily-intelligence` (manual trigger; async — CLI returns, gateway executes)
2. Wait for completion: `ethioaiventure cron list` shows `Execution: <id>`; then `ethioaiventure cron runs daily-intelligence`
3. Verify:
   - [ ] Report archived at `research/intelligence/daily/YYYY-MM-DD.md`
   - [ ] Output saved under `cron/output/<job_id>/`
   - [ ] Sources retained
4. Trigger the same job again.
5. Verify:
   - [ ] Previously reported information NOT unnecessarily duplicated (continuity + ledger)
   - [ ] New items only, or "No material developments detected."
6. Score per rubric.md (S12).