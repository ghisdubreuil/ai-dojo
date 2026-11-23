# Warm-up adventure — Your first Copilot reflex

**Duration: 15 min · Level: everyone · No coding knowledge required · Mode: Ask**

**Before you start:** you completed the [prerequisites](../docs/00-prerequisites.md), your Codespace is open and you did [the setup guide](../docs/02-setup-click-by-click.md) (at least Parts 1 to 4). If you have not read the [introduction to Copilot](../docs/01-getting-started-with-copilot.md), do it now (5 min).

## Context
Welcome to **Maison Orélia**, a fictional luxury house. You are a newcomer and you are handed files you have never seen. Your mission: tame your copilot.

## Step 1 — Understand the company (2 min)
1. In the **Explorer** (left), click the small arrow **›** next to the folder `docs` to open it.
2. Click `organisation.md`.
   - ✅ The file opens in the editor.
3. Press `Ctrl + Shift + V` (Mac: `Command + Shift + V`) to see it nicely formatted.
   - ✅ You see two tables: 3 divisions and 6 regions.
4. Read it. Write down (in your head) the 3 divisions.

## Step 2 — Open Copilot in Ask mode (1 min)
1. Click the **chat icon** in the title bar at the top of the window (or press `Ctrl + Alt + I`).
2. At the bottom of the Chat panel, click the drop-down that says **Agent** (or **Plan**), then click **Ask**.
   - ✅ The drop-down says **Ask**.
3. If an old conversation is shown, click the **+** icon at the top of the Chat panel to start a new chat.

## Step 3 — Ask about a file (4 min)
1. In the **Explorer**, open the folder `data` and click `products.csv` so you can see it.
2. Click in the text box at the bottom of the Chat panel.
3. Type `#`, then type `products`, then click the suggestion `products.csv` in the pop-up list.
   - ✅ A tag with the file name appears in the text box.
4. Click after the tag and type this question (or copy-paste it):
   ```
   Explain this file to me as if I were new to the company. What does each column mean?
   ```
5. Press **Enter** and wait until the answer stops.
6. Read the answer. Check it against the file: pick one product in the editor and verify that Copilot described its columns correctly.
   - ✅ Success: Copilot mentions division, category, price and cost.
   - 🆘 If Copilot says it cannot see the file: repeat step 3 and make sure the tag with the file name is really in your message.

## Step 4 — Ask for a calculation, and make it show its work (4 min)
1. Keep the same chat. Click in the text box and type (copy-paste is fine):
   ```
   Which division has the highest average price? Show me how you compute it, step by step.
   ```
2. Press **Enter** and wait.
3. Check the answer by hand:
   - Click `products.csv` in the Explorer.
   - Pick the division Copilot named and look at 3 or 4 of its prices.
   - Ask yourself: "Is it plausible that this division has the highest prices?"
   - ✅ Expected: **Watches & Fine Jewelry** (its prices are in the thousands).
4. Notice whether Copilot showed its method. If not, type: `Show your calculation.` and press **Enter**.

## Step 5 — Be tricky (3 min)
1. Click the **+** icon to start a **new chat**.
2. Ask this deliberately vague question and press **Enter**:
   ```
   Which are the best products?
   ```
3. Observe: did Copilot ask what you mean by "best"? Or did it pick a definition itself (price, margin…)?
4. Now answer precisely, in the same chat:
   ```
   By "best" I mean the highest margin in euros. Use #products.csv and show the top 5 with the calculation.
   ```
   (Type `#`, choose `products.csv` in the list, and keep the rest of the sentence.)
5. Verify one line by hand: margin = price − cost.

## What to remember
- A **precise question** (goal, file, format) gives a better answer than a vague one.
- Copilot can be wrong: **check one number by hand**.
- You can keep talking: "shorter", "as a table", "explain step 2".

## ✅ Checklist: you are done when…
- [ ] You opened Chat and switched to **Ask** mode.
- [ ] You gave Copilot a file with `#`.
- [ ] You verified at least one number yourself.
- [ ] You saw the difference between a vague and a precise question.

## Choose your track
| Track | Discovery | Builder | Expert |
|---|---|---|---|
| A. Data analysis | [A1](./1-Discovery/A1-The-Sales-Mystery.md) | [A2](./2-Builder/A2-Clean-and-Analyze.md) | [A3](./3-Expert/A3-The-Living-Dashboard.md) |
| B. Knowledge agent | [B1](./1-Discovery/B1-The-Rule-Keeper.md) | [B2](./2-Builder/B2-The-Maison-Voice.md) | [B3](./3-Expert/B3-The-Knowledge-Agent.md) |
| C. Workflow | [C1](./1-Discovery/C1-Map-the-Process.md) | [C2](./2-Builder/C2-The-Great-Sort.md) | [C3](./3-Expert/C3-The-End-to-End-Workflow.md) |
