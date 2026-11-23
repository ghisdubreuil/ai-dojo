# A1 — The sales mystery 🔎 (Data · Discovery)

**Duration: 40 min · Mode: Ask · No code to write**

## Context
Management asks: "What happened in our sales?" You will explore the numbers with Copilot, without writing a single line of code, and you will **check** what it tells you.

## Files used
| File | What it is |
|---|---|
| `data/monthly_summary.csv` | Sales summarised per **month × store × division** (755 rows): `revenue_eur` and `units` (items sold). Already cleaned. |
| `data/stores.csv` | The 12 stores and their region. |
| `data/sales_sample.csv` | A small extract (114 rows) of the raw sales file. **It contains deliberate errors.** |

> **Why not the big file?** `sales.csv` has more than 21,000 rows. A chat assistant cannot reliably read that much text: it may guess instead of calculating. Giving Copilot a file of the right size is part of good practice. You will work on the big file in the Builder level.

## Quick reminders (from the setup guide)
- **Open Chat:** click the chat icon in the title bar, or press `Ctrl + Alt + I`.
- **Check the mode:** the drop-down at the bottom of the Chat panel must say **Ask**.
- **New chat:** click the **+** icon at the top of the Chat panel.
- **Give a file:** in the text box type `#`, type a few letters of the file name, click the suggestion.

---

## Step 1 — Prepare your screen (3 min)
1. In the **Explorer** (left), click the arrow **›** next to the folder `data`.
2. Click `monthly_summary.csv` to open it.
   - ✅ You see columns: `month`, `store_id`, `store_name`, `region`, `division`, `revenue_eur`, `units`.
3. Look at the first 5 rows. Each row = one store, one division, one month.
4. Open Copilot Chat (chat icon, top of the window).
5. Click the drop-down at the bottom of the Chat panel and choose **Ask**.
6. Click the **+** icon to start a new chat.

## Step 2 — Check that Copilot understood the file (3 min)
1. Click in the text box. Type `#`, then `monthly`, and click `monthly_summary.csv` in the list.
2. After the tag, type:
   ```
   Describe this file in 3 sentences: the period covered, the number of stores, and what each column means.
   ```
3. Press **Enter**. Wait until the answer stops.
4. Check against the file: scroll to the top and bottom of `monthly_summary.csv` in the editor.
   - ✅ Expected: from **January 2025** to **September 2026**, **12 stores**, 3 divisions.
   - 🆘 If Copilot gets the period wrong, tell it: `Check the first and last month again.`

## Step 3 — Question 1: which stores and regions sell the most? (6 min)
1. In the same chat, type (copy-paste is fine):
   ```
   Using #monthly_summary.csv, give me the top 3 stores and the top 2 regions by total revenue_eur over the whole period. Show the totals in a table and explain how you computed them.
   ```
   (Type `#`, pick the file in the list, then continue the sentence.)
2. Press **Enter** and wait.
3. Read the table. Are the totals in euros? Does Copilot explain its method?
4. Keep the answer in mind. Roughly, **New York Madison** should be at or near the top.
   - ⚠️ The totals Copilot gives may differ from the real ones by a few percent. A chat assistant adding up 755 numbers can slip. This is **normal**: write down the order (1st, 2nd, 3rd) and treat exact amounts with caution.
5. Type a follow-up to test it: `Are you sure about the total of the first store? List the rows you added up.`
6. Observe: does it confirm, correct itself, or show the rows? This is the verification reflex.

## Step 4 — Question 2: which division weighs the most? (4 min)
1. Type:
   ```
   Which division generates the most revenue_eur, and what share of the total does each division represent? Table please.
   ```
2. Press **Enter**.
   - ✅ Expected: **Watches & Fine Jewelry** is the biggest, around half of the revenue; **Fragrance & Beauty** the smallest.
3. Ask: `Why would this division weigh so much, given only the data in the file?` and check whether Copilot sticks to the data (the price range) or invents reasons.

## Step 5 — Question 3: is there seasonality? (6 min)
1. Type:
   ```
   For the year 2025 only, give me the total units per month, all stores together. Which months are the highest and the lowest?
   ```
   (We use **units** here: revenue jumps around because a single watch costs thousands of euros.)
2. Press **Enter**.
   - ✅ Expected: **November and December** are the highest; **January, February and August** are among the lowest.
3. Type: `Show the result as a simple text bar chart.` and press **Enter**. Copilot may draw bars with characters.
4. Type: `Explain in one sentence what a retail director should do with this information.`

## Step 6 — Question 4: did a store behave abnormally in 2026? (10 min)
This is the heart of the mystery.
1. Start by comparing a month to the same month last year. Type:
   ```
   Compare total units in March 2026 versus March 2025 for each store. Show the percentage change in a table, sorted from the biggest drop.
   ```
2. Press **Enter**.
   - ✅ Expected: one store stands out with a drop of roughly **−40 to −50%**: **Tokyo Ginza**.
   - 🆘 If Copilot hesitates, ask: `Which store has the largest drop and by how much?`
3. Check by hand:
   - In the editor, click in `monthly_summary.csv` and press `Ctrl + F` (Mac: `Command + F`).
   - Type `2026-03,B04` and look at the 3 matching rows (one per division). Add their `units` in your head.
   - Do the same with `2025-03,B04`.
   - ✅ Your totals should be close to what Copilot reported.
4. Now ask whether it is the whole region or one store:
   ```
   Tokyo Ginza and Osaka Shinsaibashi are both in the Japan region. Compare their monthly units for 2026 and tell me whether Osaka shows the same drop.
   ```
5. Press **Enter**.
   - ✅ Expected: **Osaka is not affected**. The problem is local to Tokyo Ginza.
6. Finally ask: `What are 3 possible explanations to investigate, and what data would I need to confirm each one?`
   - Notice that Copilot **cannot know** the cause from this file. A good answer lists hypotheses and the data needed.

## Step 7 — Spot data-quality problems (8 min)
1. In the Explorer, click `sales_sample.csv` to open it. It has about 114 rows: scroll through it for one minute and note anything odd.
2. In the Chat, type:
   ```
   Look at #sales_sample.csv. List every data-quality problem you find (duplicates, negative quantities, unknown product codes, badly formatted dates, missing values). For each problem, give the row and explain why it is a problem.
   ```
3. Press **Enter**.
4. Verify each finding by hand. In the editor, press `Ctrl + F` and search for:
   - `SKU999` → an unknown product code.
   - `/` → a date written as day/month/year instead of year-month-day.
   - `,-1,` → a negative quantity.
   - `,,` → a missing value (an empty channel).
5. Count how many problems Copilot found, how many you found, and how many of its findings were wrong or missing.
   - ✅ The sample contains **five types** of problems (including two duplicated rows).

---

## ✅ Success checklist
- [ ] You identified the **Tokyo Ginza drop in March 2026** and saw that **Osaka** (same region) is not affected.
- [ ] You asked Copilot **how it computed** at least once and checked one number yourself.
- [ ] You found at least 2 data-quality problems in `sales_sample.csv` by yourself.
- [ ] You can say, in one sentence, why Copilot should not be given a 21,000-row file to add up.

## Bonus
Ask Copilot: `Write a 5-line email to the retail director with my 3 main conclusions.` Create a file in `my-work` (right-click the folder `my-work` → **New File** → `email.md` → **Enter**), paste the email, and press `Ctrl + S` to save.

## Going further
Ready to build a repeatable analysis? Try [A2 — Clean and analyze](../2-Builder/A2-Clean-and-Analyze.md).
