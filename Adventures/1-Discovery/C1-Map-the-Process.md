# C1 — Map the process 🗺️ (Workflow · Discovery)

**Duration: 40 min · Mode: Ask · No code to write**

## Context
Customer care at Maison Orélia loses 2 hours a day on manual sorting. Before automating anything, you must **understand and draw** the current process, find the weak points, and design a better one with Copilot as your assistant.

## Files used
- `docs/current-returns-process.md` — the process described in words.
- You will create `my-work/current-process.md` with your results.

## Quick reminders
- **Open Chat:** chat icon in the title bar, or `Ctrl + Alt + I`.
- **Mode:** the drop-down at the bottom of the Chat panel must say **Ask**.
- **New chat:** **+** icon at the top of the Chat panel.
- **Preview a Markdown file:** open it, then `Ctrl + Shift + V` (Mac: `Command + Shift + V`).

---

## Step 1 — Read the process (4 min)
1. In the **Explorer** (left), click the arrow **›** next to `docs`.
2. Click `current-returns-process.md`.
3. Press `Ctrl + Shift + V` to see it formatted.
4. Read the 7 steps and the list of pain points. With a pen or in your head, answer: **who** does what, and **when**?

## Step 2 — Prepare Copilot (1 min)
1. Open Chat (chat icon in the title bar).
2. Check the drop-down at the bottom says **Ask** (if not, click it and choose **Ask**).
3. Click the **+** icon to start a new chat.

## Step 3 — Ask for a diagram (8 min)
1. Click in the text box. Type `#`, then `current-returns`, and click `current-returns-process.md` in the list.
2. After the tag, type:
   ```
   Turn this process into a Mermaid flowchart (flowchart TD). Use one subgraph per actor: Customer, Advisor, Coordinator, Workshop, Manager. Keep the step numbers in the box labels. Give me only the code block.
   ```
3. Press **Enter** and wait.
   - ✅ You get a block of text starting with ```` ```mermaid ```` and `flowchart TD`.
4. Create your file:
   - In the Explorer, right-click the folder `my-work`.
   - Click **New File**.
   - Type `current-process.md` and press **Enter**.
   - ✅ An empty file opens in the editor.
5. Copy the whole code block from Copilot's answer, including the lines with the three backticks (use the **copy** icon on the code block, or select the text and press `Ctrl + C`).
6. Click inside your new empty file, press `Ctrl + V` to paste, then `Ctrl + S` to save.
7. Press `Ctrl + Shift + V` (Mac: `Command + Shift + V`) to open the preview.
   - ✅ You see **boxes and arrows**, not code.
   - 🆘 If you still see code: wait 30 seconds and try again (an extension may still be loading). If it fails, tell Copilot: `Give me the same process as a numbered list with arrows (→) instead.` and continue; the diagram is a bonus.
   - 🆘 If you see an error message in the preview: copy it into the chat with `Fix this Mermaid diagram:` and paste the code again.
8. Compare the diagram with the original text. Did Copilot **forget** a step or **invent** one? Fix it by asking: `Step 6 is missing. Add it and give me the corrected code.`

## Step 4 — Rank the pain points (6 min)
1. Back in the Chat, type:
   ```
   List the pain points of this process and rank them on a table with columns: pain point, impact (high/medium/low), effort to fix (high/medium/low), who is affected.
   ```
2. Press **Enter**.
3. Read the table critically. Do you agree with the **impact** and **effort** ratings? Ask: `Why did you rate "inconsistent replies" as high impact?`
4. Change one rating yourself: type `I think the weekly report is low impact, because it is only a reporting delay. Update the table.` and see how Copilot reacts (does it adapt, push back, or just agree?).

## Step 5 — What to automate, what to keep human (8 min)
1. Type:
   ```
   Which 3 steps of this process are good candidates for automation, and which 2 must remain human? Justify each in one sentence.
   ```
2. Press **Enter**.
3. Challenge it: type `What could go wrong if step 5 (writing the reply) were fully automated?`
   - A good answer mentions **wrong promises, outdated rules, tone, and sensitive customers**.
4. Decide for yourself: which step would you keep human, and why? Write your decision in the chat (`I decide to keep step X human because ...`) so Copilot can use it next.

## Step 6 — Design the target process (7 min)
1. Type:
   ```
   Write the target process in 6 steps maximum. Mark clearly which step needs human validation and who does it. Use my decisions above.
   ```
2. Press **Enter**.
3. Copy the answer. In the Explorer, click your file `current-process.md` (tab at the top of the editor, or in `my-work`).
4. Click at the **end** of the file (press `Ctrl + End`), press **Enter** twice, type `## Target process` and press **Enter**, then paste with `Ctrl + V`. Save with `Ctrl + S`.

---

## ✅ Success checklist
- [ ] A readable diagram (or a numbered list) saved in `my-work/current-process.md`.
- [ ] A ranked table of pain points where **you** changed at least one rating.
- [ ] A target process with **one clearly identified human validation step**.
- [ ] You challenged at least one Copilot suggestion.

## Bonus
Ask: `Estimate the time saved in hours per week if the sorting is automated. List your assumptions.` Then judge: are the assumptions realistic for a team of 6 advisors handling 240 tickets a month?

## Going further
Ready to automate the sort? Try [C2 — The great sort](../2-Builder/C2-The-Great-Sort.md).
