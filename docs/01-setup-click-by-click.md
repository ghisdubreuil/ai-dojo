# Setup, click by click (10 minutes)

Do this once, before any adventure. Nothing to install on your computer: everything runs in your web browser.

> **About this guide.** Buttons and labels in VS Code and GitHub change from time to time. Every step has a **✅ You should see** check and a **🆘 If not** fallback. If your screen differs slightly, look for the closest match, or ask your facilitator.
> **Convention:** **bold** = something to click or a label on screen. `code style` = something to type or copy-paste exactly.

---

## Part 1 — Open your workspace (Codespace)

1. Open this repository's page in your web browser: `https://github.com/ghisdubreuil/ai-dojo`.
   - ✅ You should see the repository name at the top left and a list of files and folders (`Adventures`, `data`, `docs`…).
   - 🆘 If you see a "404" or "Not found": you are probably not signed in to GitHub. Click **Sign in** (top right), then reload the page.
2. Find the green button labelled **Code**, at the top right of the file list. Click it.
   - ✅ A small window opens with tabs (**Local**, **Codespaces**).
3. Click the **Codespaces** tab.
4. Click the green button that says **Create codespace on main** (the label may simply read **Create codespace**).
   - ✅ A new browser tab opens with a "Setting up your codespace" message and a progress bar.
   - 🆘 If a message says you cannot create a codespace (quota or policy): tell your facilitator. Your organisation may need to enable Codespaces for you.
5. **Wait 1 to 3 minutes** without closing the tab. The screen will change by itself.
   - ✅ You should see a code editor in your browser, with a left sidebar listing files (`Adventures`, `data`, `docs`…).
6. If a **Welcome** tab or a pop-up appears in the middle of the screen, close it by clicking the small **✕** on its tab or pop-up.
7. Wait until text stops scrolling in the black panel at the bottom (it is installing tools). This can take about a minute more.

### Your screen at a glance
| Zone | Where | What it is |
|---|---|---|
| **Explorer** | Left side. The icon at the top of the thin vertical bar (looks like two sheets of paper). | The list of files and folders. |
| **Editor** | Large central area. | Where files open, in tabs. |
| **Panel** (terminal) | Bottom. | For commands. **You can ignore it** in the no-code adventures. |
| **Chat icon** | Top of the window, in the title bar near the search box. | Opens Copilot Chat. |
| **Chat view** | Appears on the side when you open chat. | Where you talk to Copilot. |

---

## Part 2 — Open a file

1. In the **Explorer** (left), click the small arrow **›** next to the folder `data` to open it.
   - ✅ You see `products.csv`, `sales.csv`, `stores.csv`, `support_tickets.csv`.
2. Click once on `products.csv`.
   - ✅ The file opens in the central editor, as a table-like list with colours for each column.
   - 🆘 If it looks like plain text separated by commas: that is normal too. Colours come from an extension that may still be loading.
3. To go back to another file, click its name in the Explorer, or click its tab at the top of the editor.

---

## Part 3 — Open Copilot Chat

1. Click the **chat icon** in the title bar at the top of the window.
   - Keyboard alternative: `Ctrl + Alt + I` (Windows/Linux) or `Control + Command + I` (Mac).
   - ✅ A **Chat** panel opens with a text box at the bottom (it invites you to ask something).
   - 🆘 If a button asks you to **Sign in** or **Use GitHub Copilot**: click it and follow the browser prompts with the GitHub account that has Copilot.
   - 🆘 If nothing happens, wait one minute (extensions may still be loading) and try again. If it still fails, tell your facilitator.
2. Look at the bottom of the Chat panel, around the text box. You will see small drop-down controls, among them one labelled **Agent** (it may read **Ask**, **Plan** or **Agent** depending on the last choice) and one showing a **model name**.
3. Click the drop-down labelled **Agent** (or **Ask**/**Plan**).
4. Click **Ask** in the list.
   - ✅ The drop-down now says **Ask**. This is the safe mode: Copilot answers your questions but **does not change any file**.
   - 🆘 If you do not see **Ask**: choose the option whose description says it only answers questions without editing.
5. Leave the model drop-down as it is, unless your facilitator tells you otherwise.

---

## Part 4 — Send your first message

1. Click inside the text box at the bottom of the Chat panel.
2. Type: `Hello! In one sentence, what can you help me with in this project?`
3. Press **Enter** on your keyboard.
   - ✅ Words appear gradually: Copilot is answering. Wait until it stops.
4. Read the answer. You can scroll inside the Chat panel.

---

## Part 5 — Show Copilot a file (context)

Copilot answers better when you **point to the file**. Two ways:

**Way 1 — type `#`**
1. In the text box, type `#`.
   - ✅ A list of suggestions pops up (files, folders…).
2. Type a few letters of the file name, for example `products`.
3. Click the matching suggestion (for example `products.csv`) in the list, or use the arrow keys and press **Enter**.
   - ✅ A small tag with the file name appears in your message.
4. Then type your question after the tag and press **Enter**.

**Way 2 — type the full mention**
- You can also type the mention yourself: `#file:data/products.csv` followed by a space and your question.

To give a **whole folder**: type `#folder:docs/knowledge-base`.

---

## Part 6 — Useful habits

| I want to… | Do this |
|---|---|
| **Start fresh** on a new topic | Click the **+** icon at the top of the Chat panel (tooltip: **New Chat**). Previous answers stay available in the history. |
| **Ask a follow-up** | Just type in the same chat box: "shorter", "as a table", "explain step 2". |
| **Copy an answer** | Select the text with your mouse, then `Ctrl + C` (Mac: `Command + C`). Or use the **copy** icon shown on code or text blocks. |
| **Create a new file** | In the Explorer, right-click the folder `my-work` → **New File** → type the name (for example `notes.md`) → press **Enter**. Paste your text, then `Ctrl + S` to save. |
| **See a Markdown file nicely formatted** | Open the `.md` file, then click the small **preview** icon at the top right of the editor, or press `Ctrl + Shift + V` (Mac: `Command + Shift + V`). |
| **Stop a long answer** | Click the **Stop** (square) button that replaces the send button while Copilot writes. |

## You are ready
Go to the [warm-up adventure](../Adventures/StartHere.md).
