# C3 — The end-to-end workflow 🔗 (Workflow · Expert)

**Duration: 90–120 min · Copilot modes: Plan then Agent (+ Copilot coding agent if your plan includes it) · Python + GitHub**

## Context
You mapped the process (C1), sorted tickets (C2) and built a rule base (B2/B3). Now **assemble** it: from the incoming ticket to a draft reply, with a human at the right place.

## Mission
Design and implement a pipeline `my-work/support_pipeline.py`:
1. **Input**: `support_tickets.csv`.
2. **Sort**: category and priority (C2).
3. **Routing**: regional team (6) and relevant product workshop (leather goods, watchmaking, jewelry) based on the division.
4. **Enrichment**: applicable rule (including regional exceptions) and decision `reply` / `escalate`.
5. **Draft reply** in the Maison's tone.
6. **Output**: a working CSV for advisors + a weekly report (volumes, target times, % escalated).
7. No reply is ever "sent": **human validation** is mandatory (`status = to_validate`).

Then, on GitHub:
8. Create an **issue** describing an improvement (e.g. a new "gift" category) and assign it to the **Copilot coding agent** if available on your plan; otherwise implement it yourself with Agent mode in a branch. Review the resulting pull request.

## Copilot hints
- `Before coding, list the risks of this workflow (wrong reply, delivery promise, personal data) and propose a safeguard for each.`
- `Draw the target pipeline as a Mermaid diagram and check it matches the code.`

## Success criteria
- The pipeline runs end to end and produces both outputs.
- Every draft carries `status = to_validate`.
- You reviewed the pull request and left **at least one reasoned comment**.

## Bonus
Schedule the report every Monday with GitHub Actions.
