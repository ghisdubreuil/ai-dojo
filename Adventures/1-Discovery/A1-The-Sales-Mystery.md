# A1 — The sales mystery 🔎 (Data · Discovery)

**Duration: 45 min · Mode: Interactive (read-only by instruction) · No code to write**

## Context
Management asks: "What happened in our sales?" You will explore the numbers with Copilot, without writing any code, and you will **check** what it tells you.

## Files used (in your project folder, `data/`)
| File | What it is |
|---|---|
| `monthly_summary.csv` | Sales summarised per **month × store × division** (755 rows): `revenue_eur` and `units` (items sold). Already cleaned. |
| `stores.csv` | The 12 stores and their region. |
| `sales_sample.csv` | A small extract (114 rows) of the raw sales file. **It contains deliberate errors.** |

> **Why not the big file?** `sales.csv` has more than 21,000 rows. Adding up that many lines in conversation is where assistants slip. In this Discovery adventure we work on files of the right size. In the Builder level, Copilot writes a script to process the big file.

## Quick reminders
- **New session:** **+** next to **Sessions** → `ai-dojo` → check **This computer**, **Current checkout**, **Interactive**, **Assisted**.
- **Attach a file:** type `@`, a few letters, click the file.
- **Open a file yourself:** your project folder → `data` → double-click the CSV.

---

## Step 1 — Prepare your screen (4 min)
1. Open your project folder → `data` → double-click `monthly_summary.csv`.
   - ✅ A spreadsheet opens with columns `month`, `store_id`, `store_name`, `region`, `division`, `revenue_eur`, `units`.
2. Look at the first 5 rows: each row = one store, one division, one month. Keep this window open.
3. In the app, click **+** next to **Sessions** → `ai-dojo`. Check the 4 settings.
4. Paste and send the safety sentence:
   ```
   Rule for this session: do not create, modify or delete any file unless I explicitly ask you to. Answer only from the project files.
   ```

## Step 2 — Check that Copilot understood the file (4 min)
1. Type `@`, then `monthly`, click `monthly_summary.csv`.
2. After it, type and send:
   ```
   Describe this file in 3 sentences: the period covered, the number of stores, and what each column means.
   ```
3. Check in your spreadsheet: scroll to the top and bottom of the file.
   - ✅ Expected: **January 2025** to **September 2026**, **12 stores**, 3 divisions.
   - 🆘 If Copilot gets it wrong, send: `Check the first and last month again.`

## Step 3 — Question 1: which stores and regions sell the most? (6 min)
1. Send:
   ```
   Using @monthly_summary.csv, give me the top 3 stores and the top 2 regions by total revenue_eur over the whole period. Show the totals in a table and explain how you computed them.
   ```
   (Type `@`, pick the file, then continue the sentence.)
2. If a **permission request** appears (for example to run a calculation), read it; allow it if it only works on the project's files.
3. Read the table. Roughly, **New York Madison** should be at or near the top.
   - ⚠️ Treat exact amounts with caution. Note the **order** (1st, 2nd, 3rd), not every digit.
4. Test it: send `Are you sure about the total of the first store? Show how you obtained it.`
5. Observe: does it confirm, correct itself, or show its work?

## Step 4 — Question 2: which division weighs the most? (4 min)
1. Send:
   ```
   Which division generates the most revenue_eur, and what share of the total does each division represent? Table please.
   ```
   - ✅ Expected: **Watches & Fine Jewelry** is the biggest, around half of the revenue; **Fragrance & Beauty** the smallest.
2. Send: `Why would this division weigh so much, given only the data in the file?` Does Copilot stick to the data (the price range) or invent reasons?

## Step 5 — Question 3: is there seasonality? (6 min)
1. Send:
   ```
   For the year 2025 only, give me the total units per month, all stores together. Which months are the highest and the lowest?
   ```
   (We use **units**: revenue jumps around because a single watch costs thousands of euros.)
   - ✅ Expected: **November and December** are the highest; **January, February and August** are among the lowest.
2. Send: `Show the result as a simple bar chart made of text characters.`
3. Send: `Explain in one sentence what a retail director should do with this information.`

## Step 6 — Question 4: did a store behave abnormally in 2026? (10 min)
This is the heart of the mystery.
1. Send:
   ```
   Compare total units in March 2026 versus March 2025 for each store. Show the percentage change in a table, sorted from the biggest drop.
   ```
   - ✅ Expected: one store stands out with a drop of roughly **−40 to −50%**: **Tokyo Ginza**.
   - 🆘 If Copilot hesitates, send: `Which store has the largest drop and by how much?`
2. **Check by hand:** in your spreadsheet window, apply a filter on `store_id` = `B04` and `month` = `2026-03`. Add the 3 `units` values. Do the same for `2025-03`.
   - ✅ Your totals should be close to Copilot's.
   - 🆘 Don't know how to filter? Use the spreadsheet's search (`Ctrl + F` on Windows, `Command + F` on Mac) for `2026-03` and look at the rows of `Tokyo Ginza`.
3. Ask whether it is the whole region or one store:
   ```
   Tokyo Ginza and Osaka Shinsaibashi are both in the Japan region. Compare their monthly units for 2026 and tell me whether Osaka shows the same drop.
   ```
   - ✅ Expected: **Osaka is not affected**. The problem is local to Tokyo Ginza.
4. Send: `What are 3 possible explanations to investigate, and what data would I need to confirm each one?`
   - Notice that Copilot **cannot know** the cause from this file. A good answer lists hypotheses and the data needed.

## Step 7 — Spot data-quality problems (10 min)
1. In your project folder, open `data/sales_sample.csv` in the spreadsheet. Scroll for one minute and note anything odd.
2. In the app, send:
   ```
   Look at @sales_sample.csv. List every data-quality problem you find (duplicates, negative quantities, unknown product codes, badly formatted dates, missing values). For each problem, give the row and explain why it is a problem.
   ```
3. Verify each finding yourself in the spreadsheet (use search):
   - `SKU999` → an unknown product code.
   - A date with `/` (such as `14/03/2026`) → day/month/year instead of year-month-day.
   - A **negative** number in `quantity`, such as `-1`.
   - An **empty cell** in `channel`.
4. Count: problems Copilot found, problems you found, and Copilot's wrong or missing findings.
   - ✅ The sample contains **five types** of problems (including two duplicated rows).

## Step 8 — Check what changed (1 min)
Click **Changes** above the prompt box. ✅ It should be empty. If not, send `Undo your changes.`

---

## ✅ Success checklist
- [ ] You identified the **Tokyo Ginza drop in March 2026** and saw that **Osaka** is not affected.
- [ ] You asked Copilot **how it computed** at least once and checked one number yourself.
- [ ] You found at least 2 data-quality problems in `sales_sample.csv` by yourself.
- [ ] **Changes** stayed empty.

## Bonus
Send: `Write a 5-line email to the retail director with my 3 main conclusions.` Then send: `Save it as my-work/email.md.` Click **Changes** to see the new file, and open it from your project folder (`my-work`).

## Going further
Ready to build a repeatable analysis? Try [A2 — Clean and analyze](../2-Builder/A2-Clean-and-Analyze.md).
