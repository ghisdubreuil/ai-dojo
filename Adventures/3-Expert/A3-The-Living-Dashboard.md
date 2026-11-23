# A3 — The living dashboard 📊 (Data · Expert)

**Duration: 90 min · Modes: Plan, then Autopilot (or Interactive) · Python + tests**

**Before you start:** Python must be available (see [prerequisites, Part 7](../../docs/00-prerequisites.md#7-for-builder-and-expert-levels-only-optional-until-you-get-there)).

## Context
The retail director wants an interactive dashboard to open every Monday, with automatic alerts and the **confidence level** of the numbers on display.

## Mission
Get Copilot to build an app (Streamlit suggested) that:
1. Reuses your cleaning pipeline (A2) as a tested module.
2. Shows revenue, average basket, margin by division and category, filters by region (6) / division (3) / store / period, and a division × region matrix view.
3. Includes a **"Data quality"** section (rows discarded, reasons).
4. Detects and explains **anomalies** (e.g. Tokyo, March 2026).
5. Is covered by at least 5 tests (`pytest`).

## How to work in the app
1. Start a session in **Plan** mode with your goal. Do not approve until the plan is clear: architecture, files, tests. Ask for changes at least once.
2. Approve, then switch to **Autopilot** (or stay in **Interactive**) for the build. Autopilot works on its own: stay close and read the questions it asks.
3. When done, click **Changes** and review every file.
4. Ask Copilot to run the tests and show the result. Then ask it to start the dashboard. Use the **Browser** tab of the review panel to see the running app, if it is available; otherwise open the address Copilot gives you in your web browser.

## Prompt ideas
- Add your conventions (tests, no needless dependencies) to `.github/copilot-instructions.md` and observe the difference in the next session.
- `Review your code like a critical reviewer: where could a calculation be wrong?`

## Success criteria
- The dashboard runs and the tests pass.
- The dashboard numbers **match those from A2**.
- You asked Copilot to **justify** one figure and verified it independently.

## Bonus
Have Copilot generate a "How to read this dashboard" page for non-technical colleagues.
