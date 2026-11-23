# A2 — Clean and analyze 🧹 (Data · Builder)

**Duration: 60 min · Modes: Plan, then Interactive · Python (Copilot writes and runs, you review)**

**Before you start:** Python must be available (see [prerequisites, Part 7](../../docs/00-prerequisites.md#7-for-builder-and-expert-levels-only-optional-until-you-get-there)): installed on your computer, or the session's **Environment** set to **Cloud**.

> **Data:** you now work on the full raw file `data/sales.csv` (more than 21,000 rows). Do not paste it in the prompt: let Copilot write a script that processes it.

## Context
Management wants reliable revenue per store, region and division, month by month. But `data/sales.csv` is dirty. You will produce a **repeatable script** rather than a one-off manual calculation.

## Mission
Get Copilot to create `my-work/analyze_sales.py` that:
1. Loads the CSV files in `data/`.
2. **Cleans**: duplicates, negative quantities, unknown SKUs, dates in `DD/MM/YYYY` format, missing channel (mark as "unknown").
3. Prints a **quality report**: how many rows removed / fixed, and why.
4. Computes net revenue per store, region and division, per month.
5. Produces a chart `my-work/revenue_by_store.png` highlighting Tokyo in March 2026.

## How to work in the app
1. Start a session: **+** next to **Sessions** → `ai-dojo`. Set the mode to **Plan**, **Tool permissions** to **Assisted**.
2. Describe the goal (the Mission above). Copilot proposes a **plan**: read it, ask for changes, then **approve**.
3. Switch the mode to **Interactive** (mode drop-down) so Copilot writes the script and waits for you at each step.
4. Click **Changes** to review the files created.
5. Ask Copilot to **run** the script and show the output. Open the **Terminal** tab of the review panel to see the run, if it is available on your screen.

## Prompt ideas
- `Write a Python script with pandas that loads @sales.csv and lists every data-quality problem you detect, before fixing anything.`
- `Add comments explaining each cleaning rule.`
- `Explain line by line what the cleaning function does.`
- When it breaks: `Run it again, read the error, fix the cause and explain it.`

## Success criteria
- The script runs without error and prints a quality report that **counts each type of anomaly**.
- You can explain, in your own words, **one** cleaning rule and why it is justified.
- You compared two numbers from the output with `monthly_summary.csv` and they match (within the duplicates and invalid rows removed).

## Bonus
Add a rule: alert when a store's monthly revenue drops by more than 30% versus the average of the previous 3 months.
