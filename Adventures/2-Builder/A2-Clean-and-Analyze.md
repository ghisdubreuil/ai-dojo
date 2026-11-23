# A2 — Clean and analyze 🧹 (Data · Builder)

**Duration: 45–60 min · Copilot modes: Ask, then Plan → Agent in small steps · Python (Copilot writes, you review)**

## Context
Management wants reliable revenue per store, region and division, month by month. But `data/sales.csv` is dirty. You will produce a **repeatable script** rather than a one-off manual calculation.

## Mission
Create `my-work/analyze_sales.py` that:
1. Loads the CSV files in `data/`.
2. **Cleans**: duplicates, negative quantities, unknown SKUs, dates in `DD/MM/YYYY` format, missing channel (mark as "unknown").
3. Prints a **quality report**: how many rows removed / fixed, and why.
4. Computes net revenue per store, region and division, per month.
5. Produces a chart `my-work/revenue_by_store.png` highlighting Tokyo in March 2026.

## Copilot hints
- `Write a Python script with pandas that loads #file:data/sales.csv and lists every data-quality problem you detect, before fixing anything.`
- `Add comments explaining each cleaning rule.`
- `Explain line by line what the cleaning function does.`
- When it breaks: paste the error in the chat with `Fix this error and explain the cause`.

## Success criteria
- The script runs with `python my-work/analyze_sales.py` without error.
- The quality report counts each type of anomaly.
- You can explain, in your own words, **one** cleaning rule and why it is justified.

## Bonus
Add a rule: alert when a store's monthly revenue drops by more than 30% versus the average of the previous 3 months.
