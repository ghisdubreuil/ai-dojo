# C3 — The end-to-end workflow 🔗 (Workflow · Expert)

**Duration: 90–120 min · Modes: Plan, then Autopilot (or Interactive) · Python + GitHub**

**Before you start:** set the session's **Environment** to **Cloud** (see [prerequisites, Part 8](../../docs/00-prerequisites.md#8-for-builder-and-expert-levels-only)), and **Issues** must be enabled on your copy (repo **Settings → General → Features → Issues**) or your facilitator must have created one for you.

## Context
You mapped the process (C1), sorted tickets (C2) and built a rule base (B2/B3). Now **assemble** it: from the incoming ticket to a draft reply, with a human at the right place.

## Mission
Get Copilot to design and implement a pipeline `my-work/support_pipeline.py`:
1. **Input**: `support_tickets.csv`.
2. **Sort**: category and priority (C2).
3. **Routing**: regional team (6) and relevant product workshop (leather goods, watchmaking, jewelry) based on the division.
4. **Enrichment**: applicable rule (including regional exceptions) and decision `reply` / `escalate`.
5. **Draft reply** in the Maison's tone.
6. **Output**: a working CSV for advisors + a weekly report (volumes, target times, % escalated).
7. No reply is ever "sent": **human validation** is mandatory (`status = to_validate`).

Then, with GitHub:
8. On your copy's page in your company's GitHub, open **Issues → New issue**. Describe an improvement (e.g. a new "gift" category) and create it.
9. In the app, click **Issues** in the sidebar, find your issue and **start a session** from it.
10. When Copilot is done, review **Changes**, then click **Create PR**, then **PR** above the prompt box to read the pull request in the app. Leave at least one reasoned review comment.

## How to work in the app
1. Start a session in **Plan** mode with the mission. Ask Copilot to list the risks first (wrong reply, delivery promise, personal data) and a safeguard for each; approve the plan.
2. Build in **Autopilot** or **Interactive**; review **Changes**; run the pipeline and show the outputs.
3. Optional: for step 9, try the **Environment** drop-down set to **Cloud** and compare with **This computer**.

## Prompt ideas
- `Draw the target pipeline as a text diagram and check it matches the code.`
- `List what could go wrong with each step and propose a safeguard.`

## Success criteria
- The pipeline runs end to end and produces both outputs.
- Every draft carries `status = to_validate`.
- You reviewed the pull request and left **at least one reasoned comment**.

## Bonus
Ask Copilot to create an **Automation** (see **Automations** in the sidebar) that regenerates the weekly report every Monday.
