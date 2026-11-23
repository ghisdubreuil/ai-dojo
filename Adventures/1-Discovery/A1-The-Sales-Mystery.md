# A1 — The sales mystery 🔎 (Data · Discovery)

**Duration: 30 min · Copilot mode: Ask · No code to write**

## Context
Management asks: "What happened in our sales?" You have `data/sales.csv`, `data/products.csv` (with the division) and `data/stores.csv` (with the region). Read `docs/organisation.md` first.

## Mission
Answer 4 questions in plain language, using Copilot Chat (`#file:data/sales.csv` gives it the file):
1. Which 3 stores and which 2 regions sell the most (revenue)?
2. Which division weighs the most? And within each division, which category?
3. Is there visible seasonality?
4. **Did a store behave abnormally in 2026?** Is it the whole region, or only one store in that region?

## Copilot hints
- `Using #file:data/sales.csv and #file:data/products.csv, compute revenue per store (quantity × price × (1 - discount)). Explain your method.`
- `Give me a month-by-month table for the store that looks odd.`
- `What follow-up questions should I ask management?`

## Success criteria
- You identified the **Tokyo Ginza drop in March 2026** and noticed that **Osaka** (same Japan region) is not affected.
- You asked Copilot **how it computed** its numbers.
- You spotted at least 2 data-quality issues (duplicates, negative quantities, badly formatted dates…).

## Bonus
Ask Copilot to draft a 5-line email to management with your 3 conclusions.
