# Warm-up adventure — Your first Copilot reflex

**Duration: 20 min · Level: everyone · No coding knowledge required · Mode: Interactive**

**Before you start:** you completed the [prerequisites](../docs/00-prerequisites.md), read the [introduction to Copilot](../docs/01-getting-started-with-copilot.md) and did the [app tour](../docs/02-setup-click-by-click.md).

## Context
Welcome to **Maison Orélia**, a fictional luxury house. You are a newcomer and you are handed files you have never seen. Your mission: tame your copilot.

## Step 1 — Open your project folder on your computer (3 min)
1. Open the folder you pinned in the app tour (File Explorer or Finder).
   - 🆘 Lost it? In the app, open a session and ask: `What is the full path of this project folder?`, then paste it in File Explorer's address bar (Windows) or in Finder with `Shift + Command + G` (macOS).
2. Double-click the folder `docs`, then right-click `organisation.md` → **Open with** → **Notepad** (Windows) or **TextEdit** (macOS).
   - ✅ You see two tables: 3 divisions and 6 regions.
3. Read it (2 min). Remember the 3 divisions.

## Step 2 — Start a safe session (3 min)
1. In the app, click the **+** next to **Sessions** in the sidebar.
2. Under **Start session in**, click `ai-dojo`.
3. Below the prompt box, check: **Environment** = **This computer**, **Workspace** = **Current checkout**, mode = **Interactive**, **Tool permissions** = **Assisted**. (Change any that differ, see the [app tour, Part 2](../docs/02-setup-click-by-click.md#part-2--start-a-session-your-daily-gesture).)
4. Click in the prompt box, paste this and press **Enter**:
   ```
   Rule for this session: do not create, modify or delete any file unless I explicitly ask you to. Answer only from the project files.
   ```
   - ✅ Copilot confirms.

## Step 3 — Ask about a file (5 min)
1. In the prompt box, type `@`, then `products`, then click `products.csv` in the list.
   - ✅ The file is attached.
2. After it, type (or paste) and press **Enter**:
   ```
   Explain this file to me as if I were new to the company. What does each column mean?
   ```
3. Wait until the answer stops. If a **permission request** appears, read it and allow it if it is only about reading a project file.
4. **Check it yourself:** in your project folder, open `data/products.csv` (double-click, it opens in a spreadsheet). Pick one product and verify that Copilot described its columns correctly.
   - ✅ Success: Copilot mentions division, category, price and cost.
   - 🆘 If Copilot says it cannot see the file: repeat step 1 and make sure the file is attached.

## Step 4 — Ask for a calculation, and make it show its work (5 min)
1. In the same session, type and send:
   ```
   Which division has the highest average price? Show me how you compute it, step by step.
   ```
2. Check by hand in the spreadsheet: look at 3 or 4 prices in the division Copilot named.
   - ✅ Expected: **Watches & Fine Jewelry** (prices in the thousands).
3. If Copilot did not show its method, send: `Show your calculation.`

## Step 5 — Be tricky (4 min)
1. Start a **new session** (+ next to **Sessions**, **ai-dojo**, same settings, paste the safety sentence again).
2. Ask this deliberately vague question and press **Enter**:
   ```
   Which are the best products?
   ```
3. Observe: did Copilot ask what you mean by "best"? Or did it pick a definition itself (price, margin…)?
4. Answer precisely, in the same session:
   ```
   By "best" I mean the highest margin in euros (price minus cost). Use @products.csv and show the top 5 with the calculation.
   ```
5. Verify one line by hand in the spreadsheet: price − cost.

## Step 6 — Check what changed (1 min)
1. Click **Changes** above the prompt box.
   - ✅ It should be **empty**: Copilot respected your safety sentence.
   - If not, note which file it touched and send: `Undo your changes.` Then check **Changes** again.

## What to remember
- A **precise question** (goal, file, format) gives a better answer than a vague one.
- Copilot can be wrong: **check one number by hand**.
- Check **Changes** after every session: you are in charge.

## ✅ Checklist: you are done when…
- [ ] You started a session with the right settings (**Interactive**, **Assisted**).
- [ ] You attached a file with `@`.
- [ ] You verified at least one number yourself in the file.
- [ ] You saw the difference between a vague and a precise question.
- [ ] **Changes** was empty at the end.

## Choose your track
| Track | Discovery | Builder | Expert |
|---|---|---|---|
| A. Data analysis | [A1](./1-Discovery/A1-The-Sales-Mystery.md) | [A2](./2-Builder/A2-Clean-and-Analyze.md) | [A3](./3-Expert/A3-The-Living-Dashboard.md) |
| B. Knowledge agent | [B1](./1-Discovery/B1-The-Rule-Keeper.md) | [B2](./2-Builder/B2-The-Maison-Voice.md) | [B3](./3-Expert/B3-The-Knowledge-Agent.md) |
| C. Workflow | [C1](./1-Discovery/C1-Map-the-Process.md) | [C2](./2-Builder/C2-The-Great-Sort.md) | [C3](./3-Expert/C3-The-End-to-End-Workflow.md) |
