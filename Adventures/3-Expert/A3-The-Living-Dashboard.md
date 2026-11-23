# A3 — The living dashboard 📊 (Data · Expert)

**Duration: 90 min · Copilot modes: Plan then Agent · Python + tests**

## Context
The retail director wants an interactive dashboard to open every Monday, with automatic alerts and the **confidence level** of the numbers on display.

## Mission
With **Plan**, then **Agent**, build an app (Streamlit suggested) that:
1. Reuses your cleaning pipeline (A2) as a tested module.
2. Shows revenue, average basket, margin by division and category, filters by region (6) / division (3) / store / period, and a division × region matrix view.
3. Includes a **"Data quality"** section (rows discarded, reasons).
4. Detects and explains **anomalies** (e.g. Tokyo, March 2026).
5. Is covered by at least 5 tests (`pytest`).

## Copilot hints
- Start with `/plan` and your goal. Do not approve until the plan is clear: architecture, files, tests.
- Edit `.github/copilot-instructions.md` with your conventions (tests, no needless dependencies) and observe the difference.
- `Review your code like a critical reviewer: where could a calculation be wrong?`

## Success criteria
- `streamlit run app.py` works in the Codespace.
- The dashboard numbers **match those from A2**.
- You asked the agent to **justify** one figure and verified it independently.

## Bonus
Have Copilot generate a "How to read this dashboard" page for non-technical colleagues.
