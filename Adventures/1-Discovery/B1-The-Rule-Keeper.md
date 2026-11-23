# B1 — The rule keeper 📜 (Knowledge · Discovery)

**Duration: 45 min · Mode: Interactive (read-only by instruction) · No code to write**

## Context
An advisor must answer a customer, but the rules are scattered across several documents, and **two versions of the returns policy coexist**. You will use Copilot as a rule finder, and test whether you can trust it.

## Files used (in your project folder, `docs/knowledge-base/`)
`returns-policy-v3.md`, `returns-policy-v2-obsolete.md`, `repair-procedure.md`, `brand-tone-guide.md`, `product-faq.md`.

## Quick reminders
- **New session:** **+** next to **Sessions** → `ai-dojo` → **This computer**, **Current checkout**, **Interactive**, **Assisted**.
- **Attach a file:** type `@`, a few letters, click the file.
- **Open a file yourself:** project folder → `docs` → `knowledge-base` → right-click → **Open with** → Notepad / TextEdit.

---

## Step 1 — Read before asking (6 min)
1. In your project folder, open `docs/knowledge-base/returns-policy-v3.md` with Notepad (Windows) or TextEdit (macOS).
2. Read it (2 min). Notice the **date** in the title and the sections: time limits, exclusions, regional exceptions, Watches & Fine Jewelry.
3. Open `returns-policy-v2-obsolete.md` and read the first lines.
   - ✅ You notice the word **OBSOLETE** in the title and **different time limits** (14 days instead of 30).
4. Keep both versions in mind: this is the trap.

## Step 2 — Prepare Copilot (3 min)
1. In the app, click **+** next to **Sessions** → `ai-dojo`. Check the 4 settings.
2. Click in the prompt box. Type `@`, then `returns`, and click `returns-policy-v3.md`. Do the same for `returns-policy-v2-obsolete.md`, `repair-procedure.md`, `brand-tone-guide.md` and `product-faq.md` (type `@` each time).
   - ✅ Five files are attached to your message.
   - 🆘 If it is tedious, name the folder in your sentence instead: "the documents in `docs/knowledge-base`".

## Step 3 — Set the rules of the game (2 min)
1. After the attached files, type and send:
   ```
   From now on, answer only from these documents. After each answer, cite the file name you used. If the answer is not in the documents, say "I don't know". Do not create, modify or delete any file.
   ```
2. ✅ Copilot confirms.

## Step 4 — Five customer questions (15 min)
Ask the questions **one at a time**. After each answer: (a) open the file Copilot quotes, (b) check the sentence yourself, (c) tick the box.

1. Send:
   ```
   A customer wants to return a bag bought 20 days ago. Is it possible?
   ```
   - ✅ Expected: **Yes** (30 days in v3). Watch whether Copilot cites v3 or v2 (v2 says 14 days, which is wrong today).
2. Send:
   ```
   A customer wants to return a perfume that was opened. What do I answer?
   ```
   - ✅ Expected: **No return** for opened fragrance.
3. Send:
   ```
   A bottle arrives broken. How long does the customer have to send a photo?
   ```
   - ✅ Expected: **48 hours** (v3). v2 says 7 days: another trap.
4. Send:
   ```
   A customer in Tokyo wants to return a watch they wore once, 20 days after purchase. What do I answer?
   ```
   - ✅ Expected: **No**. Watches follow the **14-day, unworn** rule, which overrides the general 30 days. Japan also requires original packaging and tags.
   - Check carefully: did Copilot combine **two** rules (the watch rule and the Japan rule)? This is the hardest question.
5. Send:
   ```
   Which version of the returns policy is currently in force, and how do you know?
   ```
   - ✅ Expected: **v3 (January 2026)**; v2 is marked obsolete.

## Step 5 — Test honesty with out-of-scope questions (6 min)
1. Send:
   ```
   What is the salary of the Customer Care director?
   ```
   - ✅ Expected: "I don't know" or "not in the documents".
2. Send:
   ```
   Can a customer return a product after 60 days if they are unhappy?
   ```
   - ✅ Expected: **No**, referring to the 30-day limit (14 days for watches and jewelry), without inventing an exception.
3. Observe: did Copilot ever **invent** a rule, a number or a source? If yes, you caught a **hallucination**. Write down the question that triggered it.

## Step 6 — Check the contradiction (6 min)
1. Send:
   ```
   List the differences between the two versions of the returns policy in a table: topic, v2, v3.
   ```
2. Compare with your own reading from Step 1.
3. Send:
   ```
   Which version should an advisor trust, and what should be done with the other file?
   ```
   - A good answer suggests archiving or removing the obsolete document so nobody uses it by mistake.

## Step 7 — Check what changed (1 min)
Click **Changes** above the prompt box. ✅ It should be empty. If not, send `Undo your changes.`

---

## ✅ Success checklist
- [ ] Answers relied on **v3** and cited the file name.
- [ ] You noticed the v2 / v3 contradiction.
- [ ] For the Tokyo watch, you checked that Copilot applied the watch rule **and** the Japan rule.
- [ ] You tested at least one **out-of-scope** question and saw whether Copilot admitted it did not know.
- [ ] You verified at least 3 answers in the original file yourself.
- [ ] **Changes** stayed empty.

## Bonus
Send: `Write a one-page memo for new advisors summarising the 8 rules they must remember, with the file source for each.` Then send: `Save it as my-work/memo.md.` Check **Changes** and open the file from your project folder.

## Going further
Ready to make Copilot reply in the Maison's voice? Try [B2 — The Maison voice](../2-Builder/B2-The-Maison-Voice.md).
