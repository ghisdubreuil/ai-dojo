# B1 — The rule keeper 📜 (Knowledge · Discovery)

**Duration: 40 min · Mode: Ask · No code to write**

## Context
An advisor must answer a customer, but the rules are scattered across several documents, and **two versions of the returns policy coexist**. You will use Copilot as a rule finder, and test whether you can trust it.

## Files used
All in `docs/knowledge-base/`: `returns-policy-v3.md`, `returns-policy-v2-obsolete.md`, `repair-procedure.md`, `brand-tone-guide.md`, `product-faq.md`.

## Quick reminders
- **Open Chat:** chat icon in the title bar, or `Ctrl + Alt + I`.
- **Mode:** the drop-down at the bottom of the Chat panel must say **Ask**.
- **New chat:** the **+** icon at the top of the Chat panel.
- **Give a folder:** in the text box, type `#folder:docs/knowledge-base` exactly, then a space.

---

## Step 1 — Read before asking (5 min)
1. In the **Explorer** (left), click the arrow **›** next to `docs`, then next to `knowledge-base`.
2. Click `returns-policy-v3.md`. Press `Ctrl + Shift + V` (Mac: `Command + Shift + V`) to see it formatted.
3. Read it (2 min). Notice the title with the **date** and the sections: time limits, exclusions, regional exceptions, Watches & Fine Jewelry.
4. Click `returns-policy-v2-obsolete.md` and read the first lines.
   - ✅ You notice the word **OBSOLETE** in the title and **different time limits** (14 days instead of 30).
5. Keep both versions in mind: this is the trap.

## Step 2 — Prepare Copilot (2 min)
1. Click the chat icon in the title bar to open Chat.
2. At the bottom of the Chat panel, click the drop-down and choose **Ask**.
3. Click the **+** icon to start a new chat.
4. Click in the text box and type `#folder:docs/knowledge-base ` (with a space at the end).
   - ✅ A tag for the folder appears in the box.
   - 🆘 If no tag appears: type `#`, type `folder`, click **Folder…** or the folder suggestion, and pick `docs/knowledge-base`.

## Step 3 — Set the rules of the game (2 min)
1. After the folder tag, type:
   ```
   From now on, answer only from these documents. After each answer, cite the file name you used. If the answer is not in the documents, say "I don't know".
   ```
2. Press **Enter**. Copilot should confirm.

## Step 4 — Five customer questions (15 min)
Ask the questions **one at a time**. After each answer: (a) find the quoted file in the Explorer, (b) check the sentence yourself, (c) tick the box.

1. Type and send:
   ```
   A customer wants to return a bag bought 20 days ago. Is it possible?
   ```
   - ✅ Expected: **Yes** (30 days in v3). Watch whether Copilot cites v3 or v2 (v2 would say 14 days, which is wrong today).
2. Type and send:
   ```
   A customer wants to return a perfume that was opened. What do I answer?
   ```
   - ✅ Expected: **No return** for opened fragrance.
3. Type and send:
   ```
   A bottle arrives broken. How long does the customer have to send a photo?
   ```
   - ✅ Expected: **48 hours** (v3). v2 says 7 days: another trap.
4. Type and send:
   ```
   A customer in Tokyo wants to return a watch they wore once, 20 days after purchase. What do I answer?
   ```
   - ✅ Expected: **No**. Watches follow the **14-day, unworn** rule, which overrides the general 30 days. Japan also requires original packaging and tags.
   - Check carefully: did Copilot combine **two** rules (the watch rule and the Japan rule)? That is the hardest question.
5. Type and send:
   ```
   Which version of the returns policy is currently in force, and how do you know?
   ```
   - ✅ Expected: **v3 (January 2026)**; v2 is marked obsolete.

## Step 5 — Test honesty with out-of-scope questions (6 min)
1. Type and send:
   ```
   What is the salary of the Customer Care director?
   ```
   - ✅ Expected: "I don't know" or "not in the documents".
2. Type and send:
   ```
   Can a customer return a product after 60 days if they are unhappy?
   ```
   - ✅ Expected: **No**, referring to the 30-day limit (and 14 days for watches and jewelry), without inventing an exception.
3. Observe: did Copilot ever **invent** a rule, a number or a source? If yes, you caught a **hallucination**. Write down the question that triggered it.

## Step 6 — Check the contradiction (5 min)
1. Type and send:
   ```
   List the differences between the two versions of the returns policy in a table: topic, v2, v3.
   ```
2. Compare with your own reading from Step 1.
3. Type and send:
   ```
   Which version should an advisor trust, and what should be done with the other file?
   ```
   - A good answer suggests archiving or removing the obsolete document so nobody uses it by mistake.

---

## ✅ Success checklist
- [ ] Answers relied on **v3** and cited the file name.
- [ ] You noticed the v2 / v3 contradiction.
- [ ] For the Tokyo watch, you checked that Copilot applied the watch rule **and** the Japan rule.
- [ ] You tested at least one **out-of-scope** question and saw whether Copilot admitted it did not know.
- [ ] You verified at least 3 answers in the original file yourself.

## Bonus
Ask: `Write a one-page memo for new advisors summarising the 8 rules they must remember, with the file source for each.` Create `memo.md` in `my-work` (right-click `my-work` → **New File** → `memo.md` → **Enter**), paste the memo, press `Ctrl + S`.

## Going further
Ready to make Copilot reply in the Maison's voice? Try [B2 — The Maison voice](../2-Builder/B2-The-Maison-Voice.md).
