# C1 — Map the process 🗺️ (Workflow · Discovery)

**Duration: 45 min · Mode: Interactive (read-only except where stated) · No code to write**

## Context
Customer care at Maison Orélia loses 2 hours a day on manual sorting. Before automating anything, you must **understand and draw** the current process, find the weak points, and design a better one with Copilot as your assistant.

## Files used
- `docs/current-returns-process.md` — the process described in words.
- You will ask Copilot to create `my-work/current-process.md` with your results.

## Quick reminders
- **New session:** **+** next to **Sessions** → `ai-dojo` → **This computer**, **Current checkout**, **Interactive**, **Assisted**.
- **Attach a file:** type `@`, a few letters, click the file.
- **Open a file yourself:** project folder → right-click → **Open with** → Notepad / TextEdit.

---

## Step 1 — Read the process (5 min)
1. In your project folder, open `docs/current-returns-process.md` with Notepad / TextEdit.
2. Read the 7 steps and the list of pain points. With a pen or in your head, answer: **who** does what, and **when**?

## Step 2 — Prepare Copilot (3 min)
1. In the app, click **+** next to **Sessions** → `ai-dojo`. Check the 4 settings.
2. Paste and send:
   ```
   Rule for this session: do not create, modify or delete any file unless I explicitly ask you to. Answer only from the project files.
   ```

## Step 3 — Ask for a text diagram (8 min)
1. Type `@`, then `current-returns`, click `current-returns-process.md`.
2. After it, type and send:
   ```
   Turn this process into a text flow diagram: one block per actor (Customer, Advisor, Coordinator, Workshop, Manager), numbered steps, and arrows (→) showing who passes the request to whom. Keep the step numbers of the document.
   ```
3. Compare the result with the original text. Did Copilot **forget** a step or **invent** one?
4. Fix it: `Step 6 is missing. Add it and show the corrected diagram.`
5. Now ask Copilot to save it (this is the first time a file may change):
   ```
   You may now create one file: my-work/current-process.md with this diagram. Do not touch any other file.
   ```
6. If a **permission request** appears, check that it concerns `my-work/current-process.md` only, then allow it.
7. Click **Changes** above the prompt box.
   - ✅ You see exactly one new file, `my-work/current-process.md`, with your diagram.
8. Open it from your project folder (`my-work`) with Notepad / TextEdit.

## Step 4 — Rank the pain points (6 min)
1. Send:
   ```
   List the pain points of this process in a table with columns: pain point, impact (high/medium/low), effort to fix (high/medium/low), who is affected. Do not modify any file.
   ```
2. Read the table critically. Do you agree with the ratings? Ask: `Why did you rate "inconsistent replies" as high impact?`
3. Change one rating yourself: send `I think the weekly report is low impact, because it is only a reporting delay. Update the table.` Does Copilot adapt, push back, or just agree?

## Step 5 — What to automate, what to keep human (8 min)
1. Send:
   ```
   Which 3 steps of this process are good candidates for automation, and which 2 must remain human? Justify each in one sentence.
   ```
2. Challenge it: send `What could go wrong if step 5 (writing the reply) were fully automated?`
   - A good answer mentions **wrong promises, outdated rules, tone, and sensitive customers**.
3. Decide for yourself: which step would you keep human, and why? Write it in the session (`I decide to keep step X human because …`) so Copilot can use it next.

## Step 6 — Design the target process (8 min)
1. Send:
   ```
   Write the target process in 6 steps maximum. Mark clearly which step needs human validation and who does it. Use my decisions above.
   ```
2. Ask Copilot to add it to your file:
   ```
   Add this target process at the end of my-work/current-process.md under a heading "Target process". Do not touch any other file.
   ```
3. Allow the permission request if it concerns that file only. Click **Changes**: ✅ one file modified.
4. Open `my-work/current-process.md` from your project folder and read the final result.

---

## ✅ Success checklist
- [ ] A readable text diagram saved in `my-work/current-process.md`.
- [ ] A ranked table of pain points where **you** changed at least one rating.
- [ ] A target process with **one clearly identified human validation step**.
- [ ] You challenged at least one Copilot suggestion.
- [ ] **Changes** showed only the file you authorised.

## Bonus 1 — A picture
Send: `Create my-work/process-diagram.html: a single self-contained web page that draws the target process as boxes and arrows. Do not touch any other file.` Then double-click the file in your project folder: it opens in your web browser.

## Bonus 2 — Time saved
Send: `Estimate the time saved in hours per week if the sorting is automated. List your assumptions.` Are the assumptions realistic for a team of 6 advisors handling 240 tickets a month?

## Going further
Ready to automate the sort? Try [C2 — The great sort](../2-Builder/C2-The-Great-Sort.md).
